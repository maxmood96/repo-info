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
-	[`nats:2.2.1`](#nats221)
-	[`nats:2.2.1-alpine`](#nats221-alpine)
-	[`nats:2.2.1-alpine3.13`](#nats221-alpine313)
-	[`nats:2.2.1-linux`](#nats221-linux)
-	[`nats:2.2.1-nanoserver`](#nats221-nanoserver)
-	[`nats:2.2.1-nanoserver-1809`](#nats221-nanoserver-1809)
-	[`nats:2.2.1-scratch`](#nats221-scratch)
-	[`nats:2.2.1-windowsservercore`](#nats221-windowsservercore)
-	[`nats:2.2.1-windowsservercore-1809`](#nats221-windowsservercore-1809)
-	[`nats:2.2.1-windowsservercore-ltsc2016`](#nats221-windowsservercore-ltsc2016)
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
$ docker pull nats@sha256:f0c80abcc8d86c26b77b4cfbf150821d7e71ace88e2ea39d8a5bfa33caf0317a
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
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
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
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:786039ea5743e66f92097f4c98419cdb7755824388806faae9ca893626cda20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:11a99e623a9df5677bdcbcff33bd032975aabdc9c226e00410997607a5398ad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7303859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56ceabe89d18dd0b0c58d97b018484ed43d818791b7a1d9e5e8a09123c6cbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:02:20 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:02:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:02:24 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:02:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab87484469466c6eeb084bcbe5538907a8cca9e02c6c00ffc4e03bd68d4563`  
		Last Modified: Sat, 03 Apr 2021 03:03:06 GMT  
		Size: 4.5 MB (4490943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63537464a64606bc6b408c793c1b726d40b4b1a540a829516859d3405c203e37`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843bbc65e4b41319d487b9ba5eb3a58b709e795448cc632d75fb8f54d76868d9`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:5980c4f84be539fd1b559624db6fa63ee409f825e4a93fa441598e93115d4b15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6784924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f97d97f7e09aa5c9f936e0377789f200b06c8aabe846ce2591ebff76f7db8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:02:19 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:02:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:02:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:02:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:02:26 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:02:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d4b6ba6b297e822b0c0fe254f2d6b5afda81265eaf2481116af687cf66235c`  
		Last Modified: Sat, 03 Apr 2021 01:03:09 GMT  
		Size: 4.2 MB (4161834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0dfcf0132d6f11bd4762e4d1ec0b73f5ee36875a95dc78731673415f9de05`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f6ffd2be76e6334bd04318e19b02428d71b315b61ae8bb68ade8b07279ccff`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8e048143304eabc1fad2f149b2761e661ebe261c60e0ecb4cd0f58818ca12090
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6583142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ad730346110f756c4e29df7ebe6e02cb97db3770b8fdda258f5f4def7c2f88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 18:13:27 GMT
ADD file:56e92c06393237a87e0a1ff475e9c9dc80e897d69ec20f45359b587906da345b in / 
# Wed, 31 Mar 2021 18:13:31 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:45:11 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:45:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:45:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:45:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:45:19 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:45:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:07389e51ea05e1c9a3cb0ef92d31181f2afa1e445207ad99ffd8a94d6d6af295`  
		Last Modified: Wed, 31 Mar 2021 18:14:57 GMT  
		Size: 2.4 MB (2424108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7331da30076f2eba452960efaf8df4620f03624062670e29e8e3fb97823756b3`  
		Last Modified: Sat, 03 Apr 2021 01:46:03 GMT  
		Size: 4.2 MB (4158064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd26a9a6149ca00bb0a5e94ae858765a0b787564c99ea0ba4ec23d5cd7a8bd9`  
		Last Modified: Sat, 03 Apr 2021 01:46:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a5a7410fa6228e048f75c6327720948ad9d6dd06db4b594d43165c1f6cab1c`  
		Last Modified: Sat, 03 Apr 2021 01:46:01 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:980841965bacdff61fc62145784092e89a8c0db1f125fccc5e9d240f60f94e93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99075b219d76c9593adb6b735cc906569e0124a6761312332407ee8de31e6382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:47:42 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:47:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:47:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:47:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9228d7a2d7ff547081c5c823de18c8fa62bb6200cee9f820f437c3004e90f309`  
		Last Modified: Sat, 03 Apr 2021 03:48:31 GMT  
		Size: 4.1 MB (4131414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec0c89cac556aea8879a9beeefc7c2f8528b16539e3765c11de3c76e564e6f6`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc29c470aa8216b46da0c00b30283b238b812f9d1395be3920045c367005af`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.13`

```console
$ docker pull nats@sha256:786039ea5743e66f92097f4c98419cdb7755824388806faae9ca893626cda20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:11a99e623a9df5677bdcbcff33bd032975aabdc9c226e00410997607a5398ad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7303859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56ceabe89d18dd0b0c58d97b018484ed43d818791b7a1d9e5e8a09123c6cbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:02:20 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:02:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:02:24 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:02:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab87484469466c6eeb084bcbe5538907a8cca9e02c6c00ffc4e03bd68d4563`  
		Last Modified: Sat, 03 Apr 2021 03:03:06 GMT  
		Size: 4.5 MB (4490943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63537464a64606bc6b408c793c1b726d40b4b1a540a829516859d3405c203e37`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843bbc65e4b41319d487b9ba5eb3a58b709e795448cc632d75fb8f54d76868d9`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:5980c4f84be539fd1b559624db6fa63ee409f825e4a93fa441598e93115d4b15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6784924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f97d97f7e09aa5c9f936e0377789f200b06c8aabe846ce2591ebff76f7db8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:02:19 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:02:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:02:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:02:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:02:26 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:02:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d4b6ba6b297e822b0c0fe254f2d6b5afda81265eaf2481116af687cf66235c`  
		Last Modified: Sat, 03 Apr 2021 01:03:09 GMT  
		Size: 4.2 MB (4161834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0dfcf0132d6f11bd4762e4d1ec0b73f5ee36875a95dc78731673415f9de05`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f6ffd2be76e6334bd04318e19b02428d71b315b61ae8bb68ade8b07279ccff`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:8e048143304eabc1fad2f149b2761e661ebe261c60e0ecb4cd0f58818ca12090
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6583142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ad730346110f756c4e29df7ebe6e02cb97db3770b8fdda258f5f4def7c2f88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 18:13:27 GMT
ADD file:56e92c06393237a87e0a1ff475e9c9dc80e897d69ec20f45359b587906da345b in / 
# Wed, 31 Mar 2021 18:13:31 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:45:11 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:45:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:45:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:45:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:45:19 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:45:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:07389e51ea05e1c9a3cb0ef92d31181f2afa1e445207ad99ffd8a94d6d6af295`  
		Last Modified: Wed, 31 Mar 2021 18:14:57 GMT  
		Size: 2.4 MB (2424108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7331da30076f2eba452960efaf8df4620f03624062670e29e8e3fb97823756b3`  
		Last Modified: Sat, 03 Apr 2021 01:46:03 GMT  
		Size: 4.2 MB (4158064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd26a9a6149ca00bb0a5e94ae858765a0b787564c99ea0ba4ec23d5cd7a8bd9`  
		Last Modified: Sat, 03 Apr 2021 01:46:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a5a7410fa6228e048f75c6327720948ad9d6dd06db4b594d43165c1f6cab1c`  
		Last Modified: Sat, 03 Apr 2021 01:46:01 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:980841965bacdff61fc62145784092e89a8c0db1f125fccc5e9d240f60f94e93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99075b219d76c9593adb6b735cc906569e0124a6761312332407ee8de31e6382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:47:42 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:47:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:47:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:47:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9228d7a2d7ff547081c5c823de18c8fa62bb6200cee9f820f437c3004e90f309`  
		Last Modified: Sat, 03 Apr 2021 03:48:31 GMT  
		Size: 4.1 MB (4131414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec0c89cac556aea8879a9beeefc7c2f8528b16539e3765c11de3c76e564e6f6`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc29c470aa8216b46da0c00b30283b238b812f9d1395be3920045c367005af`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:f116a903fd14977153dc2ae74e3b0437762ee2a6c7858807246d6501b2a9af54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:236c67f0c205b9cfab2809ce1dea44a20258d371c82264afd3172f29c8c70fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
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
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:236c67f0c205b9cfab2809ce1dea44a20258d371c82264afd3172f29c8c70fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
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
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:f116a903fd14977153dc2ae74e3b0437762ee2a6c7858807246d6501b2a9af54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:a6c1153fd919a539581471edd798478057cef10a6347e770d03336a20d5e472b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:9f3868f133ddd1a10ac71bbe835764e9d60e9b00081851a00ca05cd3362ea5d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484142070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be425426bfa101eb4fdc6741eccbeaddde31c6c0761a665b4654dea39a17279`
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
# Wed, 14 Apr 2021 16:02:51 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:02:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:02:53 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:03:32 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:04:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:04:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:04:56 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:04:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:04:58 GMT
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
	-	`sha256:daae5ee02f484d7c054ad550cbee6900a35477f4e23e322cc3af6eb7c4690416`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4df8575d5fc511a7ac278cfc55a4053b36afce4c0bcae2af0af7907c7f91e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570a7e5edba00d92281a4a147639b5fc0b6724693cbfed80007b5b5db612a3e8`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60092b7b0679ad17236eb09b832adcc7bb67a5fd8c2d9a69ffbfc863716274c2`  
		Last Modified: Wed, 14 Apr 2021 16:10:15 GMT  
		Size: 5.1 MB (5072726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5d3b99689d155ccd6cdf6acbc7ef61472c65ce2cee49f441c4c3b844242410`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 9.3 MB (9302175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dae780c7132cf39c97d1602e11b6a58481594df6d896054f3a9e6e9f54e63a`  
		Last Modified: Wed, 14 Apr 2021 16:10:10 GMT  
		Size: 2.0 KB (1957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f2291e14ae4d6e97942f3284122a80c7c969cb9bcfc9a417a833439505f85d`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b07be56d63a82b0606023df13bf32a522a13a12a44c53116ec24d0c1bd2ca1`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6cc0327d5edba60d3e99a97fa6c015e1953c9451bc816f20d6d73a67b9e426`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.4350; amd64

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

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:3002e35b4bb91080eac08408891e6bb9155d38086cbb6fcfb654b61e0d2383e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:9f3868f133ddd1a10ac71bbe835764e9d60e9b00081851a00ca05cd3362ea5d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484142070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be425426bfa101eb4fdc6741eccbeaddde31c6c0761a665b4654dea39a17279`
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
# Wed, 14 Apr 2021 16:02:51 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:02:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:02:53 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:03:32 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:04:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:04:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:04:56 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:04:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:04:58 GMT
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
	-	`sha256:daae5ee02f484d7c054ad550cbee6900a35477f4e23e322cc3af6eb7c4690416`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4df8575d5fc511a7ac278cfc55a4053b36afce4c0bcae2af0af7907c7f91e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570a7e5edba00d92281a4a147639b5fc0b6724693cbfed80007b5b5db612a3e8`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60092b7b0679ad17236eb09b832adcc7bb67a5fd8c2d9a69ffbfc863716274c2`  
		Last Modified: Wed, 14 Apr 2021 16:10:15 GMT  
		Size: 5.1 MB (5072726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5d3b99689d155ccd6cdf6acbc7ef61472c65ce2cee49f441c4c3b844242410`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 9.3 MB (9302175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dae780c7132cf39c97d1602e11b6a58481594df6d896054f3a9e6e9f54e63a`  
		Last Modified: Wed, 14 Apr 2021 16:10:10 GMT  
		Size: 2.0 KB (1957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f2291e14ae4d6e97942f3284122a80c7c969cb9bcfc9a417a833439505f85d`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b07be56d63a82b0606023df13bf32a522a13a12a44c53116ec24d0c1bd2ca1`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6cc0327d5edba60d3e99a97fa6c015e1953c9451bc816f20d6d73a67b9e426`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1424 bytes)  
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
$ docker pull nats@sha256:f0c80abcc8d86c26b77b4cfbf150821d7e71ace88e2ea39d8a5bfa33caf0317a
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
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
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
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-alpine`

```console
$ docker pull nats@sha256:786039ea5743e66f92097f4c98419cdb7755824388806faae9ca893626cda20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:11a99e623a9df5677bdcbcff33bd032975aabdc9c226e00410997607a5398ad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7303859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56ceabe89d18dd0b0c58d97b018484ed43d818791b7a1d9e5e8a09123c6cbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:02:20 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:02:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:02:24 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:02:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab87484469466c6eeb084bcbe5538907a8cca9e02c6c00ffc4e03bd68d4563`  
		Last Modified: Sat, 03 Apr 2021 03:03:06 GMT  
		Size: 4.5 MB (4490943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63537464a64606bc6b408c793c1b726d40b4b1a540a829516859d3405c203e37`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843bbc65e4b41319d487b9ba5eb3a58b709e795448cc632d75fb8f54d76868d9`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:5980c4f84be539fd1b559624db6fa63ee409f825e4a93fa441598e93115d4b15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6784924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f97d97f7e09aa5c9f936e0377789f200b06c8aabe846ce2591ebff76f7db8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:02:19 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:02:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:02:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:02:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:02:26 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:02:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d4b6ba6b297e822b0c0fe254f2d6b5afda81265eaf2481116af687cf66235c`  
		Last Modified: Sat, 03 Apr 2021 01:03:09 GMT  
		Size: 4.2 MB (4161834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0dfcf0132d6f11bd4762e4d1ec0b73f5ee36875a95dc78731673415f9de05`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f6ffd2be76e6334bd04318e19b02428d71b315b61ae8bb68ade8b07279ccff`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8e048143304eabc1fad2f149b2761e661ebe261c60e0ecb4cd0f58818ca12090
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6583142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ad730346110f756c4e29df7ebe6e02cb97db3770b8fdda258f5f4def7c2f88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 18:13:27 GMT
ADD file:56e92c06393237a87e0a1ff475e9c9dc80e897d69ec20f45359b587906da345b in / 
# Wed, 31 Mar 2021 18:13:31 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:45:11 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:45:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:45:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:45:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:45:19 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:45:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:07389e51ea05e1c9a3cb0ef92d31181f2afa1e445207ad99ffd8a94d6d6af295`  
		Last Modified: Wed, 31 Mar 2021 18:14:57 GMT  
		Size: 2.4 MB (2424108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7331da30076f2eba452960efaf8df4620f03624062670e29e8e3fb97823756b3`  
		Last Modified: Sat, 03 Apr 2021 01:46:03 GMT  
		Size: 4.2 MB (4158064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd26a9a6149ca00bb0a5e94ae858765a0b787564c99ea0ba4ec23d5cd7a8bd9`  
		Last Modified: Sat, 03 Apr 2021 01:46:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a5a7410fa6228e048f75c6327720948ad9d6dd06db4b594d43165c1f6cab1c`  
		Last Modified: Sat, 03 Apr 2021 01:46:01 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:980841965bacdff61fc62145784092e89a8c0db1f125fccc5e9d240f60f94e93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99075b219d76c9593adb6b735cc906569e0124a6761312332407ee8de31e6382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:47:42 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:47:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:47:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:47:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9228d7a2d7ff547081c5c823de18c8fa62bb6200cee9f820f437c3004e90f309`  
		Last Modified: Sat, 03 Apr 2021 03:48:31 GMT  
		Size: 4.1 MB (4131414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec0c89cac556aea8879a9beeefc7c2f8528b16539e3765c11de3c76e564e6f6`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc29c470aa8216b46da0c00b30283b238b812f9d1395be3920045c367005af`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-alpine3.13`

```console
$ docker pull nats@sha256:786039ea5743e66f92097f4c98419cdb7755824388806faae9ca893626cda20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2-alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:11a99e623a9df5677bdcbcff33bd032975aabdc9c226e00410997607a5398ad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7303859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56ceabe89d18dd0b0c58d97b018484ed43d818791b7a1d9e5e8a09123c6cbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:02:20 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:02:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:02:24 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:02:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab87484469466c6eeb084bcbe5538907a8cca9e02c6c00ffc4e03bd68d4563`  
		Last Modified: Sat, 03 Apr 2021 03:03:06 GMT  
		Size: 4.5 MB (4490943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63537464a64606bc6b408c793c1b726d40b4b1a540a829516859d3405c203e37`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843bbc65e4b41319d487b9ba5eb3a58b709e795448cc632d75fb8f54d76868d9`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:5980c4f84be539fd1b559624db6fa63ee409f825e4a93fa441598e93115d4b15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6784924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f97d97f7e09aa5c9f936e0377789f200b06c8aabe846ce2591ebff76f7db8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:02:19 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:02:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:02:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:02:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:02:26 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:02:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d4b6ba6b297e822b0c0fe254f2d6b5afda81265eaf2481116af687cf66235c`  
		Last Modified: Sat, 03 Apr 2021 01:03:09 GMT  
		Size: 4.2 MB (4161834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0dfcf0132d6f11bd4762e4d1ec0b73f5ee36875a95dc78731673415f9de05`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f6ffd2be76e6334bd04318e19b02428d71b315b61ae8bb68ade8b07279ccff`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:8e048143304eabc1fad2f149b2761e661ebe261c60e0ecb4cd0f58818ca12090
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6583142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ad730346110f756c4e29df7ebe6e02cb97db3770b8fdda258f5f4def7c2f88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 18:13:27 GMT
ADD file:56e92c06393237a87e0a1ff475e9c9dc80e897d69ec20f45359b587906da345b in / 
# Wed, 31 Mar 2021 18:13:31 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:45:11 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:45:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:45:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:45:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:45:19 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:45:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:07389e51ea05e1c9a3cb0ef92d31181f2afa1e445207ad99ffd8a94d6d6af295`  
		Last Modified: Wed, 31 Mar 2021 18:14:57 GMT  
		Size: 2.4 MB (2424108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7331da30076f2eba452960efaf8df4620f03624062670e29e8e3fb97823756b3`  
		Last Modified: Sat, 03 Apr 2021 01:46:03 GMT  
		Size: 4.2 MB (4158064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd26a9a6149ca00bb0a5e94ae858765a0b787564c99ea0ba4ec23d5cd7a8bd9`  
		Last Modified: Sat, 03 Apr 2021 01:46:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a5a7410fa6228e048f75c6327720948ad9d6dd06db4b594d43165c1f6cab1c`  
		Last Modified: Sat, 03 Apr 2021 01:46:01 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:980841965bacdff61fc62145784092e89a8c0db1f125fccc5e9d240f60f94e93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99075b219d76c9593adb6b735cc906569e0124a6761312332407ee8de31e6382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:47:42 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:47:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:47:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:47:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9228d7a2d7ff547081c5c823de18c8fa62bb6200cee9f820f437c3004e90f309`  
		Last Modified: Sat, 03 Apr 2021 03:48:31 GMT  
		Size: 4.1 MB (4131414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec0c89cac556aea8879a9beeefc7c2f8528b16539e3765c11de3c76e564e6f6`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc29c470aa8216b46da0c00b30283b238b812f9d1395be3920045c367005af`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-linux`

```console
$ docker pull nats@sha256:f116a903fd14977153dc2ae74e3b0437762ee2a6c7858807246d6501b2a9af54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2-linux` - linux; amd64

```console
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-nanoserver`

```console
$ docker pull nats@sha256:236c67f0c205b9cfab2809ce1dea44a20258d371c82264afd3172f29c8c70fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2-nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
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
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-nanoserver-1809`

```console
$ docker pull nats@sha256:236c67f0c205b9cfab2809ce1dea44a20258d371c82264afd3172f29c8c70fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
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
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-scratch`

```console
$ docker pull nats@sha256:f116a903fd14977153dc2ae74e3b0437762ee2a6c7858807246d6501b2a9af54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2-windowsservercore`

```console
$ docker pull nats@sha256:a6c1153fd919a539581471edd798478057cef10a6347e770d03336a20d5e472b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats:2.2-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:9f3868f133ddd1a10ac71bbe835764e9d60e9b00081851a00ca05cd3362ea5d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484142070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be425426bfa101eb4fdc6741eccbeaddde31c6c0761a665b4654dea39a17279`
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
# Wed, 14 Apr 2021 16:02:51 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:02:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:02:53 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:03:32 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:04:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:04:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:04:56 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:04:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:04:58 GMT
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
	-	`sha256:daae5ee02f484d7c054ad550cbee6900a35477f4e23e322cc3af6eb7c4690416`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4df8575d5fc511a7ac278cfc55a4053b36afce4c0bcae2af0af7907c7f91e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570a7e5edba00d92281a4a147639b5fc0b6724693cbfed80007b5b5db612a3e8`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60092b7b0679ad17236eb09b832adcc7bb67a5fd8c2d9a69ffbfc863716274c2`  
		Last Modified: Wed, 14 Apr 2021 16:10:15 GMT  
		Size: 5.1 MB (5072726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5d3b99689d155ccd6cdf6acbc7ef61472c65ce2cee49f441c4c3b844242410`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 9.3 MB (9302175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dae780c7132cf39c97d1602e11b6a58481594df6d896054f3a9e6e9f54e63a`  
		Last Modified: Wed, 14 Apr 2021 16:10:10 GMT  
		Size: 2.0 KB (1957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f2291e14ae4d6e97942f3284122a80c7c969cb9bcfc9a417a833439505f85d`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b07be56d63a82b0606023df13bf32a522a13a12a44c53116ec24d0c1bd2ca1`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6cc0327d5edba60d3e99a97fa6c015e1953c9451bc816f20d6d73a67b9e426`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2-windowsservercore` - windows version 10.0.14393.4350; amd64

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

## `nats:2.2-windowsservercore-1809`

```console
$ docker pull nats@sha256:3002e35b4bb91080eac08408891e6bb9155d38086cbb6fcfb654b61e0d2383e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:9f3868f133ddd1a10ac71bbe835764e9d60e9b00081851a00ca05cd3362ea5d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484142070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be425426bfa101eb4fdc6741eccbeaddde31c6c0761a665b4654dea39a17279`
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
# Wed, 14 Apr 2021 16:02:51 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:02:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:02:53 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:03:32 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:04:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:04:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:04:56 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:04:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:04:58 GMT
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
	-	`sha256:daae5ee02f484d7c054ad550cbee6900a35477f4e23e322cc3af6eb7c4690416`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4df8575d5fc511a7ac278cfc55a4053b36afce4c0bcae2af0af7907c7f91e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570a7e5edba00d92281a4a147639b5fc0b6724693cbfed80007b5b5db612a3e8`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60092b7b0679ad17236eb09b832adcc7bb67a5fd8c2d9a69ffbfc863716274c2`  
		Last Modified: Wed, 14 Apr 2021 16:10:15 GMT  
		Size: 5.1 MB (5072726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5d3b99689d155ccd6cdf6acbc7ef61472c65ce2cee49f441c4c3b844242410`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 9.3 MB (9302175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dae780c7132cf39c97d1602e11b6a58481594df6d896054f3a9e6e9f54e63a`  
		Last Modified: Wed, 14 Apr 2021 16:10:10 GMT  
		Size: 2.0 KB (1957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f2291e14ae4d6e97942f3284122a80c7c969cb9bcfc9a417a833439505f85d`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b07be56d63a82b0606023df13bf32a522a13a12a44c53116ec24d0c1bd2ca1`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6cc0327d5edba60d3e99a97fa6c015e1953c9451bc816f20d6d73a67b9e426`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1424 bytes)  
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

## `nats:2.2.1`

```console
$ docker pull nats@sha256:f0c80abcc8d86c26b77b4cfbf150821d7e71ace88e2ea39d8a5bfa33caf0317a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2.1` - linux; amd64

```console
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
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
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.1-alpine`

```console
$ docker pull nats@sha256:786039ea5743e66f92097f4c98419cdb7755824388806faae9ca893626cda20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2.1-alpine` - linux; amd64

```console
$ docker pull nats@sha256:11a99e623a9df5677bdcbcff33bd032975aabdc9c226e00410997607a5398ad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7303859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56ceabe89d18dd0b0c58d97b018484ed43d818791b7a1d9e5e8a09123c6cbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:02:20 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:02:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:02:24 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:02:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab87484469466c6eeb084bcbe5538907a8cca9e02c6c00ffc4e03bd68d4563`  
		Last Modified: Sat, 03 Apr 2021 03:03:06 GMT  
		Size: 4.5 MB (4490943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63537464a64606bc6b408c793c1b726d40b4b1a540a829516859d3405c203e37`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843bbc65e4b41319d487b9ba5eb3a58b709e795448cc632d75fb8f54d76868d9`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:5980c4f84be539fd1b559624db6fa63ee409f825e4a93fa441598e93115d4b15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6784924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f97d97f7e09aa5c9f936e0377789f200b06c8aabe846ce2591ebff76f7db8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:02:19 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:02:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:02:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:02:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:02:26 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:02:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d4b6ba6b297e822b0c0fe254f2d6b5afda81265eaf2481116af687cf66235c`  
		Last Modified: Sat, 03 Apr 2021 01:03:09 GMT  
		Size: 4.2 MB (4161834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0dfcf0132d6f11bd4762e4d1ec0b73f5ee36875a95dc78731673415f9de05`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f6ffd2be76e6334bd04318e19b02428d71b315b61ae8bb68ade8b07279ccff`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8e048143304eabc1fad2f149b2761e661ebe261c60e0ecb4cd0f58818ca12090
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6583142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ad730346110f756c4e29df7ebe6e02cb97db3770b8fdda258f5f4def7c2f88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 18:13:27 GMT
ADD file:56e92c06393237a87e0a1ff475e9c9dc80e897d69ec20f45359b587906da345b in / 
# Wed, 31 Mar 2021 18:13:31 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:45:11 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:45:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:45:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:45:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:45:19 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:45:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:07389e51ea05e1c9a3cb0ef92d31181f2afa1e445207ad99ffd8a94d6d6af295`  
		Last Modified: Wed, 31 Mar 2021 18:14:57 GMT  
		Size: 2.4 MB (2424108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7331da30076f2eba452960efaf8df4620f03624062670e29e8e3fb97823756b3`  
		Last Modified: Sat, 03 Apr 2021 01:46:03 GMT  
		Size: 4.2 MB (4158064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd26a9a6149ca00bb0a5e94ae858765a0b787564c99ea0ba4ec23d5cd7a8bd9`  
		Last Modified: Sat, 03 Apr 2021 01:46:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a5a7410fa6228e048f75c6327720948ad9d6dd06db4b594d43165c1f6cab1c`  
		Last Modified: Sat, 03 Apr 2021 01:46:01 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:980841965bacdff61fc62145784092e89a8c0db1f125fccc5e9d240f60f94e93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99075b219d76c9593adb6b735cc906569e0124a6761312332407ee8de31e6382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:47:42 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:47:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:47:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:47:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9228d7a2d7ff547081c5c823de18c8fa62bb6200cee9f820f437c3004e90f309`  
		Last Modified: Sat, 03 Apr 2021 03:48:31 GMT  
		Size: 4.1 MB (4131414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec0c89cac556aea8879a9beeefc7c2f8528b16539e3765c11de3c76e564e6f6`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc29c470aa8216b46da0c00b30283b238b812f9d1395be3920045c367005af`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.1-alpine3.13`

```console
$ docker pull nats@sha256:786039ea5743e66f92097f4c98419cdb7755824388806faae9ca893626cda20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2.1-alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:11a99e623a9df5677bdcbcff33bd032975aabdc9c226e00410997607a5398ad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7303859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56ceabe89d18dd0b0c58d97b018484ed43d818791b7a1d9e5e8a09123c6cbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:02:20 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:02:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:02:24 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:02:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab87484469466c6eeb084bcbe5538907a8cca9e02c6c00ffc4e03bd68d4563`  
		Last Modified: Sat, 03 Apr 2021 03:03:06 GMT  
		Size: 4.5 MB (4490943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63537464a64606bc6b408c793c1b726d40b4b1a540a829516859d3405c203e37`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843bbc65e4b41319d487b9ba5eb3a58b709e795448cc632d75fb8f54d76868d9`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:5980c4f84be539fd1b559624db6fa63ee409f825e4a93fa441598e93115d4b15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6784924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f97d97f7e09aa5c9f936e0377789f200b06c8aabe846ce2591ebff76f7db8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:02:19 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:02:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:02:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:02:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:02:26 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:02:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d4b6ba6b297e822b0c0fe254f2d6b5afda81265eaf2481116af687cf66235c`  
		Last Modified: Sat, 03 Apr 2021 01:03:09 GMT  
		Size: 4.2 MB (4161834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0dfcf0132d6f11bd4762e4d1ec0b73f5ee36875a95dc78731673415f9de05`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f6ffd2be76e6334bd04318e19b02428d71b315b61ae8bb68ade8b07279ccff`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:8e048143304eabc1fad2f149b2761e661ebe261c60e0ecb4cd0f58818ca12090
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6583142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ad730346110f756c4e29df7ebe6e02cb97db3770b8fdda258f5f4def7c2f88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 18:13:27 GMT
ADD file:56e92c06393237a87e0a1ff475e9c9dc80e897d69ec20f45359b587906da345b in / 
# Wed, 31 Mar 2021 18:13:31 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:45:11 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:45:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:45:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:45:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:45:19 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:45:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:07389e51ea05e1c9a3cb0ef92d31181f2afa1e445207ad99ffd8a94d6d6af295`  
		Last Modified: Wed, 31 Mar 2021 18:14:57 GMT  
		Size: 2.4 MB (2424108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7331da30076f2eba452960efaf8df4620f03624062670e29e8e3fb97823756b3`  
		Last Modified: Sat, 03 Apr 2021 01:46:03 GMT  
		Size: 4.2 MB (4158064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd26a9a6149ca00bb0a5e94ae858765a0b787564c99ea0ba4ec23d5cd7a8bd9`  
		Last Modified: Sat, 03 Apr 2021 01:46:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a5a7410fa6228e048f75c6327720948ad9d6dd06db4b594d43165c1f6cab1c`  
		Last Modified: Sat, 03 Apr 2021 01:46:01 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:980841965bacdff61fc62145784092e89a8c0db1f125fccc5e9d240f60f94e93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99075b219d76c9593adb6b735cc906569e0124a6761312332407ee8de31e6382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:47:42 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:47:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:47:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:47:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9228d7a2d7ff547081c5c823de18c8fa62bb6200cee9f820f437c3004e90f309`  
		Last Modified: Sat, 03 Apr 2021 03:48:31 GMT  
		Size: 4.1 MB (4131414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec0c89cac556aea8879a9beeefc7c2f8528b16539e3765c11de3c76e564e6f6`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc29c470aa8216b46da0c00b30283b238b812f9d1395be3920045c367005af`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.1-linux`

```console
$ docker pull nats@sha256:f116a903fd14977153dc2ae74e3b0437762ee2a6c7858807246d6501b2a9af54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2.1-linux` - linux; amd64

```console
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.1-nanoserver`

```console
$ docker pull nats@sha256:236c67f0c205b9cfab2809ce1dea44a20258d371c82264afd3172f29c8c70fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2.1-nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
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
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.1-nanoserver-1809`

```console
$ docker pull nats@sha256:236c67f0c205b9cfab2809ce1dea44a20258d371c82264afd3172f29c8c70fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2.1-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
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
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.1-scratch`

```console
$ docker pull nats@sha256:f116a903fd14977153dc2ae74e3b0437762ee2a6c7858807246d6501b2a9af54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.2.1-scratch` - linux; amd64

```console
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.1-windowsservercore`

```console
$ docker pull nats@sha256:a6c1153fd919a539581471edd798478057cef10a6347e770d03336a20d5e472b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats:2.2.1-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:9f3868f133ddd1a10ac71bbe835764e9d60e9b00081851a00ca05cd3362ea5d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484142070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be425426bfa101eb4fdc6741eccbeaddde31c6c0761a665b4654dea39a17279`
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
# Wed, 14 Apr 2021 16:02:51 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:02:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:02:53 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:03:32 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:04:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:04:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:04:56 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:04:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:04:58 GMT
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
	-	`sha256:daae5ee02f484d7c054ad550cbee6900a35477f4e23e322cc3af6eb7c4690416`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4df8575d5fc511a7ac278cfc55a4053b36afce4c0bcae2af0af7907c7f91e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570a7e5edba00d92281a4a147639b5fc0b6724693cbfed80007b5b5db612a3e8`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60092b7b0679ad17236eb09b832adcc7bb67a5fd8c2d9a69ffbfc863716274c2`  
		Last Modified: Wed, 14 Apr 2021 16:10:15 GMT  
		Size: 5.1 MB (5072726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5d3b99689d155ccd6cdf6acbc7ef61472c65ce2cee49f441c4c3b844242410`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 9.3 MB (9302175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dae780c7132cf39c97d1602e11b6a58481594df6d896054f3a9e6e9f54e63a`  
		Last Modified: Wed, 14 Apr 2021 16:10:10 GMT  
		Size: 2.0 KB (1957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f2291e14ae4d6e97942f3284122a80c7c969cb9bcfc9a417a833439505f85d`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b07be56d63a82b0606023df13bf32a522a13a12a44c53116ec24d0c1bd2ca1`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6cc0327d5edba60d3e99a97fa6c015e1953c9451bc816f20d6d73a67b9e426`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.2.1-windowsservercore` - windows version 10.0.14393.4350; amd64

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

## `nats:2.2.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:3002e35b4bb91080eac08408891e6bb9155d38086cbb6fcfb654b61e0d2383e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:2.2.1-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:9f3868f133ddd1a10ac71bbe835764e9d60e9b00081851a00ca05cd3362ea5d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484142070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be425426bfa101eb4fdc6741eccbeaddde31c6c0761a665b4654dea39a17279`
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
# Wed, 14 Apr 2021 16:02:51 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:02:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:02:53 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:03:32 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:04:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:04:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:04:56 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:04:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:04:58 GMT
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
	-	`sha256:daae5ee02f484d7c054ad550cbee6900a35477f4e23e322cc3af6eb7c4690416`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4df8575d5fc511a7ac278cfc55a4053b36afce4c0bcae2af0af7907c7f91e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570a7e5edba00d92281a4a147639b5fc0b6724693cbfed80007b5b5db612a3e8`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60092b7b0679ad17236eb09b832adcc7bb67a5fd8c2d9a69ffbfc863716274c2`  
		Last Modified: Wed, 14 Apr 2021 16:10:15 GMT  
		Size: 5.1 MB (5072726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5d3b99689d155ccd6cdf6acbc7ef61472c65ce2cee49f441c4c3b844242410`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 9.3 MB (9302175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dae780c7132cf39c97d1602e11b6a58481594df6d896054f3a9e6e9f54e63a`  
		Last Modified: Wed, 14 Apr 2021 16:10:10 GMT  
		Size: 2.0 KB (1957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f2291e14ae4d6e97942f3284122a80c7c969cb9bcfc9a417a833439505f85d`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b07be56d63a82b0606023df13bf32a522a13a12a44c53116ec24d0c1bd2ca1`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6cc0327d5edba60d3e99a97fa6c015e1953c9451bc816f20d6d73a67b9e426`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.2.1-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:486439b61d7c8307b15b01bae5f574784e333ee642d1d3285e3bf61785ea00cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `nats:2.2.1-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

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

## `nats:alpine`

```console
$ docker pull nats@sha256:786039ea5743e66f92097f4c98419cdb7755824388806faae9ca893626cda20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:11a99e623a9df5677bdcbcff33bd032975aabdc9c226e00410997607a5398ad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7303859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56ceabe89d18dd0b0c58d97b018484ed43d818791b7a1d9e5e8a09123c6cbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:02:20 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:02:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:02:24 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:02:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab87484469466c6eeb084bcbe5538907a8cca9e02c6c00ffc4e03bd68d4563`  
		Last Modified: Sat, 03 Apr 2021 03:03:06 GMT  
		Size: 4.5 MB (4490943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63537464a64606bc6b408c793c1b726d40b4b1a540a829516859d3405c203e37`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843bbc65e4b41319d487b9ba5eb3a58b709e795448cc632d75fb8f54d76868d9`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:5980c4f84be539fd1b559624db6fa63ee409f825e4a93fa441598e93115d4b15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6784924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f97d97f7e09aa5c9f936e0377789f200b06c8aabe846ce2591ebff76f7db8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:02:19 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:02:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:02:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:02:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:02:26 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:02:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d4b6ba6b297e822b0c0fe254f2d6b5afda81265eaf2481116af687cf66235c`  
		Last Modified: Sat, 03 Apr 2021 01:03:09 GMT  
		Size: 4.2 MB (4161834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0dfcf0132d6f11bd4762e4d1ec0b73f5ee36875a95dc78731673415f9de05`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f6ffd2be76e6334bd04318e19b02428d71b315b61ae8bb68ade8b07279ccff`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8e048143304eabc1fad2f149b2761e661ebe261c60e0ecb4cd0f58818ca12090
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6583142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ad730346110f756c4e29df7ebe6e02cb97db3770b8fdda258f5f4def7c2f88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 18:13:27 GMT
ADD file:56e92c06393237a87e0a1ff475e9c9dc80e897d69ec20f45359b587906da345b in / 
# Wed, 31 Mar 2021 18:13:31 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:45:11 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:45:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:45:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:45:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:45:19 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:45:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:07389e51ea05e1c9a3cb0ef92d31181f2afa1e445207ad99ffd8a94d6d6af295`  
		Last Modified: Wed, 31 Mar 2021 18:14:57 GMT  
		Size: 2.4 MB (2424108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7331da30076f2eba452960efaf8df4620f03624062670e29e8e3fb97823756b3`  
		Last Modified: Sat, 03 Apr 2021 01:46:03 GMT  
		Size: 4.2 MB (4158064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd26a9a6149ca00bb0a5e94ae858765a0b787564c99ea0ba4ec23d5cd7a8bd9`  
		Last Modified: Sat, 03 Apr 2021 01:46:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a5a7410fa6228e048f75c6327720948ad9d6dd06db4b594d43165c1f6cab1c`  
		Last Modified: Sat, 03 Apr 2021 01:46:01 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:980841965bacdff61fc62145784092e89a8c0db1f125fccc5e9d240f60f94e93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99075b219d76c9593adb6b735cc906569e0124a6761312332407ee8de31e6382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:47:42 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:47:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:47:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:47:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9228d7a2d7ff547081c5c823de18c8fa62bb6200cee9f820f437c3004e90f309`  
		Last Modified: Sat, 03 Apr 2021 03:48:31 GMT  
		Size: 4.1 MB (4131414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec0c89cac556aea8879a9beeefc7c2f8528b16539e3765c11de3c76e564e6f6`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc29c470aa8216b46da0c00b30283b238b812f9d1395be3920045c367005af`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.13`

```console
$ docker pull nats@sha256:786039ea5743e66f92097f4c98419cdb7755824388806faae9ca893626cda20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:11a99e623a9df5677bdcbcff33bd032975aabdc9c226e00410997607a5398ad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7303859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56ceabe89d18dd0b0c58d97b018484ed43d818791b7a1d9e5e8a09123c6cbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:02:20 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:02:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:02:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:02:24 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:02:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab87484469466c6eeb084bcbe5538907a8cca9e02c6c00ffc4e03bd68d4563`  
		Last Modified: Sat, 03 Apr 2021 03:03:06 GMT  
		Size: 4.5 MB (4490943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63537464a64606bc6b408c793c1b726d40b4b1a540a829516859d3405c203e37`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843bbc65e4b41319d487b9ba5eb3a58b709e795448cc632d75fb8f54d76868d9`  
		Last Modified: Sat, 03 Apr 2021 03:03:05 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:5980c4f84be539fd1b559624db6fa63ee409f825e4a93fa441598e93115d4b15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6784924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f97d97f7e09aa5c9f936e0377789f200b06c8aabe846ce2591ebff76f7db8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:18:49 GMT
ADD file:988879d74f643b89539e5a0b6d74221621f19f4f87f722614addadc46ce47200 in / 
# Wed, 31 Mar 2021 17:18:50 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:02:19 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:02:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:02:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:02:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:02:26 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:02:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bb87125c6ee1ce30c6b33d2c96a9fbe46da4a290f7cb1dd73fd62d4e06503699`  
		Last Modified: Wed, 31 Mar 2021 17:19:55 GMT  
		Size: 2.6 MB (2622116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d4b6ba6b297e822b0c0fe254f2d6b5afda81265eaf2481116af687cf66235c`  
		Last Modified: Sat, 03 Apr 2021 01:03:09 GMT  
		Size: 4.2 MB (4161834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0dfcf0132d6f11bd4762e4d1ec0b73f5ee36875a95dc78731673415f9de05`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f6ffd2be76e6334bd04318e19b02428d71b315b61ae8bb68ade8b07279ccff`  
		Last Modified: Sat, 03 Apr 2021 01:03:07 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:8e048143304eabc1fad2f149b2761e661ebe261c60e0ecb4cd0f58818ca12090
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6583142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ad730346110f756c4e29df7ebe6e02cb97db3770b8fdda258f5f4def7c2f88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 18:13:27 GMT
ADD file:56e92c06393237a87e0a1ff475e9c9dc80e897d69ec20f45359b587906da345b in / 
# Wed, 31 Mar 2021 18:13:31 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 01:45:11 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 01:45:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 01:45:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 01:45:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 01:45:19 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 01:45:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:07389e51ea05e1c9a3cb0ef92d31181f2afa1e445207ad99ffd8a94d6d6af295`  
		Last Modified: Wed, 31 Mar 2021 18:14:57 GMT  
		Size: 2.4 MB (2424108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7331da30076f2eba452960efaf8df4620f03624062670e29e8e3fb97823756b3`  
		Last Modified: Sat, 03 Apr 2021 01:46:03 GMT  
		Size: 4.2 MB (4158064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd26a9a6149ca00bb0a5e94ae858765a0b787564c99ea0ba4ec23d5cd7a8bd9`  
		Last Modified: Sat, 03 Apr 2021 01:46:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a5a7410fa6228e048f75c6327720948ad9d6dd06db4b594d43165c1f6cab1c`  
		Last Modified: Sat, 03 Apr 2021 01:46:01 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:980841965bacdff61fc62145784092e89a8c0db1f125fccc5e9d240f60f94e93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6844304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99075b219d76c9593adb6b735cc906569e0124a6761312332407ee8de31e6382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Sat, 03 Apr 2021 03:47:42 GMT
ENV NATS_SERVER=2.2.1
# Sat, 03 Apr 2021 03:47:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0123d924907282265190258662edf8ad4351055083b5040e3bdf59117bd1c51c' ;; 		armhf) natsArch='arm6'; sha256='da719b07fd57137f85bfa6cffc7d00841a9c1fb4cdf7ca9a537bfc3f99b71f36' ;; 		armv7) natsArch='arm7'; sha256='cf6e8d9a9cc5d05f7320fb4be8fc9239cb87b91c6600a61ce7a2fb63e2f29f5a' ;; 		x86_64) natsArch='amd64'; sha256='70cb40d78b82ea6c0ca926c31ef98d2e1c885cfe2f73f34883e4ca448366c2dd' ;; 		x86) natsArch='386'; sha256='da54d129f8a52c048ded61e3b62e946037a9464d02cf818e568bbf1e385ce6be' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 03 Apr 2021 03:47:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 03 Apr 2021 03:47:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Apr 2021 03:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Apr 2021 03:47:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9228d7a2d7ff547081c5c823de18c8fa62bb6200cee9f820f437c3004e90f309`  
		Last Modified: Sat, 03 Apr 2021 03:48:31 GMT  
		Size: 4.1 MB (4131414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec0c89cac556aea8879a9beeefc7c2f8528b16539e3765c11de3c76e564e6f6`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc29c470aa8216b46da0c00b30283b238b812f9d1395be3920045c367005af`  
		Last Modified: Sat, 03 Apr 2021 03:48:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:f0c80abcc8d86c26b77b4cfbf150821d7e71ace88e2ea39d8a5bfa33caf0317a
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
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
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
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:f116a903fd14977153dc2ae74e3b0437762ee2a6c7858807246d6501b2a9af54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:236c67f0c205b9cfab2809ce1dea44a20258d371c82264afd3172f29c8c70fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
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
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:236c67f0c205b9cfab2809ce1dea44a20258d371c82264afd3172f29c8c70fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:545e15088a9a48d35878789abdde98cb7a98627e5a7c3be56f42abb2e13632e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105608630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac61d30cc1900a1011f83ffa5dbcfd15a0a1754f790b94bdded5ed0cd4b673`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Apr 2021 16:05:20 GMT
RUN cmd /S /C #(nop) COPY file:428a7e80db4313301a46326a9a79832e9cbe7d78c94e749b5c295e813e484f21 in C:\nats-server.exe 
# Wed, 14 Apr 2021 16:05:21 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:05:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:05:23 GMT
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
	-	`sha256:d6f599ec3e67dbcacd5ebae06ae984f5a688eba397e2280187ee399da88dc6ad`  
		Last Modified: Wed, 14 Apr 2021 16:10:38 GMT  
		Size: 4.3 MB (4262107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780b42108cdc95774ec8d8239a9027e7382a875cf25306df1b01363dd2dc7aa4`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b002edb80987b79bb224f75e7c65e924d45dc54e548ce835539ca82dcdcc08e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b88ce7ff0e645ebee08b98beb32730028b41f85296f22b03154fa54614ac`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dc978ed7937ca238d82c78779b6e3a605e64ba31e2a5adac73bc7da1f63ede`  
		Last Modified: Wed, 14 Apr 2021 16:10:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:f116a903fd14977153dc2ae74e3b0437762ee2a6c7858807246d6501b2a9af54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:3bd24b6508d68c6d8835ecf42066a66f01b9e58d55c7a82d99eb3f1d9041fe15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68fc0ca6306424854628406a234c7c5f76f2a13d658233ecefdb59a3de4ec89`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:02:40 GMT
COPY file:494bfb1615387aa8aa24059641c501c246cffbb47653109c93d498a68ccce32a in /nats-server 
# Sat, 03 Apr 2021 03:02:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:02:41 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:02:41 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:02:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:832634cbfed021f934fff287987e6acb75f23228af46328d3f79d812b6462c57`  
		Last Modified: Sat, 03 Apr 2021 03:03:31 GMT  
		Size: 4.2 MB (4208232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f381d2349aa770a85b4fde9e5c7794fe38c878aea8784f679b3f09728534a4`  
		Last Modified: Sat, 03 Apr 2021 03:03:30 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:0c1db0c5e32501c283742665116d2ae34168be99f1f0298a17fe6a1a0c3c9cb1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3882437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadccf67b2f681485255da8d75647104535e861fb3ee82f610f6d42281a07300`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:02:37 GMT
COPY file:54bee7857c6b5cc9e3287e28fd1ffbbd529d72e791a1746d90d0b66346698246 in /nats-server 
# Sat, 03 Apr 2021 01:02:38 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:02:38 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:02:39 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:02:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:91cca6fbde65445d7c75ad5de8204fd8356fa76f2dd2983a53b2c0d9b7255bd9`  
		Last Modified: Sat, 03 Apr 2021 01:03:23 GMT  
		Size: 3.9 MB (3881961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8d6f093021c26c95a4df34d728495a189d358902c6fed301d6bc06e93f4e85`  
		Last Modified: Sat, 03 Apr 2021 01:03:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:61dade57dcce93e1f3ea3e01779c4d2f1bf4ff21415290e42dfe72cba333f7d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3877449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad61fe367441505f4bdd49177124c6f6fbb5d9e212c6b871aec402ea6c4122`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 01:45:33 GMT
COPY file:d95e297af0c7798d74c045b7143a48199a8e32ca5c5aa0b8d7c967a602bc1cfe in /nats-server 
# Sat, 03 Apr 2021 01:45:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 01:45:35 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 01:45:36 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 01:45:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7919165d0b190df92f81ef4af9a0a2fef8a2da95dac86e567498a9364b0be069`  
		Last Modified: Sat, 03 Apr 2021 01:46:21 GMT  
		Size: 3.9 MB (3876974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfa2b4e61cc1a65501d2feea740d0f932e2bf901c202226b24a7d787c0f4dff`  
		Last Modified: Sat, 03 Apr 2021 01:46:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:13c34571ac946007679eb9333b30ca2fc5225ea3afdeb3ec3082bf4e5befe284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8fa2c7d5a8fb8a3e96f92707cd39a3107455acd96b42415d60cf31cae334d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 03 Apr 2021 03:48:01 GMT
COPY file:4d714e3c520aa8a1f5935c65806500f01ea25ace84372fd7f3aa0a06f1f626c9 in /nats-server 
# Sat, 03 Apr 2021 03:48:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 03 Apr 2021 03:48:03 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Apr 2021 03:48:04 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Apr 2021 03:48:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:310f293639061b27b8965c8683cf2bffb7d9b58bdb924635525fa7d990f2f3fb`  
		Last Modified: Sat, 03 Apr 2021 03:48:48 GMT  
		Size: 3.9 MB (3850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e64370dd792941a18253408636a97ab34ef2f6ea706da1fe18ae7e008a3b13e`  
		Last Modified: Sat, 03 Apr 2021 03:48:47 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:a6c1153fd919a539581471edd798478057cef10a6347e770d03336a20d5e472b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `nats:windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:9f3868f133ddd1a10ac71bbe835764e9d60e9b00081851a00ca05cd3362ea5d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484142070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be425426bfa101eb4fdc6741eccbeaddde31c6c0761a665b4654dea39a17279`
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
# Wed, 14 Apr 2021 16:02:51 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:02:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:02:53 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:03:32 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:04:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:04:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:04:56 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:04:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:04:58 GMT
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
	-	`sha256:daae5ee02f484d7c054ad550cbee6900a35477f4e23e322cc3af6eb7c4690416`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4df8575d5fc511a7ac278cfc55a4053b36afce4c0bcae2af0af7907c7f91e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570a7e5edba00d92281a4a147639b5fc0b6724693cbfed80007b5b5db612a3e8`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60092b7b0679ad17236eb09b832adcc7bb67a5fd8c2d9a69ffbfc863716274c2`  
		Last Modified: Wed, 14 Apr 2021 16:10:15 GMT  
		Size: 5.1 MB (5072726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5d3b99689d155ccd6cdf6acbc7ef61472c65ce2cee49f441c4c3b844242410`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 9.3 MB (9302175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dae780c7132cf39c97d1602e11b6a58481594df6d896054f3a9e6e9f54e63a`  
		Last Modified: Wed, 14 Apr 2021 16:10:10 GMT  
		Size: 2.0 KB (1957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f2291e14ae4d6e97942f3284122a80c7c969cb9bcfc9a417a833439505f85d`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b07be56d63a82b0606023df13bf32a522a13a12a44c53116ec24d0c1bd2ca1`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6cc0327d5edba60d3e99a97fa6c015e1953c9451bc816f20d6d73a67b9e426`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4350; amd64

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

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:3002e35b4bb91080eac08408891e6bb9155d38086cbb6fcfb654b61e0d2383e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:9f3868f133ddd1a10ac71bbe835764e9d60e9b00081851a00ca05cd3362ea5d1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2484142070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be425426bfa101eb4fdc6741eccbeaddde31c6c0761a665b4654dea39a17279`
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
# Wed, 14 Apr 2021 16:02:51 GMT
ENV NATS_SERVER=2.2.1
# Wed, 14 Apr 2021 16:02:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.2.1/nats-server-v2.2.1-windows-amd64.zip
# Wed, 14 Apr 2021 16:02:53 GMT
ENV GIT_DOWNLOAD_SHA256=1f0d48a7ba9200e2572016a9f3e1ec7e630f0518cc0b40950c14ff3a5d900924
# Wed, 14 Apr 2021 16:03:32 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Apr 2021 16:04:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Apr 2021 16:04:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Apr 2021 16:04:56 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Apr 2021 16:04:57 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Apr 2021 16:04:58 GMT
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
	-	`sha256:daae5ee02f484d7c054ad550cbee6900a35477f4e23e322cc3af6eb7c4690416`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4df8575d5fc511a7ac278cfc55a4053b36afce4c0bcae2af0af7907c7f91e6`  
		Last Modified: Wed, 14 Apr 2021 16:10:14 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570a7e5edba00d92281a4a147639b5fc0b6724693cbfed80007b5b5db612a3e8`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60092b7b0679ad17236eb09b832adcc7bb67a5fd8c2d9a69ffbfc863716274c2`  
		Last Modified: Wed, 14 Apr 2021 16:10:15 GMT  
		Size: 5.1 MB (5072726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5d3b99689d155ccd6cdf6acbc7ef61472c65ce2cee49f441c4c3b844242410`  
		Last Modified: Wed, 14 Apr 2021 16:10:13 GMT  
		Size: 9.3 MB (9302175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dae780c7132cf39c97d1602e11b6a58481594df6d896054f3a9e6e9f54e63a`  
		Last Modified: Wed, 14 Apr 2021 16:10:10 GMT  
		Size: 2.0 KB (1957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f2291e14ae4d6e97942f3284122a80c7c969cb9bcfc9a417a833439505f85d`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b07be56d63a82b0606023df13bf32a522a13a12a44c53116ec24d0c1bd2ca1`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6cc0327d5edba60d3e99a97fa6c015e1953c9451bc816f20d6d73a67b9e426`  
		Last Modified: Wed, 14 Apr 2021 16:10:11 GMT  
		Size: 1.4 KB (1424 bytes)  
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

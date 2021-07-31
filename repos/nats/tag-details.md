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
-	[`nats:2.3`](#nats23)
-	[`nats:2.3-alpine`](#nats23-alpine)
-	[`nats:2.3-alpine3.14`](#nats23-alpine314)
-	[`nats:2.3-linux`](#nats23-linux)
-	[`nats:2.3-nanoserver`](#nats23-nanoserver)
-	[`nats:2.3-nanoserver-1809`](#nats23-nanoserver-1809)
-	[`nats:2.3-scratch`](#nats23-scratch)
-	[`nats:2.3-windowsservercore`](#nats23-windowsservercore)
-	[`nats:2.3-windowsservercore-1809`](#nats23-windowsservercore-1809)
-	[`nats:2.3-windowsservercore-ltsc2016`](#nats23-windowsservercore-ltsc2016)
-	[`nats:2.3.2`](#nats232)
-	[`nats:2.3.2-alpine`](#nats232-alpine)
-	[`nats:2.3.2-alpine3.14`](#nats232-alpine314)
-	[`nats:2.3.2-linux`](#nats232-linux)
-	[`nats:2.3.2-nanoserver`](#nats232-nanoserver)
-	[`nats:2.3.2-nanoserver-1809`](#nats232-nanoserver-1809)
-	[`nats:2.3.2-scratch`](#nats232-scratch)
-	[`nats:2.3.2-windowsservercore`](#nats232-windowsservercore)
-	[`nats:2.3.2-windowsservercore-1809`](#nats232-windowsservercore-1809)
-	[`nats:2.3.2-windowsservercore-ltsc2016`](#nats232-windowsservercore-ltsc2016)
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
$ docker pull nats@sha256:a22f80da6194bad3f89acb878d319d07bef10f6ea86c00c88721e96b45df7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2061; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:da01747b3b1b793d26f23d641b1e96439c8a4a7e06f996382ad5a588b3f22e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72641b68d54bc7007ad321eb3eab0f114b2744342ca010c87f647f84c0b86bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:697b18ad11c92732a089bd820afbe690cc8392744bc144a4dd94fd2d25aba511 in /nats-server 
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 00:20:42 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 00:20:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:411fd8300ee124a1c5d0cc25aaede18c5e3b9fcf63ad8db3e23a2a589145d0a0`  
		Last Modified: Wed, 07 Jul 2021 00:21:35 GMT  
		Size: 4.3 MB (4338149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214f5e8798288f091409c5b65e7d796a10e7924cb3aab9f85ea83d1837dca61`  
		Last Modified: Wed, 07 Jul 2021 00:21:34 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:11d953a654ef8984c4a9d2a827f11e5eed4a915f05dde024747634b3936c2949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1823a5f86be207fedbb468235bfd36c4b4b33de712c7d197b20c4b867cc10b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 03:21:12 GMT
COPY file:d4fbcc1923412df19a9fc206b745d07fe40999759232f3707f975a3195904bce in /nats-server 
# Wed, 07 Jul 2021 03:21:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 03:21:14 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 03:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 03:21:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ecb7ed08cb4eadf3cb26a4e7eb5c842903e149b620335c14815b4802f4ef67e`  
		Last Modified: Wed, 07 Jul 2021 03:23:40 GMT  
		Size: 4.0 MB (3997302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744553c17d9fabfcec8a7f1d9e4bd2d190b882df4735823eae181498786e62dd`  
		Last Modified: Wed, 07 Jul 2021 03:23:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:def02210305c7940addd2f5e26e8417017a2f2ae11116ee001b8f2a7bcb17bff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20941bb671159cef8cb5d6b9047f5c6c298a495274b06f9c6d9278ea5f9e5a1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:38:20 GMT
COPY file:a259b6f87cc2d22082524e5ba23201057e836734749f0d28676e8637d920d385 in /nats-server 
# Wed, 07 Jul 2021 06:38:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:38:21 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:38:22 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:38:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:434fc0c4a6c5daa82c731102728bcac575b5a312862a89edf401b0305d2efc82`  
		Last Modified: Wed, 07 Jul 2021 06:40:42 GMT  
		Size: 4.0 MB (3992410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c195f08925b050ce566763c31c813f3d8c7e1ba40bc4ccdf0949cb87373c3a43`  
		Last Modified: Wed, 07 Jul 2021 06:40:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:173c1afbfe6375d1f5670d632776a2132a1162d63517b952247a24e276bf1cdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4271d9d9d24a753bd371794f03c2c998e68346939612c8fd4c4c87ce372beb7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:ca5c64a22cab87809781278f49e476ff3d7d60b6d6d543ec243ed60a38654388 in /nats-server 
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:47:25 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:47:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:47:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c79949c52fa3b392514bb25b934eddd3777757b19d9389238626e96a6a3a243`  
		Last Modified: Wed, 07 Jul 2021 06:48:50 GMT  
		Size: 4.0 MB (3960542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0d08b9515c574d6baae1ae28b5767b4dd1a3ef4fec706cd0441f08497c619`  
		Last Modified: Wed, 07 Jul 2021 06:48:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:78a502a4470119b5ccf89f143feb35c164329288904ca0a2733b5331ec765ca8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107131765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479dee98537cc4a38350f37c146d6779bb0ae71a188e169fa838fc485e3016d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:35:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:28 GMT
RUN cmd /S /C #(nop) COPY file:573109625f0f6f957389174434c1f89cbff70ddfa1fa88ec82d3bbcc17b55fc0 in C:\nats-server.exe 
# Wed, 14 Jul 2021 02:35:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec20c4c9f6fa5e782e09342d50033ef24c4049a9dad1befd33c96759b71da6de`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54da7510a4c6639da510b1b1d4ef3c60875b1c401117b4caa1de1831db9e316`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 4.4 MB (4399677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa421afe026b6d93c2ee9b799feca2b86512c2c5a2e69c58eb68808dd7fd6`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.8 KB (1776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fbe77295342d38688cb0f7212e9ee70e7fc78dfa739e6fcd3d2c774b7d77`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09913e0e2081a0b9559e8643c36d52e8a63b692308f7b08310c99502f845bc`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f9e3c1e074debc991926ff6a6674e615ff31c36080c4fa5f6e2d1150f357`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:311b5c6c40288203dc4e3281b4a9b3c4a6cac4f3383dd8da40e6a546e5d8e884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:3c2b7ad7052fdc5f13e360dc9b3e3513997b071ec008bd61d3bff3e862c1947a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49258f52dfceee0babf527ce8158ba3f98a998fa6ff73f8dc05dc67ec2c7a96e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 00:20:14 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 00:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 00:20:18 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 00:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be4d9f8cb68409d6fb7407ab14ce49d214464c023f641670bfdefab42009a4`  
		Last Modified: Wed, 07 Jul 2021 00:21:10 GMT  
		Size: 4.6 MB (4621729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee574d4f4017f32800275aeefde40b62872bca2876fe91025cdc68dd97f0d8c7`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d9cc62817a68bf383b92f18b776f88224028a2c6e33c8df4dcad380c76ec52`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:4847b1671080a6caad7803cf200ced965db8767cc9bf2074acbb47c8af4285a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6904326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e2558ac7efdda215c5835a53e89fbbed3cbf5663aa449620393561fb6c4371`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:42 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Fri, 30 Jul 2021 17:49:42 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:37:00 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 02:37:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 02:37:06 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 02:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 02:37:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59232f7a71e570822a9e6fb2265a241076b0256fcc9b0922b6e2f6872bd59ab`  
		Last Modified: Sat, 31 Jul 2021 02:39:09 GMT  
		Size: 4.3 MB (4278973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed212fd4c3d3aae796a3e81594b3919840f408ea96c0732151264bf34f2e06a0`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10863bd3a6e18b15368401690e36adf17ea3f7e91b7f4213e0b57bd0680dbeb`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:0cd94d122e5dd418d4d447257c6622e13c1d86149c0e7979057664951ab5a020
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6703143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5635c4604b79a25fc3fdf3ccf6606d69eb347b3e8a3cb756dd261e2ca83e780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 03:13:57 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 03:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 03:14:04 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 03:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 03:14:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0b8bfe79fe7add5c0f3af812a506d01cc94a574cd58ba1f81146318d3638c`  
		Last Modified: Sat, 31 Jul 2021 03:16:43 GMT  
		Size: 4.3 MB (4274251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35ac8f58b7f43ebc215a5713841cf5a94983b092019cf46da7ce8a3c9c84146`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735e5b5c342cb95f3f2eb33812321a4305479b159555d6fed062e4bb2880dc66`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:deaf6d647392081aca4583994c636c08933207d39db66c3f1c95b819b22b6b5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3354f4f30fd9160606507f59e9f0408338ff23f522fe71627defa8faa9793c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 06:46:50 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 06:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 06:46:54 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:46:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 06:46:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466aa348560edb5133af08a0f1c6913f1e859d87ac4efe59f2d0caa58c3a2b27`  
		Last Modified: Wed, 07 Jul 2021 06:48:18 GMT  
		Size: 4.2 MB (4244306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf9efaff12ffb1bc52633008fbb1ea048542934bc23331770580cf3e81ba97e`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674feaf82840d440dfb9812d17bd6603ff1bb7bbd1bc6a191ce7b456ed497839`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.14`

```console
$ docker pull nats@sha256:311b5c6c40288203dc4e3281b4a9b3c4a6cac4f3383dd8da40e6a546e5d8e884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:3c2b7ad7052fdc5f13e360dc9b3e3513997b071ec008bd61d3bff3e862c1947a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49258f52dfceee0babf527ce8158ba3f98a998fa6ff73f8dc05dc67ec2c7a96e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 00:20:14 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 00:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 00:20:18 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 00:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be4d9f8cb68409d6fb7407ab14ce49d214464c023f641670bfdefab42009a4`  
		Last Modified: Wed, 07 Jul 2021 00:21:10 GMT  
		Size: 4.6 MB (4621729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee574d4f4017f32800275aeefde40b62872bca2876fe91025cdc68dd97f0d8c7`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d9cc62817a68bf383b92f18b776f88224028a2c6e33c8df4dcad380c76ec52`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:4847b1671080a6caad7803cf200ced965db8767cc9bf2074acbb47c8af4285a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6904326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e2558ac7efdda215c5835a53e89fbbed3cbf5663aa449620393561fb6c4371`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:42 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Fri, 30 Jul 2021 17:49:42 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:37:00 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 02:37:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 02:37:06 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 02:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 02:37:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59232f7a71e570822a9e6fb2265a241076b0256fcc9b0922b6e2f6872bd59ab`  
		Last Modified: Sat, 31 Jul 2021 02:39:09 GMT  
		Size: 4.3 MB (4278973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed212fd4c3d3aae796a3e81594b3919840f408ea96c0732151264bf34f2e06a0`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10863bd3a6e18b15368401690e36adf17ea3f7e91b7f4213e0b57bd0680dbeb`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:0cd94d122e5dd418d4d447257c6622e13c1d86149c0e7979057664951ab5a020
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6703143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5635c4604b79a25fc3fdf3ccf6606d69eb347b3e8a3cb756dd261e2ca83e780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 03:13:57 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 03:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 03:14:04 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 03:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 03:14:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0b8bfe79fe7add5c0f3af812a506d01cc94a574cd58ba1f81146318d3638c`  
		Last Modified: Sat, 31 Jul 2021 03:16:43 GMT  
		Size: 4.3 MB (4274251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35ac8f58b7f43ebc215a5713841cf5a94983b092019cf46da7ce8a3c9c84146`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735e5b5c342cb95f3f2eb33812321a4305479b159555d6fed062e4bb2880dc66`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:deaf6d647392081aca4583994c636c08933207d39db66c3f1c95b819b22b6b5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3354f4f30fd9160606507f59e9f0408338ff23f522fe71627defa8faa9793c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 06:46:50 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 06:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 06:46:54 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:46:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 06:46:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466aa348560edb5133af08a0f1c6913f1e859d87ac4efe59f2d0caa58c3a2b27`  
		Last Modified: Wed, 07 Jul 2021 06:48:18 GMT  
		Size: 4.2 MB (4244306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf9efaff12ffb1bc52633008fbb1ea048542934bc23331770580cf3e81ba97e`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674feaf82840d440dfb9812d17bd6603ff1bb7bbd1bc6a191ce7b456ed497839`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:0af0863d42cecaaf08f44e31a170fe6a0d640ed1980f2979e09863167ea5c5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:da01747b3b1b793d26f23d641b1e96439c8a4a7e06f996382ad5a588b3f22e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72641b68d54bc7007ad321eb3eab0f114b2744342ca010c87f647f84c0b86bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:697b18ad11c92732a089bd820afbe690cc8392744bc144a4dd94fd2d25aba511 in /nats-server 
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 00:20:42 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 00:20:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:411fd8300ee124a1c5d0cc25aaede18c5e3b9fcf63ad8db3e23a2a589145d0a0`  
		Last Modified: Wed, 07 Jul 2021 00:21:35 GMT  
		Size: 4.3 MB (4338149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214f5e8798288f091409c5b65e7d796a10e7924cb3aab9f85ea83d1837dca61`  
		Last Modified: Wed, 07 Jul 2021 00:21:34 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:11d953a654ef8984c4a9d2a827f11e5eed4a915f05dde024747634b3936c2949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1823a5f86be207fedbb468235bfd36c4b4b33de712c7d197b20c4b867cc10b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 03:21:12 GMT
COPY file:d4fbcc1923412df19a9fc206b745d07fe40999759232f3707f975a3195904bce in /nats-server 
# Wed, 07 Jul 2021 03:21:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 03:21:14 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 03:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 03:21:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ecb7ed08cb4eadf3cb26a4e7eb5c842903e149b620335c14815b4802f4ef67e`  
		Last Modified: Wed, 07 Jul 2021 03:23:40 GMT  
		Size: 4.0 MB (3997302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744553c17d9fabfcec8a7f1d9e4bd2d190b882df4735823eae181498786e62dd`  
		Last Modified: Wed, 07 Jul 2021 03:23:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:def02210305c7940addd2f5e26e8417017a2f2ae11116ee001b8f2a7bcb17bff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20941bb671159cef8cb5d6b9047f5c6c298a495274b06f9c6d9278ea5f9e5a1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:38:20 GMT
COPY file:a259b6f87cc2d22082524e5ba23201057e836734749f0d28676e8637d920d385 in /nats-server 
# Wed, 07 Jul 2021 06:38:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:38:21 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:38:22 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:38:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:434fc0c4a6c5daa82c731102728bcac575b5a312862a89edf401b0305d2efc82`  
		Last Modified: Wed, 07 Jul 2021 06:40:42 GMT  
		Size: 4.0 MB (3992410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c195f08925b050ce566763c31c813f3d8c7e1ba40bc4ccdf0949cb87373c3a43`  
		Last Modified: Wed, 07 Jul 2021 06:40:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:173c1afbfe6375d1f5670d632776a2132a1162d63517b952247a24e276bf1cdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4271d9d9d24a753bd371794f03c2c998e68346939612c8fd4c4c87ce372beb7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:ca5c64a22cab87809781278f49e476ff3d7d60b6d6d543ec243ed60a38654388 in /nats-server 
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:47:25 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:47:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:47:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c79949c52fa3b392514bb25b934eddd3777757b19d9389238626e96a6a3a243`  
		Last Modified: Wed, 07 Jul 2021 06:48:50 GMT  
		Size: 4.0 MB (3960542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0d08b9515c574d6baae1ae28b5767b4dd1a3ef4fec706cd0441f08497c619`  
		Last Modified: Wed, 07 Jul 2021 06:48:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:5a0efd0e8d161d797c966f6e269a09b2c527a6761d49314012f29ac83654b1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:78a502a4470119b5ccf89f143feb35c164329288904ca0a2733b5331ec765ca8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107131765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479dee98537cc4a38350f37c146d6779bb0ae71a188e169fa838fc485e3016d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:35:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:28 GMT
RUN cmd /S /C #(nop) COPY file:573109625f0f6f957389174434c1f89cbff70ddfa1fa88ec82d3bbcc17b55fc0 in C:\nats-server.exe 
# Wed, 14 Jul 2021 02:35:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec20c4c9f6fa5e782e09342d50033ef24c4049a9dad1befd33c96759b71da6de`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54da7510a4c6639da510b1b1d4ef3c60875b1c401117b4caa1de1831db9e316`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 4.4 MB (4399677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa421afe026b6d93c2ee9b799feca2b86512c2c5a2e69c58eb68808dd7fd6`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.8 KB (1776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fbe77295342d38688cb0f7212e9ee70e7fc78dfa739e6fcd3d2c774b7d77`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09913e0e2081a0b9559e8643c36d52e8a63b692308f7b08310c99502f845bc`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f9e3c1e074debc991926ff6a6674e615ff31c36080c4fa5f6e2d1150f357`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:5a0efd0e8d161d797c966f6e269a09b2c527a6761d49314012f29ac83654b1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:78a502a4470119b5ccf89f143feb35c164329288904ca0a2733b5331ec765ca8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107131765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479dee98537cc4a38350f37c146d6779bb0ae71a188e169fa838fc485e3016d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:35:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:28 GMT
RUN cmd /S /C #(nop) COPY file:573109625f0f6f957389174434c1f89cbff70ddfa1fa88ec82d3bbcc17b55fc0 in C:\nats-server.exe 
# Wed, 14 Jul 2021 02:35:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec20c4c9f6fa5e782e09342d50033ef24c4049a9dad1befd33c96759b71da6de`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54da7510a4c6639da510b1b1d4ef3c60875b1c401117b4caa1de1831db9e316`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 4.4 MB (4399677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa421afe026b6d93c2ee9b799feca2b86512c2c5a2e69c58eb68808dd7fd6`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.8 KB (1776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fbe77295342d38688cb0f7212e9ee70e7fc78dfa739e6fcd3d2c774b7d77`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09913e0e2081a0b9559e8643c36d52e8a63b692308f7b08310c99502f845bc`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f9e3c1e074debc991926ff6a6674e615ff31c36080c4fa5f6e2d1150f357`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:0af0863d42cecaaf08f44e31a170fe6a0d640ed1980f2979e09863167ea5c5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:da01747b3b1b793d26f23d641b1e96439c8a4a7e06f996382ad5a588b3f22e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72641b68d54bc7007ad321eb3eab0f114b2744342ca010c87f647f84c0b86bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:697b18ad11c92732a089bd820afbe690cc8392744bc144a4dd94fd2d25aba511 in /nats-server 
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 00:20:42 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 00:20:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:411fd8300ee124a1c5d0cc25aaede18c5e3b9fcf63ad8db3e23a2a589145d0a0`  
		Last Modified: Wed, 07 Jul 2021 00:21:35 GMT  
		Size: 4.3 MB (4338149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214f5e8798288f091409c5b65e7d796a10e7924cb3aab9f85ea83d1837dca61`  
		Last Modified: Wed, 07 Jul 2021 00:21:34 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:11d953a654ef8984c4a9d2a827f11e5eed4a915f05dde024747634b3936c2949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1823a5f86be207fedbb468235bfd36c4b4b33de712c7d197b20c4b867cc10b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 03:21:12 GMT
COPY file:d4fbcc1923412df19a9fc206b745d07fe40999759232f3707f975a3195904bce in /nats-server 
# Wed, 07 Jul 2021 03:21:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 03:21:14 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 03:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 03:21:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ecb7ed08cb4eadf3cb26a4e7eb5c842903e149b620335c14815b4802f4ef67e`  
		Last Modified: Wed, 07 Jul 2021 03:23:40 GMT  
		Size: 4.0 MB (3997302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744553c17d9fabfcec8a7f1d9e4bd2d190b882df4735823eae181498786e62dd`  
		Last Modified: Wed, 07 Jul 2021 03:23:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:def02210305c7940addd2f5e26e8417017a2f2ae11116ee001b8f2a7bcb17bff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20941bb671159cef8cb5d6b9047f5c6c298a495274b06f9c6d9278ea5f9e5a1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:38:20 GMT
COPY file:a259b6f87cc2d22082524e5ba23201057e836734749f0d28676e8637d920d385 in /nats-server 
# Wed, 07 Jul 2021 06:38:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:38:21 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:38:22 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:38:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:434fc0c4a6c5daa82c731102728bcac575b5a312862a89edf401b0305d2efc82`  
		Last Modified: Wed, 07 Jul 2021 06:40:42 GMT  
		Size: 4.0 MB (3992410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c195f08925b050ce566763c31c813f3d8c7e1ba40bc4ccdf0949cb87373c3a43`  
		Last Modified: Wed, 07 Jul 2021 06:40:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:173c1afbfe6375d1f5670d632776a2132a1162d63517b952247a24e276bf1cdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4271d9d9d24a753bd371794f03c2c998e68346939612c8fd4c4c87ce372beb7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:ca5c64a22cab87809781278f49e476ff3d7d60b6d6d543ec243ed60a38654388 in /nats-server 
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:47:25 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:47:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:47:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c79949c52fa3b392514bb25b934eddd3777757b19d9389238626e96a6a3a243`  
		Last Modified: Wed, 07 Jul 2021 06:48:50 GMT  
		Size: 4.0 MB (3960542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0d08b9515c574d6baae1ae28b5767b4dd1a3ef4fec706cd0441f08497c619`  
		Last Modified: Wed, 07 Jul 2021 06:48:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:0b8e165d4355d79cc830cad2c312463d6c6b26fb861b5d51a4f2e98df4592627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2061; amd64
	-	windows version 10.0.14393.4530; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:ca5887b3ce3a2738a0cfef1b4fd7cef529463530fa913d9a5475dae6f42b4ab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2690560697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b4597deddc6fd13552dd1047dafd05cec22dcbad1a8b9cc530ec01c876e72`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 01:07:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:31:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:31:29 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:31:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:31:35 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:33:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:34:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:34:57 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:00 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:adcec6ff907307155c0652222cc9b95a0cc964d4c371e02767e72a5c90472192`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92bdc410321db22d4cf09322869bd9fb2495788c3725624c86d76a6ab3d95d3`  
		Last Modified: Wed, 14 Jul 2021 02:40:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd169b67bc0adfc5e8226697e4b07a433d05f84e1f7980b215d9126986ac8c4a`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695a1183c47a024177260d6b0f7eff188406b4ab73009e842467f74341644a3`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf9174b261ac8925172304e0ac5ec195d9c6dffe5af096c1ed7184e214a5f13`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98392ef89b669613db784f731fccf1528b34957595fb1c683d489bd5761413c`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 360.2 KB (360240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db372963a1fbdd84f209e09c63d416d5a046688eac3586747db505d4aa5c5034`  
		Last Modified: Wed, 14 Jul 2021 02:40:17 GMT  
		Size: 4.7 MB (4740427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beaa69f0b720b237e52da8c8fe32c34a1f02bae8dcd52a610c9fbb01534c70a`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4ff7071a01299a4c43612bdcc5bf06555b7d0ed7e93f9aa5a043eda5d00102`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1a64510bb6ae1abc9697871026362c0c6481cc9f0c3c547fada800dcdb72c0`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0d00003e8fcfea5412c43907e3ed19bd73d18b392b24ed5607642abea515a8`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.4530; amd64

```console
$ docker pull nats@sha256:491f727092d1f1cc50faa02fa4b0c23d1dec175367f55291964468853737ab05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6279205071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fec2ab6a3510ab48fb94d8e3122a4055cca848ef1c6e2560c443fc31346f2d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 01:14:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:35:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:51 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:35:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:35:57 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:37:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:39:29 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:39:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:39:35 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:39:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:39:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fed351b78c876c55ec9c7e75d3b9d1b146c5c5dfeb4b5480c0a7c384322df98c`  
		Last Modified: Wed, 14 Jul 2021 02:03:37 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf08cae8b8db8f3f89e1a9192d393f2da55b44efce4e778fdb58debe2d608275`  
		Last Modified: Wed, 14 Jul 2021 02:40:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301246d6a689a00ca80c879c7036294c7c08f9628a3f7e143d00600f5fae9a2`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1135fddfb2a7acb97ec630ed1c2c9c9f7c53cdc995ae9ce746a18b8b67463f17`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c522e9c4ef7e0c5d6366bc22e9dd4ccd99d4e97501eec8ee9d83a0584f452e6`  
		Last Modified: Wed, 14 Jul 2021 02:40:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f11d018be60739ca143906be9e8a5d7833e083c9e76f9b4c5ad679dd62e546`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 325.3 KB (325309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef654d127a05fa7be2581174b3af9056cd84a24b53d639b29790480363fd13a`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 9.2 MB (9235231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62edb8d00046240ed89b64b658216821381a04ad85d9e93148a87633dceebad`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af7ff0ca1393713d4ada7de795553fe6e3ba4c1eb050652a87f27fc1cc293fb`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034662c21f82b31e87a354b8351637cedaeae62586649149d223908bd4c06b62`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07aed375d2f1ee02071c44422a10de0afa5fa38501cb09fa40125ad504ad6bd8`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:de456b6d65e1ee5c7a2a23ed3122872764275185e5f749034e065b1e9cdb1ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:ca5887b3ce3a2738a0cfef1b4fd7cef529463530fa913d9a5475dae6f42b4ab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2690560697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b4597deddc6fd13552dd1047dafd05cec22dcbad1a8b9cc530ec01c876e72`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 01:07:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:31:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:31:29 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:31:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:31:35 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:33:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:34:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:34:57 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:00 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:adcec6ff907307155c0652222cc9b95a0cc964d4c371e02767e72a5c90472192`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92bdc410321db22d4cf09322869bd9fb2495788c3725624c86d76a6ab3d95d3`  
		Last Modified: Wed, 14 Jul 2021 02:40:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd169b67bc0adfc5e8226697e4b07a433d05f84e1f7980b215d9126986ac8c4a`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695a1183c47a024177260d6b0f7eff188406b4ab73009e842467f74341644a3`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf9174b261ac8925172304e0ac5ec195d9c6dffe5af096c1ed7184e214a5f13`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98392ef89b669613db784f731fccf1528b34957595fb1c683d489bd5761413c`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 360.2 KB (360240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db372963a1fbdd84f209e09c63d416d5a046688eac3586747db505d4aa5c5034`  
		Last Modified: Wed, 14 Jul 2021 02:40:17 GMT  
		Size: 4.7 MB (4740427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beaa69f0b720b237e52da8c8fe32c34a1f02bae8dcd52a610c9fbb01534c70a`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4ff7071a01299a4c43612bdcc5bf06555b7d0ed7e93f9aa5a043eda5d00102`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1a64510bb6ae1abc9697871026362c0c6481cc9f0c3c547fada800dcdb72c0`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0d00003e8fcfea5412c43907e3ed19bd73d18b392b24ed5607642abea515a8`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b192069a4cfd70392063967b2ce1090d6f8a094812fa4be622ffa35843463560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4530; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4530; amd64

```console
$ docker pull nats@sha256:491f727092d1f1cc50faa02fa4b0c23d1dec175367f55291964468853737ab05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6279205071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fec2ab6a3510ab48fb94d8e3122a4055cca848ef1c6e2560c443fc31346f2d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 01:14:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:35:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:51 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:35:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:35:57 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:37:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:39:29 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:39:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:39:35 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:39:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:39:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fed351b78c876c55ec9c7e75d3b9d1b146c5c5dfeb4b5480c0a7c384322df98c`  
		Last Modified: Wed, 14 Jul 2021 02:03:37 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf08cae8b8db8f3f89e1a9192d393f2da55b44efce4e778fdb58debe2d608275`  
		Last Modified: Wed, 14 Jul 2021 02:40:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301246d6a689a00ca80c879c7036294c7c08f9628a3f7e143d00600f5fae9a2`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1135fddfb2a7acb97ec630ed1c2c9c9f7c53cdc995ae9ce746a18b8b67463f17`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c522e9c4ef7e0c5d6366bc22e9dd4ccd99d4e97501eec8ee9d83a0584f452e6`  
		Last Modified: Wed, 14 Jul 2021 02:40:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f11d018be60739ca143906be9e8a5d7833e083c9e76f9b4c5ad679dd62e546`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 325.3 KB (325309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef654d127a05fa7be2581174b3af9056cd84a24b53d639b29790480363fd13a`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 9.2 MB (9235231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62edb8d00046240ed89b64b658216821381a04ad85d9e93148a87633dceebad`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af7ff0ca1393713d4ada7de795553fe6e3ba4c1eb050652a87f27fc1cc293fb`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034662c21f82b31e87a354b8351637cedaeae62586649149d223908bd4c06b62`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07aed375d2f1ee02071c44422a10de0afa5fa38501cb09fa40125ad504ad6bd8`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3`

```console
$ docker pull nats@sha256:a22f80da6194bad3f89acb878d319d07bef10f6ea86c00c88721e96b45df7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2061; amd64

### `nats:2.3` - linux; amd64

```console
$ docker pull nats@sha256:da01747b3b1b793d26f23d641b1e96439c8a4a7e06f996382ad5a588b3f22e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72641b68d54bc7007ad321eb3eab0f114b2744342ca010c87f647f84c0b86bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:697b18ad11c92732a089bd820afbe690cc8392744bc144a4dd94fd2d25aba511 in /nats-server 
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 00:20:42 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 00:20:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:411fd8300ee124a1c5d0cc25aaede18c5e3b9fcf63ad8db3e23a2a589145d0a0`  
		Last Modified: Wed, 07 Jul 2021 00:21:35 GMT  
		Size: 4.3 MB (4338149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214f5e8798288f091409c5b65e7d796a10e7924cb3aab9f85ea83d1837dca61`  
		Last Modified: Wed, 07 Jul 2021 00:21:34 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3` - linux; arm variant v6

```console
$ docker pull nats@sha256:11d953a654ef8984c4a9d2a827f11e5eed4a915f05dde024747634b3936c2949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1823a5f86be207fedbb468235bfd36c4b4b33de712c7d197b20c4b867cc10b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 03:21:12 GMT
COPY file:d4fbcc1923412df19a9fc206b745d07fe40999759232f3707f975a3195904bce in /nats-server 
# Wed, 07 Jul 2021 03:21:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 03:21:14 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 03:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 03:21:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ecb7ed08cb4eadf3cb26a4e7eb5c842903e149b620335c14815b4802f4ef67e`  
		Last Modified: Wed, 07 Jul 2021 03:23:40 GMT  
		Size: 4.0 MB (3997302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744553c17d9fabfcec8a7f1d9e4bd2d190b882df4735823eae181498786e62dd`  
		Last Modified: Wed, 07 Jul 2021 03:23:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3` - linux; arm variant v7

```console
$ docker pull nats@sha256:def02210305c7940addd2f5e26e8417017a2f2ae11116ee001b8f2a7bcb17bff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20941bb671159cef8cb5d6b9047f5c6c298a495274b06f9c6d9278ea5f9e5a1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:38:20 GMT
COPY file:a259b6f87cc2d22082524e5ba23201057e836734749f0d28676e8637d920d385 in /nats-server 
# Wed, 07 Jul 2021 06:38:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:38:21 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:38:22 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:38:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:434fc0c4a6c5daa82c731102728bcac575b5a312862a89edf401b0305d2efc82`  
		Last Modified: Wed, 07 Jul 2021 06:40:42 GMT  
		Size: 4.0 MB (3992410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c195f08925b050ce566763c31c813f3d8c7e1ba40bc4ccdf0949cb87373c3a43`  
		Last Modified: Wed, 07 Jul 2021 06:40:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:173c1afbfe6375d1f5670d632776a2132a1162d63517b952247a24e276bf1cdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4271d9d9d24a753bd371794f03c2c998e68346939612c8fd4c4c87ce372beb7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:ca5c64a22cab87809781278f49e476ff3d7d60b6d6d543ec243ed60a38654388 in /nats-server 
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:47:25 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:47:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:47:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c79949c52fa3b392514bb25b934eddd3777757b19d9389238626e96a6a3a243`  
		Last Modified: Wed, 07 Jul 2021 06:48:50 GMT  
		Size: 4.0 MB (3960542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0d08b9515c574d6baae1ae28b5767b4dd1a3ef4fec706cd0441f08497c619`  
		Last Modified: Wed, 07 Jul 2021 06:48:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:78a502a4470119b5ccf89f143feb35c164329288904ca0a2733b5331ec765ca8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107131765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479dee98537cc4a38350f37c146d6779bb0ae71a188e169fa838fc485e3016d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:35:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:28 GMT
RUN cmd /S /C #(nop) COPY file:573109625f0f6f957389174434c1f89cbff70ddfa1fa88ec82d3bbcc17b55fc0 in C:\nats-server.exe 
# Wed, 14 Jul 2021 02:35:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec20c4c9f6fa5e782e09342d50033ef24c4049a9dad1befd33c96759b71da6de`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54da7510a4c6639da510b1b1d4ef3c60875b1c401117b4caa1de1831db9e316`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 4.4 MB (4399677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa421afe026b6d93c2ee9b799feca2b86512c2c5a2e69c58eb68808dd7fd6`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.8 KB (1776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fbe77295342d38688cb0f7212e9ee70e7fc78dfa739e6fcd3d2c774b7d77`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09913e0e2081a0b9559e8643c36d52e8a63b692308f7b08310c99502f845bc`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f9e3c1e074debc991926ff6a6674e615ff31c36080c4fa5f6e2d1150f357`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-alpine`

```console
$ docker pull nats@sha256:311b5c6c40288203dc4e3281b4a9b3c4a6cac4f3383dd8da40e6a546e5d8e884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3-alpine` - linux; amd64

```console
$ docker pull nats@sha256:3c2b7ad7052fdc5f13e360dc9b3e3513997b071ec008bd61d3bff3e862c1947a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49258f52dfceee0babf527ce8158ba3f98a998fa6ff73f8dc05dc67ec2c7a96e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 00:20:14 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 00:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 00:20:18 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 00:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be4d9f8cb68409d6fb7407ab14ce49d214464c023f641670bfdefab42009a4`  
		Last Modified: Wed, 07 Jul 2021 00:21:10 GMT  
		Size: 4.6 MB (4621729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee574d4f4017f32800275aeefde40b62872bca2876fe91025cdc68dd97f0d8c7`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d9cc62817a68bf383b92f18b776f88224028a2c6e33c8df4dcad380c76ec52`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:4847b1671080a6caad7803cf200ced965db8767cc9bf2074acbb47c8af4285a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6904326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e2558ac7efdda215c5835a53e89fbbed3cbf5663aa449620393561fb6c4371`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:42 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Fri, 30 Jul 2021 17:49:42 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:37:00 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 02:37:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 02:37:06 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 02:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 02:37:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59232f7a71e570822a9e6fb2265a241076b0256fcc9b0922b6e2f6872bd59ab`  
		Last Modified: Sat, 31 Jul 2021 02:39:09 GMT  
		Size: 4.3 MB (4278973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed212fd4c3d3aae796a3e81594b3919840f408ea96c0732151264bf34f2e06a0`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10863bd3a6e18b15368401690e36adf17ea3f7e91b7f4213e0b57bd0680dbeb`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:0cd94d122e5dd418d4d447257c6622e13c1d86149c0e7979057664951ab5a020
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6703143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5635c4604b79a25fc3fdf3ccf6606d69eb347b3e8a3cb756dd261e2ca83e780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 03:13:57 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 03:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 03:14:04 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 03:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 03:14:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0b8bfe79fe7add5c0f3af812a506d01cc94a574cd58ba1f81146318d3638c`  
		Last Modified: Sat, 31 Jul 2021 03:16:43 GMT  
		Size: 4.3 MB (4274251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35ac8f58b7f43ebc215a5713841cf5a94983b092019cf46da7ce8a3c9c84146`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735e5b5c342cb95f3f2eb33812321a4305479b159555d6fed062e4bb2880dc66`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:deaf6d647392081aca4583994c636c08933207d39db66c3f1c95b819b22b6b5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3354f4f30fd9160606507f59e9f0408338ff23f522fe71627defa8faa9793c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 06:46:50 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 06:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 06:46:54 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:46:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 06:46:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466aa348560edb5133af08a0f1c6913f1e859d87ac4efe59f2d0caa58c3a2b27`  
		Last Modified: Wed, 07 Jul 2021 06:48:18 GMT  
		Size: 4.2 MB (4244306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf9efaff12ffb1bc52633008fbb1ea048542934bc23331770580cf3e81ba97e`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674feaf82840d440dfb9812d17bd6603ff1bb7bbd1bc6a191ce7b456ed497839`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-alpine3.14`

```console
$ docker pull nats@sha256:311b5c6c40288203dc4e3281b4a9b3c4a6cac4f3383dd8da40e6a546e5d8e884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:3c2b7ad7052fdc5f13e360dc9b3e3513997b071ec008bd61d3bff3e862c1947a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49258f52dfceee0babf527ce8158ba3f98a998fa6ff73f8dc05dc67ec2c7a96e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 00:20:14 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 00:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 00:20:18 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 00:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be4d9f8cb68409d6fb7407ab14ce49d214464c023f641670bfdefab42009a4`  
		Last Modified: Wed, 07 Jul 2021 00:21:10 GMT  
		Size: 4.6 MB (4621729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee574d4f4017f32800275aeefde40b62872bca2876fe91025cdc68dd97f0d8c7`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d9cc62817a68bf383b92f18b776f88224028a2c6e33c8df4dcad380c76ec52`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:4847b1671080a6caad7803cf200ced965db8767cc9bf2074acbb47c8af4285a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6904326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e2558ac7efdda215c5835a53e89fbbed3cbf5663aa449620393561fb6c4371`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:42 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Fri, 30 Jul 2021 17:49:42 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:37:00 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 02:37:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 02:37:06 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 02:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 02:37:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59232f7a71e570822a9e6fb2265a241076b0256fcc9b0922b6e2f6872bd59ab`  
		Last Modified: Sat, 31 Jul 2021 02:39:09 GMT  
		Size: 4.3 MB (4278973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed212fd4c3d3aae796a3e81594b3919840f408ea96c0732151264bf34f2e06a0`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10863bd3a6e18b15368401690e36adf17ea3f7e91b7f4213e0b57bd0680dbeb`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:0cd94d122e5dd418d4d447257c6622e13c1d86149c0e7979057664951ab5a020
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6703143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5635c4604b79a25fc3fdf3ccf6606d69eb347b3e8a3cb756dd261e2ca83e780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 03:13:57 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 03:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 03:14:04 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 03:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 03:14:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0b8bfe79fe7add5c0f3af812a506d01cc94a574cd58ba1f81146318d3638c`  
		Last Modified: Sat, 31 Jul 2021 03:16:43 GMT  
		Size: 4.3 MB (4274251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35ac8f58b7f43ebc215a5713841cf5a94983b092019cf46da7ce8a3c9c84146`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735e5b5c342cb95f3f2eb33812321a4305479b159555d6fed062e4bb2880dc66`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:deaf6d647392081aca4583994c636c08933207d39db66c3f1c95b819b22b6b5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3354f4f30fd9160606507f59e9f0408338ff23f522fe71627defa8faa9793c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 06:46:50 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 06:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 06:46:54 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:46:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 06:46:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466aa348560edb5133af08a0f1c6913f1e859d87ac4efe59f2d0caa58c3a2b27`  
		Last Modified: Wed, 07 Jul 2021 06:48:18 GMT  
		Size: 4.2 MB (4244306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf9efaff12ffb1bc52633008fbb1ea048542934bc23331770580cf3e81ba97e`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674feaf82840d440dfb9812d17bd6603ff1bb7bbd1bc6a191ce7b456ed497839`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-linux`

```console
$ docker pull nats@sha256:0af0863d42cecaaf08f44e31a170fe6a0d640ed1980f2979e09863167ea5c5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3-linux` - linux; amd64

```console
$ docker pull nats@sha256:da01747b3b1b793d26f23d641b1e96439c8a4a7e06f996382ad5a588b3f22e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72641b68d54bc7007ad321eb3eab0f114b2744342ca010c87f647f84c0b86bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:697b18ad11c92732a089bd820afbe690cc8392744bc144a4dd94fd2d25aba511 in /nats-server 
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 00:20:42 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 00:20:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:411fd8300ee124a1c5d0cc25aaede18c5e3b9fcf63ad8db3e23a2a589145d0a0`  
		Last Modified: Wed, 07 Jul 2021 00:21:35 GMT  
		Size: 4.3 MB (4338149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214f5e8798288f091409c5b65e7d796a10e7924cb3aab9f85ea83d1837dca61`  
		Last Modified: Wed, 07 Jul 2021 00:21:34 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:11d953a654ef8984c4a9d2a827f11e5eed4a915f05dde024747634b3936c2949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1823a5f86be207fedbb468235bfd36c4b4b33de712c7d197b20c4b867cc10b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 03:21:12 GMT
COPY file:d4fbcc1923412df19a9fc206b745d07fe40999759232f3707f975a3195904bce in /nats-server 
# Wed, 07 Jul 2021 03:21:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 03:21:14 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 03:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 03:21:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ecb7ed08cb4eadf3cb26a4e7eb5c842903e149b620335c14815b4802f4ef67e`  
		Last Modified: Wed, 07 Jul 2021 03:23:40 GMT  
		Size: 4.0 MB (3997302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744553c17d9fabfcec8a7f1d9e4bd2d190b882df4735823eae181498786e62dd`  
		Last Modified: Wed, 07 Jul 2021 03:23:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:def02210305c7940addd2f5e26e8417017a2f2ae11116ee001b8f2a7bcb17bff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20941bb671159cef8cb5d6b9047f5c6c298a495274b06f9c6d9278ea5f9e5a1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:38:20 GMT
COPY file:a259b6f87cc2d22082524e5ba23201057e836734749f0d28676e8637d920d385 in /nats-server 
# Wed, 07 Jul 2021 06:38:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:38:21 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:38:22 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:38:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:434fc0c4a6c5daa82c731102728bcac575b5a312862a89edf401b0305d2efc82`  
		Last Modified: Wed, 07 Jul 2021 06:40:42 GMT  
		Size: 4.0 MB (3992410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c195f08925b050ce566763c31c813f3d8c7e1ba40bc4ccdf0949cb87373c3a43`  
		Last Modified: Wed, 07 Jul 2021 06:40:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:173c1afbfe6375d1f5670d632776a2132a1162d63517b952247a24e276bf1cdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4271d9d9d24a753bd371794f03c2c998e68346939612c8fd4c4c87ce372beb7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:ca5c64a22cab87809781278f49e476ff3d7d60b6d6d543ec243ed60a38654388 in /nats-server 
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:47:25 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:47:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:47:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c79949c52fa3b392514bb25b934eddd3777757b19d9389238626e96a6a3a243`  
		Last Modified: Wed, 07 Jul 2021 06:48:50 GMT  
		Size: 4.0 MB (3960542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0d08b9515c574d6baae1ae28b5767b4dd1a3ef4fec706cd0441f08497c619`  
		Last Modified: Wed, 07 Jul 2021 06:48:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-nanoserver`

```console
$ docker pull nats@sha256:5a0efd0e8d161d797c966f6e269a09b2c527a6761d49314012f29ac83654b1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:2.3-nanoserver` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:78a502a4470119b5ccf89f143feb35c164329288904ca0a2733b5331ec765ca8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107131765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479dee98537cc4a38350f37c146d6779bb0ae71a188e169fa838fc485e3016d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:35:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:28 GMT
RUN cmd /S /C #(nop) COPY file:573109625f0f6f957389174434c1f89cbff70ddfa1fa88ec82d3bbcc17b55fc0 in C:\nats-server.exe 
# Wed, 14 Jul 2021 02:35:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec20c4c9f6fa5e782e09342d50033ef24c4049a9dad1befd33c96759b71da6de`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54da7510a4c6639da510b1b1d4ef3c60875b1c401117b4caa1de1831db9e316`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 4.4 MB (4399677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa421afe026b6d93c2ee9b799feca2b86512c2c5a2e69c58eb68808dd7fd6`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.8 KB (1776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fbe77295342d38688cb0f7212e9ee70e7fc78dfa739e6fcd3d2c774b7d77`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09913e0e2081a0b9559e8643c36d52e8a63b692308f7b08310c99502f845bc`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f9e3c1e074debc991926ff6a6674e615ff31c36080c4fa5f6e2d1150f357`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-nanoserver-1809`

```console
$ docker pull nats@sha256:5a0efd0e8d161d797c966f6e269a09b2c527a6761d49314012f29ac83654b1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:2.3-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:78a502a4470119b5ccf89f143feb35c164329288904ca0a2733b5331ec765ca8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107131765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479dee98537cc4a38350f37c146d6779bb0ae71a188e169fa838fc485e3016d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:35:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:28 GMT
RUN cmd /S /C #(nop) COPY file:573109625f0f6f957389174434c1f89cbff70ddfa1fa88ec82d3bbcc17b55fc0 in C:\nats-server.exe 
# Wed, 14 Jul 2021 02:35:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec20c4c9f6fa5e782e09342d50033ef24c4049a9dad1befd33c96759b71da6de`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54da7510a4c6639da510b1b1d4ef3c60875b1c401117b4caa1de1831db9e316`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 4.4 MB (4399677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa421afe026b6d93c2ee9b799feca2b86512c2c5a2e69c58eb68808dd7fd6`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.8 KB (1776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fbe77295342d38688cb0f7212e9ee70e7fc78dfa739e6fcd3d2c774b7d77`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09913e0e2081a0b9559e8643c36d52e8a63b692308f7b08310c99502f845bc`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f9e3c1e074debc991926ff6a6674e615ff31c36080c4fa5f6e2d1150f357`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-scratch`

```console
$ docker pull nats@sha256:0af0863d42cecaaf08f44e31a170fe6a0d640ed1980f2979e09863167ea5c5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3-scratch` - linux; amd64

```console
$ docker pull nats@sha256:da01747b3b1b793d26f23d641b1e96439c8a4a7e06f996382ad5a588b3f22e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72641b68d54bc7007ad321eb3eab0f114b2744342ca010c87f647f84c0b86bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:697b18ad11c92732a089bd820afbe690cc8392744bc144a4dd94fd2d25aba511 in /nats-server 
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 00:20:42 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 00:20:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:411fd8300ee124a1c5d0cc25aaede18c5e3b9fcf63ad8db3e23a2a589145d0a0`  
		Last Modified: Wed, 07 Jul 2021 00:21:35 GMT  
		Size: 4.3 MB (4338149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214f5e8798288f091409c5b65e7d796a10e7924cb3aab9f85ea83d1837dca61`  
		Last Modified: Wed, 07 Jul 2021 00:21:34 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:11d953a654ef8984c4a9d2a827f11e5eed4a915f05dde024747634b3936c2949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1823a5f86be207fedbb468235bfd36c4b4b33de712c7d197b20c4b867cc10b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 03:21:12 GMT
COPY file:d4fbcc1923412df19a9fc206b745d07fe40999759232f3707f975a3195904bce in /nats-server 
# Wed, 07 Jul 2021 03:21:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 03:21:14 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 03:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 03:21:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ecb7ed08cb4eadf3cb26a4e7eb5c842903e149b620335c14815b4802f4ef67e`  
		Last Modified: Wed, 07 Jul 2021 03:23:40 GMT  
		Size: 4.0 MB (3997302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744553c17d9fabfcec8a7f1d9e4bd2d190b882df4735823eae181498786e62dd`  
		Last Modified: Wed, 07 Jul 2021 03:23:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:def02210305c7940addd2f5e26e8417017a2f2ae11116ee001b8f2a7bcb17bff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20941bb671159cef8cb5d6b9047f5c6c298a495274b06f9c6d9278ea5f9e5a1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:38:20 GMT
COPY file:a259b6f87cc2d22082524e5ba23201057e836734749f0d28676e8637d920d385 in /nats-server 
# Wed, 07 Jul 2021 06:38:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:38:21 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:38:22 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:38:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:434fc0c4a6c5daa82c731102728bcac575b5a312862a89edf401b0305d2efc82`  
		Last Modified: Wed, 07 Jul 2021 06:40:42 GMT  
		Size: 4.0 MB (3992410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c195f08925b050ce566763c31c813f3d8c7e1ba40bc4ccdf0949cb87373c3a43`  
		Last Modified: Wed, 07 Jul 2021 06:40:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:173c1afbfe6375d1f5670d632776a2132a1162d63517b952247a24e276bf1cdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4271d9d9d24a753bd371794f03c2c998e68346939612c8fd4c4c87ce372beb7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:ca5c64a22cab87809781278f49e476ff3d7d60b6d6d543ec243ed60a38654388 in /nats-server 
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:47:25 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:47:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:47:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c79949c52fa3b392514bb25b934eddd3777757b19d9389238626e96a6a3a243`  
		Last Modified: Wed, 07 Jul 2021 06:48:50 GMT  
		Size: 4.0 MB (3960542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0d08b9515c574d6baae1ae28b5767b4dd1a3ef4fec706cd0441f08497c619`  
		Last Modified: Wed, 07 Jul 2021 06:48:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-windowsservercore`

```console
$ docker pull nats@sha256:0b8e165d4355d79cc830cad2c312463d6c6b26fb861b5d51a4f2e98df4592627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2061; amd64
	-	windows version 10.0.14393.4530; amd64

### `nats:2.3-windowsservercore` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:ca5887b3ce3a2738a0cfef1b4fd7cef529463530fa913d9a5475dae6f42b4ab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2690560697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b4597deddc6fd13552dd1047dafd05cec22dcbad1a8b9cc530ec01c876e72`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 01:07:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:31:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:31:29 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:31:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:31:35 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:33:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:34:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:34:57 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:00 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:adcec6ff907307155c0652222cc9b95a0cc964d4c371e02767e72a5c90472192`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92bdc410321db22d4cf09322869bd9fb2495788c3725624c86d76a6ab3d95d3`  
		Last Modified: Wed, 14 Jul 2021 02:40:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd169b67bc0adfc5e8226697e4b07a433d05f84e1f7980b215d9126986ac8c4a`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695a1183c47a024177260d6b0f7eff188406b4ab73009e842467f74341644a3`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf9174b261ac8925172304e0ac5ec195d9c6dffe5af096c1ed7184e214a5f13`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98392ef89b669613db784f731fccf1528b34957595fb1c683d489bd5761413c`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 360.2 KB (360240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db372963a1fbdd84f209e09c63d416d5a046688eac3586747db505d4aa5c5034`  
		Last Modified: Wed, 14 Jul 2021 02:40:17 GMT  
		Size: 4.7 MB (4740427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beaa69f0b720b237e52da8c8fe32c34a1f02bae8dcd52a610c9fbb01534c70a`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4ff7071a01299a4c43612bdcc5bf06555b7d0ed7e93f9aa5a043eda5d00102`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1a64510bb6ae1abc9697871026362c0c6481cc9f0c3c547fada800dcdb72c0`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0d00003e8fcfea5412c43907e3ed19bd73d18b392b24ed5607642abea515a8`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3-windowsservercore` - windows version 10.0.14393.4530; amd64

```console
$ docker pull nats@sha256:491f727092d1f1cc50faa02fa4b0c23d1dec175367f55291964468853737ab05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6279205071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fec2ab6a3510ab48fb94d8e3122a4055cca848ef1c6e2560c443fc31346f2d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 01:14:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:35:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:51 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:35:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:35:57 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:37:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:39:29 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:39:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:39:35 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:39:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:39:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fed351b78c876c55ec9c7e75d3b9d1b146c5c5dfeb4b5480c0a7c384322df98c`  
		Last Modified: Wed, 14 Jul 2021 02:03:37 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf08cae8b8db8f3f89e1a9192d393f2da55b44efce4e778fdb58debe2d608275`  
		Last Modified: Wed, 14 Jul 2021 02:40:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301246d6a689a00ca80c879c7036294c7c08f9628a3f7e143d00600f5fae9a2`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1135fddfb2a7acb97ec630ed1c2c9c9f7c53cdc995ae9ce746a18b8b67463f17`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c522e9c4ef7e0c5d6366bc22e9dd4ccd99d4e97501eec8ee9d83a0584f452e6`  
		Last Modified: Wed, 14 Jul 2021 02:40:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f11d018be60739ca143906be9e8a5d7833e083c9e76f9b4c5ad679dd62e546`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 325.3 KB (325309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef654d127a05fa7be2581174b3af9056cd84a24b53d639b29790480363fd13a`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 9.2 MB (9235231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62edb8d00046240ed89b64b658216821381a04ad85d9e93148a87633dceebad`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af7ff0ca1393713d4ada7de795553fe6e3ba4c1eb050652a87f27fc1cc293fb`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034662c21f82b31e87a354b8351637cedaeae62586649149d223908bd4c06b62`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07aed375d2f1ee02071c44422a10de0afa5fa38501cb09fa40125ad504ad6bd8`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-windowsservercore-1809`

```console
$ docker pull nats@sha256:de456b6d65e1ee5c7a2a23ed3122872764275185e5f749034e065b1e9cdb1ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:2.3-windowsservercore-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:ca5887b3ce3a2738a0cfef1b4fd7cef529463530fa913d9a5475dae6f42b4ab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2690560697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b4597deddc6fd13552dd1047dafd05cec22dcbad1a8b9cc530ec01c876e72`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 01:07:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:31:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:31:29 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:31:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:31:35 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:33:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:34:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:34:57 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:00 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:adcec6ff907307155c0652222cc9b95a0cc964d4c371e02767e72a5c90472192`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92bdc410321db22d4cf09322869bd9fb2495788c3725624c86d76a6ab3d95d3`  
		Last Modified: Wed, 14 Jul 2021 02:40:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd169b67bc0adfc5e8226697e4b07a433d05f84e1f7980b215d9126986ac8c4a`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695a1183c47a024177260d6b0f7eff188406b4ab73009e842467f74341644a3`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf9174b261ac8925172304e0ac5ec195d9c6dffe5af096c1ed7184e214a5f13`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98392ef89b669613db784f731fccf1528b34957595fb1c683d489bd5761413c`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 360.2 KB (360240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db372963a1fbdd84f209e09c63d416d5a046688eac3586747db505d4aa5c5034`  
		Last Modified: Wed, 14 Jul 2021 02:40:17 GMT  
		Size: 4.7 MB (4740427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beaa69f0b720b237e52da8c8fe32c34a1f02bae8dcd52a610c9fbb01534c70a`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4ff7071a01299a4c43612bdcc5bf06555b7d0ed7e93f9aa5a043eda5d00102`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1a64510bb6ae1abc9697871026362c0c6481cc9f0c3c547fada800dcdb72c0`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0d00003e8fcfea5412c43907e3ed19bd73d18b392b24ed5607642abea515a8`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b192069a4cfd70392063967b2ce1090d6f8a094812fa4be622ffa35843463560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4530; amd64

### `nats:2.3-windowsservercore-ltsc2016` - windows version 10.0.14393.4530; amd64

```console
$ docker pull nats@sha256:491f727092d1f1cc50faa02fa4b0c23d1dec175367f55291964468853737ab05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6279205071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fec2ab6a3510ab48fb94d8e3122a4055cca848ef1c6e2560c443fc31346f2d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 01:14:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:35:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:51 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:35:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:35:57 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:37:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:39:29 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:39:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:39:35 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:39:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:39:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fed351b78c876c55ec9c7e75d3b9d1b146c5c5dfeb4b5480c0a7c384322df98c`  
		Last Modified: Wed, 14 Jul 2021 02:03:37 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf08cae8b8db8f3f89e1a9192d393f2da55b44efce4e778fdb58debe2d608275`  
		Last Modified: Wed, 14 Jul 2021 02:40:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301246d6a689a00ca80c879c7036294c7c08f9628a3f7e143d00600f5fae9a2`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1135fddfb2a7acb97ec630ed1c2c9c9f7c53cdc995ae9ce746a18b8b67463f17`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c522e9c4ef7e0c5d6366bc22e9dd4ccd99d4e97501eec8ee9d83a0584f452e6`  
		Last Modified: Wed, 14 Jul 2021 02:40:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f11d018be60739ca143906be9e8a5d7833e083c9e76f9b4c5ad679dd62e546`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 325.3 KB (325309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef654d127a05fa7be2581174b3af9056cd84a24b53d639b29790480363fd13a`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 9.2 MB (9235231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62edb8d00046240ed89b64b658216821381a04ad85d9e93148a87633dceebad`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af7ff0ca1393713d4ada7de795553fe6e3ba4c1eb050652a87f27fc1cc293fb`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034662c21f82b31e87a354b8351637cedaeae62586649149d223908bd4c06b62`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07aed375d2f1ee02071c44422a10de0afa5fa38501cb09fa40125ad504ad6bd8`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.2`

```console
$ docker pull nats@sha256:a22f80da6194bad3f89acb878d319d07bef10f6ea86c00c88721e96b45df7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2061; amd64

### `nats:2.3.2` - linux; amd64

```console
$ docker pull nats@sha256:da01747b3b1b793d26f23d641b1e96439c8a4a7e06f996382ad5a588b3f22e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72641b68d54bc7007ad321eb3eab0f114b2744342ca010c87f647f84c0b86bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:697b18ad11c92732a089bd820afbe690cc8392744bc144a4dd94fd2d25aba511 in /nats-server 
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 00:20:42 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 00:20:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:411fd8300ee124a1c5d0cc25aaede18c5e3b9fcf63ad8db3e23a2a589145d0a0`  
		Last Modified: Wed, 07 Jul 2021 00:21:35 GMT  
		Size: 4.3 MB (4338149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214f5e8798288f091409c5b65e7d796a10e7924cb3aab9f85ea83d1837dca61`  
		Last Modified: Wed, 07 Jul 2021 00:21:34 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2` - linux; arm variant v6

```console
$ docker pull nats@sha256:11d953a654ef8984c4a9d2a827f11e5eed4a915f05dde024747634b3936c2949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1823a5f86be207fedbb468235bfd36c4b4b33de712c7d197b20c4b867cc10b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 03:21:12 GMT
COPY file:d4fbcc1923412df19a9fc206b745d07fe40999759232f3707f975a3195904bce in /nats-server 
# Wed, 07 Jul 2021 03:21:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 03:21:14 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 03:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 03:21:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ecb7ed08cb4eadf3cb26a4e7eb5c842903e149b620335c14815b4802f4ef67e`  
		Last Modified: Wed, 07 Jul 2021 03:23:40 GMT  
		Size: 4.0 MB (3997302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744553c17d9fabfcec8a7f1d9e4bd2d190b882df4735823eae181498786e62dd`  
		Last Modified: Wed, 07 Jul 2021 03:23:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2` - linux; arm variant v7

```console
$ docker pull nats@sha256:def02210305c7940addd2f5e26e8417017a2f2ae11116ee001b8f2a7bcb17bff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20941bb671159cef8cb5d6b9047f5c6c298a495274b06f9c6d9278ea5f9e5a1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:38:20 GMT
COPY file:a259b6f87cc2d22082524e5ba23201057e836734749f0d28676e8637d920d385 in /nats-server 
# Wed, 07 Jul 2021 06:38:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:38:21 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:38:22 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:38:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:434fc0c4a6c5daa82c731102728bcac575b5a312862a89edf401b0305d2efc82`  
		Last Modified: Wed, 07 Jul 2021 06:40:42 GMT  
		Size: 4.0 MB (3992410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c195f08925b050ce566763c31c813f3d8c7e1ba40bc4ccdf0949cb87373c3a43`  
		Last Modified: Wed, 07 Jul 2021 06:40:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:173c1afbfe6375d1f5670d632776a2132a1162d63517b952247a24e276bf1cdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4271d9d9d24a753bd371794f03c2c998e68346939612c8fd4c4c87ce372beb7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:ca5c64a22cab87809781278f49e476ff3d7d60b6d6d543ec243ed60a38654388 in /nats-server 
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:47:25 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:47:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:47:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c79949c52fa3b392514bb25b934eddd3777757b19d9389238626e96a6a3a243`  
		Last Modified: Wed, 07 Jul 2021 06:48:50 GMT  
		Size: 4.0 MB (3960542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0d08b9515c574d6baae1ae28b5767b4dd1a3ef4fec706cd0441f08497c619`  
		Last Modified: Wed, 07 Jul 2021 06:48:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:78a502a4470119b5ccf89f143feb35c164329288904ca0a2733b5331ec765ca8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107131765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479dee98537cc4a38350f37c146d6779bb0ae71a188e169fa838fc485e3016d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:35:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:28 GMT
RUN cmd /S /C #(nop) COPY file:573109625f0f6f957389174434c1f89cbff70ddfa1fa88ec82d3bbcc17b55fc0 in C:\nats-server.exe 
# Wed, 14 Jul 2021 02:35:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec20c4c9f6fa5e782e09342d50033ef24c4049a9dad1befd33c96759b71da6de`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54da7510a4c6639da510b1b1d4ef3c60875b1c401117b4caa1de1831db9e316`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 4.4 MB (4399677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa421afe026b6d93c2ee9b799feca2b86512c2c5a2e69c58eb68808dd7fd6`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.8 KB (1776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fbe77295342d38688cb0f7212e9ee70e7fc78dfa739e6fcd3d2c774b7d77`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09913e0e2081a0b9559e8643c36d52e8a63b692308f7b08310c99502f845bc`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f9e3c1e074debc991926ff6a6674e615ff31c36080c4fa5f6e2d1150f357`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.2-alpine`

```console
$ docker pull nats@sha256:311b5c6c40288203dc4e3281b4a9b3c4a6cac4f3383dd8da40e6a546e5d8e884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3.2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:3c2b7ad7052fdc5f13e360dc9b3e3513997b071ec008bd61d3bff3e862c1947a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49258f52dfceee0babf527ce8158ba3f98a998fa6ff73f8dc05dc67ec2c7a96e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 00:20:14 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 00:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 00:20:18 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 00:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be4d9f8cb68409d6fb7407ab14ce49d214464c023f641670bfdefab42009a4`  
		Last Modified: Wed, 07 Jul 2021 00:21:10 GMT  
		Size: 4.6 MB (4621729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee574d4f4017f32800275aeefde40b62872bca2876fe91025cdc68dd97f0d8c7`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d9cc62817a68bf383b92f18b776f88224028a2c6e33c8df4dcad380c76ec52`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:4847b1671080a6caad7803cf200ced965db8767cc9bf2074acbb47c8af4285a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6904326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e2558ac7efdda215c5835a53e89fbbed3cbf5663aa449620393561fb6c4371`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:42 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Fri, 30 Jul 2021 17:49:42 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:37:00 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 02:37:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 02:37:06 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 02:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 02:37:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59232f7a71e570822a9e6fb2265a241076b0256fcc9b0922b6e2f6872bd59ab`  
		Last Modified: Sat, 31 Jul 2021 02:39:09 GMT  
		Size: 4.3 MB (4278973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed212fd4c3d3aae796a3e81594b3919840f408ea96c0732151264bf34f2e06a0`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10863bd3a6e18b15368401690e36adf17ea3f7e91b7f4213e0b57bd0680dbeb`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:0cd94d122e5dd418d4d447257c6622e13c1d86149c0e7979057664951ab5a020
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6703143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5635c4604b79a25fc3fdf3ccf6606d69eb347b3e8a3cb756dd261e2ca83e780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 03:13:57 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 03:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 03:14:04 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 03:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 03:14:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0b8bfe79fe7add5c0f3af812a506d01cc94a574cd58ba1f81146318d3638c`  
		Last Modified: Sat, 31 Jul 2021 03:16:43 GMT  
		Size: 4.3 MB (4274251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35ac8f58b7f43ebc215a5713841cf5a94983b092019cf46da7ce8a3c9c84146`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735e5b5c342cb95f3f2eb33812321a4305479b159555d6fed062e4bb2880dc66`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:deaf6d647392081aca4583994c636c08933207d39db66c3f1c95b819b22b6b5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3354f4f30fd9160606507f59e9f0408338ff23f522fe71627defa8faa9793c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 06:46:50 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 06:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 06:46:54 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:46:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 06:46:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466aa348560edb5133af08a0f1c6913f1e859d87ac4efe59f2d0caa58c3a2b27`  
		Last Modified: Wed, 07 Jul 2021 06:48:18 GMT  
		Size: 4.2 MB (4244306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf9efaff12ffb1bc52633008fbb1ea048542934bc23331770580cf3e81ba97e`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674feaf82840d440dfb9812d17bd6603ff1bb7bbd1bc6a191ce7b456ed497839`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.2-alpine3.14`

```console
$ docker pull nats@sha256:311b5c6c40288203dc4e3281b4a9b3c4a6cac4f3383dd8da40e6a546e5d8e884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3.2-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:3c2b7ad7052fdc5f13e360dc9b3e3513997b071ec008bd61d3bff3e862c1947a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49258f52dfceee0babf527ce8158ba3f98a998fa6ff73f8dc05dc67ec2c7a96e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 00:20:14 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 00:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 00:20:18 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 00:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be4d9f8cb68409d6fb7407ab14ce49d214464c023f641670bfdefab42009a4`  
		Last Modified: Wed, 07 Jul 2021 00:21:10 GMT  
		Size: 4.6 MB (4621729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee574d4f4017f32800275aeefde40b62872bca2876fe91025cdc68dd97f0d8c7`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d9cc62817a68bf383b92f18b776f88224028a2c6e33c8df4dcad380c76ec52`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:4847b1671080a6caad7803cf200ced965db8767cc9bf2074acbb47c8af4285a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6904326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e2558ac7efdda215c5835a53e89fbbed3cbf5663aa449620393561fb6c4371`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:42 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Fri, 30 Jul 2021 17:49:42 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:37:00 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 02:37:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 02:37:06 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 02:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 02:37:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59232f7a71e570822a9e6fb2265a241076b0256fcc9b0922b6e2f6872bd59ab`  
		Last Modified: Sat, 31 Jul 2021 02:39:09 GMT  
		Size: 4.3 MB (4278973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed212fd4c3d3aae796a3e81594b3919840f408ea96c0732151264bf34f2e06a0`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10863bd3a6e18b15368401690e36adf17ea3f7e91b7f4213e0b57bd0680dbeb`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:0cd94d122e5dd418d4d447257c6622e13c1d86149c0e7979057664951ab5a020
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6703143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5635c4604b79a25fc3fdf3ccf6606d69eb347b3e8a3cb756dd261e2ca83e780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 03:13:57 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 03:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 03:14:04 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 03:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 03:14:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0b8bfe79fe7add5c0f3af812a506d01cc94a574cd58ba1f81146318d3638c`  
		Last Modified: Sat, 31 Jul 2021 03:16:43 GMT  
		Size: 4.3 MB (4274251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35ac8f58b7f43ebc215a5713841cf5a94983b092019cf46da7ce8a3c9c84146`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735e5b5c342cb95f3f2eb33812321a4305479b159555d6fed062e4bb2880dc66`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:deaf6d647392081aca4583994c636c08933207d39db66c3f1c95b819b22b6b5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3354f4f30fd9160606507f59e9f0408338ff23f522fe71627defa8faa9793c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 06:46:50 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 06:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 06:46:54 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:46:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 06:46:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466aa348560edb5133af08a0f1c6913f1e859d87ac4efe59f2d0caa58c3a2b27`  
		Last Modified: Wed, 07 Jul 2021 06:48:18 GMT  
		Size: 4.2 MB (4244306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf9efaff12ffb1bc52633008fbb1ea048542934bc23331770580cf3e81ba97e`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674feaf82840d440dfb9812d17bd6603ff1bb7bbd1bc6a191ce7b456ed497839`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.2-linux`

```console
$ docker pull nats@sha256:0af0863d42cecaaf08f44e31a170fe6a0d640ed1980f2979e09863167ea5c5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3.2-linux` - linux; amd64

```console
$ docker pull nats@sha256:da01747b3b1b793d26f23d641b1e96439c8a4a7e06f996382ad5a588b3f22e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72641b68d54bc7007ad321eb3eab0f114b2744342ca010c87f647f84c0b86bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:697b18ad11c92732a089bd820afbe690cc8392744bc144a4dd94fd2d25aba511 in /nats-server 
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 00:20:42 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 00:20:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:411fd8300ee124a1c5d0cc25aaede18c5e3b9fcf63ad8db3e23a2a589145d0a0`  
		Last Modified: Wed, 07 Jul 2021 00:21:35 GMT  
		Size: 4.3 MB (4338149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214f5e8798288f091409c5b65e7d796a10e7924cb3aab9f85ea83d1837dca61`  
		Last Modified: Wed, 07 Jul 2021 00:21:34 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:11d953a654ef8984c4a9d2a827f11e5eed4a915f05dde024747634b3936c2949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1823a5f86be207fedbb468235bfd36c4b4b33de712c7d197b20c4b867cc10b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 03:21:12 GMT
COPY file:d4fbcc1923412df19a9fc206b745d07fe40999759232f3707f975a3195904bce in /nats-server 
# Wed, 07 Jul 2021 03:21:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 03:21:14 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 03:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 03:21:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ecb7ed08cb4eadf3cb26a4e7eb5c842903e149b620335c14815b4802f4ef67e`  
		Last Modified: Wed, 07 Jul 2021 03:23:40 GMT  
		Size: 4.0 MB (3997302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744553c17d9fabfcec8a7f1d9e4bd2d190b882df4735823eae181498786e62dd`  
		Last Modified: Wed, 07 Jul 2021 03:23:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:def02210305c7940addd2f5e26e8417017a2f2ae11116ee001b8f2a7bcb17bff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20941bb671159cef8cb5d6b9047f5c6c298a495274b06f9c6d9278ea5f9e5a1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:38:20 GMT
COPY file:a259b6f87cc2d22082524e5ba23201057e836734749f0d28676e8637d920d385 in /nats-server 
# Wed, 07 Jul 2021 06:38:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:38:21 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:38:22 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:38:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:434fc0c4a6c5daa82c731102728bcac575b5a312862a89edf401b0305d2efc82`  
		Last Modified: Wed, 07 Jul 2021 06:40:42 GMT  
		Size: 4.0 MB (3992410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c195f08925b050ce566763c31c813f3d8c7e1ba40bc4ccdf0949cb87373c3a43`  
		Last Modified: Wed, 07 Jul 2021 06:40:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:173c1afbfe6375d1f5670d632776a2132a1162d63517b952247a24e276bf1cdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4271d9d9d24a753bd371794f03c2c998e68346939612c8fd4c4c87ce372beb7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:ca5c64a22cab87809781278f49e476ff3d7d60b6d6d543ec243ed60a38654388 in /nats-server 
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:47:25 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:47:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:47:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c79949c52fa3b392514bb25b934eddd3777757b19d9389238626e96a6a3a243`  
		Last Modified: Wed, 07 Jul 2021 06:48:50 GMT  
		Size: 4.0 MB (3960542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0d08b9515c574d6baae1ae28b5767b4dd1a3ef4fec706cd0441f08497c619`  
		Last Modified: Wed, 07 Jul 2021 06:48:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.2-nanoserver`

```console
$ docker pull nats@sha256:5a0efd0e8d161d797c966f6e269a09b2c527a6761d49314012f29ac83654b1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:2.3.2-nanoserver` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:78a502a4470119b5ccf89f143feb35c164329288904ca0a2733b5331ec765ca8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107131765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479dee98537cc4a38350f37c146d6779bb0ae71a188e169fa838fc485e3016d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:35:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:28 GMT
RUN cmd /S /C #(nop) COPY file:573109625f0f6f957389174434c1f89cbff70ddfa1fa88ec82d3bbcc17b55fc0 in C:\nats-server.exe 
# Wed, 14 Jul 2021 02:35:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec20c4c9f6fa5e782e09342d50033ef24c4049a9dad1befd33c96759b71da6de`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54da7510a4c6639da510b1b1d4ef3c60875b1c401117b4caa1de1831db9e316`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 4.4 MB (4399677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa421afe026b6d93c2ee9b799feca2b86512c2c5a2e69c58eb68808dd7fd6`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.8 KB (1776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fbe77295342d38688cb0f7212e9ee70e7fc78dfa739e6fcd3d2c774b7d77`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09913e0e2081a0b9559e8643c36d52e8a63b692308f7b08310c99502f845bc`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f9e3c1e074debc991926ff6a6674e615ff31c36080c4fa5f6e2d1150f357`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.2-nanoserver-1809`

```console
$ docker pull nats@sha256:5a0efd0e8d161d797c966f6e269a09b2c527a6761d49314012f29ac83654b1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:2.3.2-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:78a502a4470119b5ccf89f143feb35c164329288904ca0a2733b5331ec765ca8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107131765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479dee98537cc4a38350f37c146d6779bb0ae71a188e169fa838fc485e3016d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:35:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:28 GMT
RUN cmd /S /C #(nop) COPY file:573109625f0f6f957389174434c1f89cbff70ddfa1fa88ec82d3bbcc17b55fc0 in C:\nats-server.exe 
# Wed, 14 Jul 2021 02:35:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec20c4c9f6fa5e782e09342d50033ef24c4049a9dad1befd33c96759b71da6de`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54da7510a4c6639da510b1b1d4ef3c60875b1c401117b4caa1de1831db9e316`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 4.4 MB (4399677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa421afe026b6d93c2ee9b799feca2b86512c2c5a2e69c58eb68808dd7fd6`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.8 KB (1776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fbe77295342d38688cb0f7212e9ee70e7fc78dfa739e6fcd3d2c774b7d77`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09913e0e2081a0b9559e8643c36d52e8a63b692308f7b08310c99502f845bc`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f9e3c1e074debc991926ff6a6674e615ff31c36080c4fa5f6e2d1150f357`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.2-scratch`

```console
$ docker pull nats@sha256:0af0863d42cecaaf08f44e31a170fe6a0d640ed1980f2979e09863167ea5c5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.3.2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:da01747b3b1b793d26f23d641b1e96439c8a4a7e06f996382ad5a588b3f22e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72641b68d54bc7007ad321eb3eab0f114b2744342ca010c87f647f84c0b86bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:697b18ad11c92732a089bd820afbe690cc8392744bc144a4dd94fd2d25aba511 in /nats-server 
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 00:20:42 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 00:20:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:411fd8300ee124a1c5d0cc25aaede18c5e3b9fcf63ad8db3e23a2a589145d0a0`  
		Last Modified: Wed, 07 Jul 2021 00:21:35 GMT  
		Size: 4.3 MB (4338149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214f5e8798288f091409c5b65e7d796a10e7924cb3aab9f85ea83d1837dca61`  
		Last Modified: Wed, 07 Jul 2021 00:21:34 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:11d953a654ef8984c4a9d2a827f11e5eed4a915f05dde024747634b3936c2949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1823a5f86be207fedbb468235bfd36c4b4b33de712c7d197b20c4b867cc10b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 03:21:12 GMT
COPY file:d4fbcc1923412df19a9fc206b745d07fe40999759232f3707f975a3195904bce in /nats-server 
# Wed, 07 Jul 2021 03:21:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 03:21:14 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 03:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 03:21:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ecb7ed08cb4eadf3cb26a4e7eb5c842903e149b620335c14815b4802f4ef67e`  
		Last Modified: Wed, 07 Jul 2021 03:23:40 GMT  
		Size: 4.0 MB (3997302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744553c17d9fabfcec8a7f1d9e4bd2d190b882df4735823eae181498786e62dd`  
		Last Modified: Wed, 07 Jul 2021 03:23:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:def02210305c7940addd2f5e26e8417017a2f2ae11116ee001b8f2a7bcb17bff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20941bb671159cef8cb5d6b9047f5c6c298a495274b06f9c6d9278ea5f9e5a1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:38:20 GMT
COPY file:a259b6f87cc2d22082524e5ba23201057e836734749f0d28676e8637d920d385 in /nats-server 
# Wed, 07 Jul 2021 06:38:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:38:21 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:38:22 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:38:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:434fc0c4a6c5daa82c731102728bcac575b5a312862a89edf401b0305d2efc82`  
		Last Modified: Wed, 07 Jul 2021 06:40:42 GMT  
		Size: 4.0 MB (3992410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c195f08925b050ce566763c31c813f3d8c7e1ba40bc4ccdf0949cb87373c3a43`  
		Last Modified: Wed, 07 Jul 2021 06:40:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:173c1afbfe6375d1f5670d632776a2132a1162d63517b952247a24e276bf1cdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4271d9d9d24a753bd371794f03c2c998e68346939612c8fd4c4c87ce372beb7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:ca5c64a22cab87809781278f49e476ff3d7d60b6d6d543ec243ed60a38654388 in /nats-server 
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:47:25 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:47:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:47:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c79949c52fa3b392514bb25b934eddd3777757b19d9389238626e96a6a3a243`  
		Last Modified: Wed, 07 Jul 2021 06:48:50 GMT  
		Size: 4.0 MB (3960542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0d08b9515c574d6baae1ae28b5767b4dd1a3ef4fec706cd0441f08497c619`  
		Last Modified: Wed, 07 Jul 2021 06:48:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.2-windowsservercore`

```console
$ docker pull nats@sha256:0b8e165d4355d79cc830cad2c312463d6c6b26fb861b5d51a4f2e98df4592627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2061; amd64
	-	windows version 10.0.14393.4530; amd64

### `nats:2.3.2-windowsservercore` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:ca5887b3ce3a2738a0cfef1b4fd7cef529463530fa913d9a5475dae6f42b4ab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2690560697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b4597deddc6fd13552dd1047dafd05cec22dcbad1a8b9cc530ec01c876e72`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 01:07:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:31:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:31:29 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:31:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:31:35 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:33:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:34:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:34:57 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:00 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:adcec6ff907307155c0652222cc9b95a0cc964d4c371e02767e72a5c90472192`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92bdc410321db22d4cf09322869bd9fb2495788c3725624c86d76a6ab3d95d3`  
		Last Modified: Wed, 14 Jul 2021 02:40:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd169b67bc0adfc5e8226697e4b07a433d05f84e1f7980b215d9126986ac8c4a`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695a1183c47a024177260d6b0f7eff188406b4ab73009e842467f74341644a3`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf9174b261ac8925172304e0ac5ec195d9c6dffe5af096c1ed7184e214a5f13`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98392ef89b669613db784f731fccf1528b34957595fb1c683d489bd5761413c`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 360.2 KB (360240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db372963a1fbdd84f209e09c63d416d5a046688eac3586747db505d4aa5c5034`  
		Last Modified: Wed, 14 Jul 2021 02:40:17 GMT  
		Size: 4.7 MB (4740427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beaa69f0b720b237e52da8c8fe32c34a1f02bae8dcd52a610c9fbb01534c70a`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4ff7071a01299a4c43612bdcc5bf06555b7d0ed7e93f9aa5a043eda5d00102`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1a64510bb6ae1abc9697871026362c0c6481cc9f0c3c547fada800dcdb72c0`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0d00003e8fcfea5412c43907e3ed19bd73d18b392b24ed5607642abea515a8`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.3.2-windowsservercore` - windows version 10.0.14393.4530; amd64

```console
$ docker pull nats@sha256:491f727092d1f1cc50faa02fa4b0c23d1dec175367f55291964468853737ab05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6279205071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fec2ab6a3510ab48fb94d8e3122a4055cca848ef1c6e2560c443fc31346f2d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 01:14:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:35:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:51 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:35:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:35:57 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:37:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:39:29 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:39:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:39:35 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:39:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:39:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fed351b78c876c55ec9c7e75d3b9d1b146c5c5dfeb4b5480c0a7c384322df98c`  
		Last Modified: Wed, 14 Jul 2021 02:03:37 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf08cae8b8db8f3f89e1a9192d393f2da55b44efce4e778fdb58debe2d608275`  
		Last Modified: Wed, 14 Jul 2021 02:40:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301246d6a689a00ca80c879c7036294c7c08f9628a3f7e143d00600f5fae9a2`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1135fddfb2a7acb97ec630ed1c2c9c9f7c53cdc995ae9ce746a18b8b67463f17`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c522e9c4ef7e0c5d6366bc22e9dd4ccd99d4e97501eec8ee9d83a0584f452e6`  
		Last Modified: Wed, 14 Jul 2021 02:40:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f11d018be60739ca143906be9e8a5d7833e083c9e76f9b4c5ad679dd62e546`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 325.3 KB (325309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef654d127a05fa7be2581174b3af9056cd84a24b53d639b29790480363fd13a`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 9.2 MB (9235231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62edb8d00046240ed89b64b658216821381a04ad85d9e93148a87633dceebad`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af7ff0ca1393713d4ada7de795553fe6e3ba4c1eb050652a87f27fc1cc293fb`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034662c21f82b31e87a354b8351637cedaeae62586649149d223908bd4c06b62`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07aed375d2f1ee02071c44422a10de0afa5fa38501cb09fa40125ad504ad6bd8`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.2-windowsservercore-1809`

```console
$ docker pull nats@sha256:de456b6d65e1ee5c7a2a23ed3122872764275185e5f749034e065b1e9cdb1ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:2.3.2-windowsservercore-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:ca5887b3ce3a2738a0cfef1b4fd7cef529463530fa913d9a5475dae6f42b4ab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2690560697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b4597deddc6fd13552dd1047dafd05cec22dcbad1a8b9cc530ec01c876e72`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 01:07:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:31:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:31:29 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:31:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:31:35 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:33:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:34:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:34:57 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:00 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:adcec6ff907307155c0652222cc9b95a0cc964d4c371e02767e72a5c90472192`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92bdc410321db22d4cf09322869bd9fb2495788c3725624c86d76a6ab3d95d3`  
		Last Modified: Wed, 14 Jul 2021 02:40:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd169b67bc0adfc5e8226697e4b07a433d05f84e1f7980b215d9126986ac8c4a`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695a1183c47a024177260d6b0f7eff188406b4ab73009e842467f74341644a3`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf9174b261ac8925172304e0ac5ec195d9c6dffe5af096c1ed7184e214a5f13`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98392ef89b669613db784f731fccf1528b34957595fb1c683d489bd5761413c`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 360.2 KB (360240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db372963a1fbdd84f209e09c63d416d5a046688eac3586747db505d4aa5c5034`  
		Last Modified: Wed, 14 Jul 2021 02:40:17 GMT  
		Size: 4.7 MB (4740427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beaa69f0b720b237e52da8c8fe32c34a1f02bae8dcd52a610c9fbb01534c70a`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4ff7071a01299a4c43612bdcc5bf06555b7d0ed7e93f9aa5a043eda5d00102`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1a64510bb6ae1abc9697871026362c0c6481cc9f0c3c547fada800dcdb72c0`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0d00003e8fcfea5412c43907e3ed19bd73d18b392b24ed5607642abea515a8`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.3.2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b192069a4cfd70392063967b2ce1090d6f8a094812fa4be622ffa35843463560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4530; amd64

### `nats:2.3.2-windowsservercore-ltsc2016` - windows version 10.0.14393.4530; amd64

```console
$ docker pull nats@sha256:491f727092d1f1cc50faa02fa4b0c23d1dec175367f55291964468853737ab05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6279205071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fec2ab6a3510ab48fb94d8e3122a4055cca848ef1c6e2560c443fc31346f2d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 01:14:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:35:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:51 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:35:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:35:57 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:37:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:39:29 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:39:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:39:35 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:39:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:39:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fed351b78c876c55ec9c7e75d3b9d1b146c5c5dfeb4b5480c0a7c384322df98c`  
		Last Modified: Wed, 14 Jul 2021 02:03:37 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf08cae8b8db8f3f89e1a9192d393f2da55b44efce4e778fdb58debe2d608275`  
		Last Modified: Wed, 14 Jul 2021 02:40:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301246d6a689a00ca80c879c7036294c7c08f9628a3f7e143d00600f5fae9a2`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1135fddfb2a7acb97ec630ed1c2c9c9f7c53cdc995ae9ce746a18b8b67463f17`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c522e9c4ef7e0c5d6366bc22e9dd4ccd99d4e97501eec8ee9d83a0584f452e6`  
		Last Modified: Wed, 14 Jul 2021 02:40:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f11d018be60739ca143906be9e8a5d7833e083c9e76f9b4c5ad679dd62e546`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 325.3 KB (325309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef654d127a05fa7be2581174b3af9056cd84a24b53d639b29790480363fd13a`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 9.2 MB (9235231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62edb8d00046240ed89b64b658216821381a04ad85d9e93148a87633dceebad`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af7ff0ca1393713d4ada7de795553fe6e3ba4c1eb050652a87f27fc1cc293fb`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034662c21f82b31e87a354b8351637cedaeae62586649149d223908bd4c06b62`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07aed375d2f1ee02071c44422a10de0afa5fa38501cb09fa40125ad504ad6bd8`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:311b5c6c40288203dc4e3281b4a9b3c4a6cac4f3383dd8da40e6a546e5d8e884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:3c2b7ad7052fdc5f13e360dc9b3e3513997b071ec008bd61d3bff3e862c1947a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49258f52dfceee0babf527ce8158ba3f98a998fa6ff73f8dc05dc67ec2c7a96e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 00:20:14 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 00:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 00:20:18 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 00:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be4d9f8cb68409d6fb7407ab14ce49d214464c023f641670bfdefab42009a4`  
		Last Modified: Wed, 07 Jul 2021 00:21:10 GMT  
		Size: 4.6 MB (4621729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee574d4f4017f32800275aeefde40b62872bca2876fe91025cdc68dd97f0d8c7`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d9cc62817a68bf383b92f18b776f88224028a2c6e33c8df4dcad380c76ec52`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:4847b1671080a6caad7803cf200ced965db8767cc9bf2074acbb47c8af4285a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6904326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e2558ac7efdda215c5835a53e89fbbed3cbf5663aa449620393561fb6c4371`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:42 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Fri, 30 Jul 2021 17:49:42 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:37:00 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 02:37:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 02:37:06 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 02:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 02:37:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59232f7a71e570822a9e6fb2265a241076b0256fcc9b0922b6e2f6872bd59ab`  
		Last Modified: Sat, 31 Jul 2021 02:39:09 GMT  
		Size: 4.3 MB (4278973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed212fd4c3d3aae796a3e81594b3919840f408ea96c0732151264bf34f2e06a0`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10863bd3a6e18b15368401690e36adf17ea3f7e91b7f4213e0b57bd0680dbeb`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:0cd94d122e5dd418d4d447257c6622e13c1d86149c0e7979057664951ab5a020
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6703143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5635c4604b79a25fc3fdf3ccf6606d69eb347b3e8a3cb756dd261e2ca83e780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 03:13:57 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 03:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 03:14:04 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 03:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 03:14:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0b8bfe79fe7add5c0f3af812a506d01cc94a574cd58ba1f81146318d3638c`  
		Last Modified: Sat, 31 Jul 2021 03:16:43 GMT  
		Size: 4.3 MB (4274251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35ac8f58b7f43ebc215a5713841cf5a94983b092019cf46da7ce8a3c9c84146`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735e5b5c342cb95f3f2eb33812321a4305479b159555d6fed062e4bb2880dc66`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:deaf6d647392081aca4583994c636c08933207d39db66c3f1c95b819b22b6b5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3354f4f30fd9160606507f59e9f0408338ff23f522fe71627defa8faa9793c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 06:46:50 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 06:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 06:46:54 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:46:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 06:46:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466aa348560edb5133af08a0f1c6913f1e859d87ac4efe59f2d0caa58c3a2b27`  
		Last Modified: Wed, 07 Jul 2021 06:48:18 GMT  
		Size: 4.2 MB (4244306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf9efaff12ffb1bc52633008fbb1ea048542934bc23331770580cf3e81ba97e`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674feaf82840d440dfb9812d17bd6603ff1bb7bbd1bc6a191ce7b456ed497839`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.14`

```console
$ docker pull nats@sha256:311b5c6c40288203dc4e3281b4a9b3c4a6cac4f3383dd8da40e6a546e5d8e884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:3c2b7ad7052fdc5f13e360dc9b3e3513997b071ec008bd61d3bff3e862c1947a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49258f52dfceee0babf527ce8158ba3f98a998fa6ff73f8dc05dc67ec2c7a96e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 00:20:14 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 00:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 00:20:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 00:20:18 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 00:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45be4d9f8cb68409d6fb7407ab14ce49d214464c023f641670bfdefab42009a4`  
		Last Modified: Wed, 07 Jul 2021 00:21:10 GMT  
		Size: 4.6 MB (4621729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee574d4f4017f32800275aeefde40b62872bca2876fe91025cdc68dd97f0d8c7`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d9cc62817a68bf383b92f18b776f88224028a2c6e33c8df4dcad380c76ec52`  
		Last Modified: Wed, 07 Jul 2021 00:21:09 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:4847b1671080a6caad7803cf200ced965db8767cc9bf2074acbb47c8af4285a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6904326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e2558ac7efdda215c5835a53e89fbbed3cbf5663aa449620393561fb6c4371`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:42 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Fri, 30 Jul 2021 17:49:42 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:37:00 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 02:37:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 02:37:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 02:37:06 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 02:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 02:37:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59232f7a71e570822a9e6fb2265a241076b0256fcc9b0922b6e2f6872bd59ab`  
		Last Modified: Sat, 31 Jul 2021 02:39:09 GMT  
		Size: 4.3 MB (4278973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed212fd4c3d3aae796a3e81594b3919840f408ea96c0732151264bf34f2e06a0`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10863bd3a6e18b15368401690e36adf17ea3f7e91b7f4213e0b57bd0680dbeb`  
		Last Modified: Sat, 31 Jul 2021 02:39:06 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:0cd94d122e5dd418d4d447257c6622e13c1d86149c0e7979057664951ab5a020
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6703143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5635c4604b79a25fc3fdf3ccf6606d69eb347b3e8a3cb756dd261e2ca83e780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 03:13:57 GMT
ENV NATS_SERVER=2.3.2
# Sat, 31 Jul 2021 03:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 31 Jul 2021 03:14:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 31 Jul 2021 03:14:04 GMT
EXPOSE 4222 6222 8222
# Sat, 31 Jul 2021 03:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 03:14:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0b8bfe79fe7add5c0f3af812a506d01cc94a574cd58ba1f81146318d3638c`  
		Last Modified: Sat, 31 Jul 2021 03:16:43 GMT  
		Size: 4.3 MB (4274251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35ac8f58b7f43ebc215a5713841cf5a94983b092019cf46da7ce8a3c9c84146`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735e5b5c342cb95f3f2eb33812321a4305479b159555d6fed062e4bb2880dc66`  
		Last Modified: Sat, 31 Jul 2021 03:16:40 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:deaf6d647392081aca4583994c636c08933207d39db66c3f1c95b819b22b6b5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3354f4f30fd9160606507f59e9f0408338ff23f522fe71627defa8faa9793c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 07 Jul 2021 06:46:50 GMT
ENV NATS_SERVER=2.3.2
# Wed, 07 Jul 2021 06:46:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='18a68cbef5c7a41052f5281bdfe9164b51cbeb60ce2dd31a7945c5adbcd39c2d' ;; 		armhf) natsArch='arm6'; sha256='a37949f8a1e24d5a8e47f57786e126205de7c3f6f8b3e5b849f33adbcfe8d2fb' ;; 		armv7) natsArch='arm7'; sha256='43a4820a57161b83fe721b81098d2ba9b1e2f42923be898f031bac40279f8f6e' ;; 		x86_64) natsArch='amd64'; sha256='6e6fdf781465fbf09cb024112b34ae6b2b432d94a5fc8b62f6ebf0da5fc3345d' ;; 		x86) natsArch='386'; sha256='c7c0ea9a5343925f0f5e2dda964946152382b0a3e0db96aa43c3f2ab17a37bf0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 07 Jul 2021 06:46:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 07 Jul 2021 06:46:54 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:46:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Jul 2021 06:46:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466aa348560edb5133af08a0f1c6913f1e859d87ac4efe59f2d0caa58c3a2b27`  
		Last Modified: Wed, 07 Jul 2021 06:48:18 GMT  
		Size: 4.2 MB (4244306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf9efaff12ffb1bc52633008fbb1ea048542934bc23331770580cf3e81ba97e`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674feaf82840d440dfb9812d17bd6603ff1bb7bbd1bc6a191ce7b456ed497839`  
		Last Modified: Wed, 07 Jul 2021 06:48:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:a22f80da6194bad3f89acb878d319d07bef10f6ea86c00c88721e96b45df7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2061; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:da01747b3b1b793d26f23d641b1e96439c8a4a7e06f996382ad5a588b3f22e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72641b68d54bc7007ad321eb3eab0f114b2744342ca010c87f647f84c0b86bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:697b18ad11c92732a089bd820afbe690cc8392744bc144a4dd94fd2d25aba511 in /nats-server 
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 00:20:42 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 00:20:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:411fd8300ee124a1c5d0cc25aaede18c5e3b9fcf63ad8db3e23a2a589145d0a0`  
		Last Modified: Wed, 07 Jul 2021 00:21:35 GMT  
		Size: 4.3 MB (4338149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214f5e8798288f091409c5b65e7d796a10e7924cb3aab9f85ea83d1837dca61`  
		Last Modified: Wed, 07 Jul 2021 00:21:34 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:11d953a654ef8984c4a9d2a827f11e5eed4a915f05dde024747634b3936c2949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1823a5f86be207fedbb468235bfd36c4b4b33de712c7d197b20c4b867cc10b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 03:21:12 GMT
COPY file:d4fbcc1923412df19a9fc206b745d07fe40999759232f3707f975a3195904bce in /nats-server 
# Wed, 07 Jul 2021 03:21:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 03:21:14 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 03:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 03:21:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ecb7ed08cb4eadf3cb26a4e7eb5c842903e149b620335c14815b4802f4ef67e`  
		Last Modified: Wed, 07 Jul 2021 03:23:40 GMT  
		Size: 4.0 MB (3997302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744553c17d9fabfcec8a7f1d9e4bd2d190b882df4735823eae181498786e62dd`  
		Last Modified: Wed, 07 Jul 2021 03:23:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:def02210305c7940addd2f5e26e8417017a2f2ae11116ee001b8f2a7bcb17bff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20941bb671159cef8cb5d6b9047f5c6c298a495274b06f9c6d9278ea5f9e5a1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:38:20 GMT
COPY file:a259b6f87cc2d22082524e5ba23201057e836734749f0d28676e8637d920d385 in /nats-server 
# Wed, 07 Jul 2021 06:38:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:38:21 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:38:22 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:38:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:434fc0c4a6c5daa82c731102728bcac575b5a312862a89edf401b0305d2efc82`  
		Last Modified: Wed, 07 Jul 2021 06:40:42 GMT  
		Size: 4.0 MB (3992410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c195f08925b050ce566763c31c813f3d8c7e1ba40bc4ccdf0949cb87373c3a43`  
		Last Modified: Wed, 07 Jul 2021 06:40:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:173c1afbfe6375d1f5670d632776a2132a1162d63517b952247a24e276bf1cdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4271d9d9d24a753bd371794f03c2c998e68346939612c8fd4c4c87ce372beb7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:ca5c64a22cab87809781278f49e476ff3d7d60b6d6d543ec243ed60a38654388 in /nats-server 
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:47:25 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:47:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:47:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c79949c52fa3b392514bb25b934eddd3777757b19d9389238626e96a6a3a243`  
		Last Modified: Wed, 07 Jul 2021 06:48:50 GMT  
		Size: 4.0 MB (3960542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0d08b9515c574d6baae1ae28b5767b4dd1a3ef4fec706cd0441f08497c619`  
		Last Modified: Wed, 07 Jul 2021 06:48:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:78a502a4470119b5ccf89f143feb35c164329288904ca0a2733b5331ec765ca8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107131765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479dee98537cc4a38350f37c146d6779bb0ae71a188e169fa838fc485e3016d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:35:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:28 GMT
RUN cmd /S /C #(nop) COPY file:573109625f0f6f957389174434c1f89cbff70ddfa1fa88ec82d3bbcc17b55fc0 in C:\nats-server.exe 
# Wed, 14 Jul 2021 02:35:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec20c4c9f6fa5e782e09342d50033ef24c4049a9dad1befd33c96759b71da6de`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54da7510a4c6639da510b1b1d4ef3c60875b1c401117b4caa1de1831db9e316`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 4.4 MB (4399677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa421afe026b6d93c2ee9b799feca2b86512c2c5a2e69c58eb68808dd7fd6`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.8 KB (1776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fbe77295342d38688cb0f7212e9ee70e7fc78dfa739e6fcd3d2c774b7d77`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09913e0e2081a0b9559e8643c36d52e8a63b692308f7b08310c99502f845bc`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f9e3c1e074debc991926ff6a6674e615ff31c36080c4fa5f6e2d1150f357`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:0af0863d42cecaaf08f44e31a170fe6a0d640ed1980f2979e09863167ea5c5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:da01747b3b1b793d26f23d641b1e96439c8a4a7e06f996382ad5a588b3f22e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72641b68d54bc7007ad321eb3eab0f114b2744342ca010c87f647f84c0b86bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:697b18ad11c92732a089bd820afbe690cc8392744bc144a4dd94fd2d25aba511 in /nats-server 
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 00:20:42 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 00:20:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:411fd8300ee124a1c5d0cc25aaede18c5e3b9fcf63ad8db3e23a2a589145d0a0`  
		Last Modified: Wed, 07 Jul 2021 00:21:35 GMT  
		Size: 4.3 MB (4338149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214f5e8798288f091409c5b65e7d796a10e7924cb3aab9f85ea83d1837dca61`  
		Last Modified: Wed, 07 Jul 2021 00:21:34 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:11d953a654ef8984c4a9d2a827f11e5eed4a915f05dde024747634b3936c2949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1823a5f86be207fedbb468235bfd36c4b4b33de712c7d197b20c4b867cc10b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 03:21:12 GMT
COPY file:d4fbcc1923412df19a9fc206b745d07fe40999759232f3707f975a3195904bce in /nats-server 
# Wed, 07 Jul 2021 03:21:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 03:21:14 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 03:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 03:21:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ecb7ed08cb4eadf3cb26a4e7eb5c842903e149b620335c14815b4802f4ef67e`  
		Last Modified: Wed, 07 Jul 2021 03:23:40 GMT  
		Size: 4.0 MB (3997302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744553c17d9fabfcec8a7f1d9e4bd2d190b882df4735823eae181498786e62dd`  
		Last Modified: Wed, 07 Jul 2021 03:23:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:def02210305c7940addd2f5e26e8417017a2f2ae11116ee001b8f2a7bcb17bff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20941bb671159cef8cb5d6b9047f5c6c298a495274b06f9c6d9278ea5f9e5a1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:38:20 GMT
COPY file:a259b6f87cc2d22082524e5ba23201057e836734749f0d28676e8637d920d385 in /nats-server 
# Wed, 07 Jul 2021 06:38:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:38:21 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:38:22 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:38:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:434fc0c4a6c5daa82c731102728bcac575b5a312862a89edf401b0305d2efc82`  
		Last Modified: Wed, 07 Jul 2021 06:40:42 GMT  
		Size: 4.0 MB (3992410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c195f08925b050ce566763c31c813f3d8c7e1ba40bc4ccdf0949cb87373c3a43`  
		Last Modified: Wed, 07 Jul 2021 06:40:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:173c1afbfe6375d1f5670d632776a2132a1162d63517b952247a24e276bf1cdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4271d9d9d24a753bd371794f03c2c998e68346939612c8fd4c4c87ce372beb7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:ca5c64a22cab87809781278f49e476ff3d7d60b6d6d543ec243ed60a38654388 in /nats-server 
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:47:25 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:47:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:47:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c79949c52fa3b392514bb25b934eddd3777757b19d9389238626e96a6a3a243`  
		Last Modified: Wed, 07 Jul 2021 06:48:50 GMT  
		Size: 4.0 MB (3960542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0d08b9515c574d6baae1ae28b5767b4dd1a3ef4fec706cd0441f08497c619`  
		Last Modified: Wed, 07 Jul 2021 06:48:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:5a0efd0e8d161d797c966f6e269a09b2c527a6761d49314012f29ac83654b1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:nanoserver` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:78a502a4470119b5ccf89f143feb35c164329288904ca0a2733b5331ec765ca8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107131765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479dee98537cc4a38350f37c146d6779bb0ae71a188e169fa838fc485e3016d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:35:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:28 GMT
RUN cmd /S /C #(nop) COPY file:573109625f0f6f957389174434c1f89cbff70ddfa1fa88ec82d3bbcc17b55fc0 in C:\nats-server.exe 
# Wed, 14 Jul 2021 02:35:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec20c4c9f6fa5e782e09342d50033ef24c4049a9dad1befd33c96759b71da6de`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54da7510a4c6639da510b1b1d4ef3c60875b1c401117b4caa1de1831db9e316`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 4.4 MB (4399677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa421afe026b6d93c2ee9b799feca2b86512c2c5a2e69c58eb68808dd7fd6`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.8 KB (1776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fbe77295342d38688cb0f7212e9ee70e7fc78dfa739e6fcd3d2c774b7d77`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09913e0e2081a0b9559e8643c36d52e8a63b692308f7b08310c99502f845bc`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f9e3c1e074debc991926ff6a6674e615ff31c36080c4fa5f6e2d1150f357`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:5a0efd0e8d161d797c966f6e269a09b2c527a6761d49314012f29ac83654b1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:78a502a4470119b5ccf89f143feb35c164329288904ca0a2733b5331ec765ca8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107131765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479dee98537cc4a38350f37c146d6779bb0ae71a188e169fa838fc485e3016d0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:35:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:28 GMT
RUN cmd /S /C #(nop) COPY file:573109625f0f6f957389174434c1f89cbff70ddfa1fa88ec82d3bbcc17b55fc0 in C:\nats-server.exe 
# Wed, 14 Jul 2021 02:35:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:39 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec20c4c9f6fa5e782e09342d50033ef24c4049a9dad1befd33c96759b71da6de`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54da7510a4c6639da510b1b1d4ef3c60875b1c401117b4caa1de1831db9e316`  
		Last Modified: Wed, 14 Jul 2021 02:40:36 GMT  
		Size: 4.4 MB (4399677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa421afe026b6d93c2ee9b799feca2b86512c2c5a2e69c58eb68808dd7fd6`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.8 KB (1776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fbe77295342d38688cb0f7212e9ee70e7fc78dfa739e6fcd3d2c774b7d77`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09913e0e2081a0b9559e8643c36d52e8a63b692308f7b08310c99502f845bc`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3898f9e3c1e074debc991926ff6a6674e615ff31c36080c4fa5f6e2d1150f357`  
		Last Modified: Wed, 14 Jul 2021 02:40:34 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:0af0863d42cecaaf08f44e31a170fe6a0d640ed1980f2979e09863167ea5c5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:da01747b3b1b793d26f23d641b1e96439c8a4a7e06f996382ad5a588b3f22e9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72641b68d54bc7007ad321eb3eab0f114b2744342ca010c87f647f84c0b86bf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:697b18ad11c92732a089bd820afbe690cc8392744bc144a4dd94fd2d25aba511 in /nats-server 
# Wed, 07 Jul 2021 00:20:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 00:20:42 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 00:20:43 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 00:20:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:411fd8300ee124a1c5d0cc25aaede18c5e3b9fcf63ad8db3e23a2a589145d0a0`  
		Last Modified: Wed, 07 Jul 2021 00:21:35 GMT  
		Size: 4.3 MB (4338149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214f5e8798288f091409c5b65e7d796a10e7924cb3aab9f85ea83d1837dca61`  
		Last Modified: Wed, 07 Jul 2021 00:21:34 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:11d953a654ef8984c4a9d2a827f11e5eed4a915f05dde024747634b3936c2949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1823a5f86be207fedbb468235bfd36c4b4b33de712c7d197b20c4b867cc10b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 03:21:12 GMT
COPY file:d4fbcc1923412df19a9fc206b745d07fe40999759232f3707f975a3195904bce in /nats-server 
# Wed, 07 Jul 2021 03:21:13 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 03:21:14 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 03:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 03:21:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ecb7ed08cb4eadf3cb26a4e7eb5c842903e149b620335c14815b4802f4ef67e`  
		Last Modified: Wed, 07 Jul 2021 03:23:40 GMT  
		Size: 4.0 MB (3997302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744553c17d9fabfcec8a7f1d9e4bd2d190b882df4735823eae181498786e62dd`  
		Last Modified: Wed, 07 Jul 2021 03:23:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:def02210305c7940addd2f5e26e8417017a2f2ae11116ee001b8f2a7bcb17bff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20941bb671159cef8cb5d6b9047f5c6c298a495274b06f9c6d9278ea5f9e5a1f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:38:20 GMT
COPY file:a259b6f87cc2d22082524e5ba23201057e836734749f0d28676e8637d920d385 in /nats-server 
# Wed, 07 Jul 2021 06:38:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:38:21 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:38:22 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:38:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:434fc0c4a6c5daa82c731102728bcac575b5a312862a89edf401b0305d2efc82`  
		Last Modified: Wed, 07 Jul 2021 06:40:42 GMT  
		Size: 4.0 MB (3992410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c195f08925b050ce566763c31c813f3d8c7e1ba40bc4ccdf0949cb87373c3a43`  
		Last Modified: Wed, 07 Jul 2021 06:40:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:173c1afbfe6375d1f5670d632776a2132a1162d63517b952247a24e276bf1cdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4271d9d9d24a753bd371794f03c2c998e68346939612c8fd4c4c87ce372beb7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:ca5c64a22cab87809781278f49e476ff3d7d60b6d6d543ec243ed60a38654388 in /nats-server 
# Wed, 07 Jul 2021 06:47:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 07 Jul 2021 06:47:25 GMT
EXPOSE 4222 6222 8222
# Wed, 07 Jul 2021 06:47:26 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 07 Jul 2021 06:47:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c79949c52fa3b392514bb25b934eddd3777757b19d9389238626e96a6a3a243`  
		Last Modified: Wed, 07 Jul 2021 06:48:50 GMT  
		Size: 4.0 MB (3960542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0d08b9515c574d6baae1ae28b5767b4dd1a3ef4fec706cd0441f08497c619`  
		Last Modified: Wed, 07 Jul 2021 06:48:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:0b8e165d4355d79cc830cad2c312463d6c6b26fb861b5d51a4f2e98df4592627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2061; amd64
	-	windows version 10.0.14393.4530; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:ca5887b3ce3a2738a0cfef1b4fd7cef529463530fa913d9a5475dae6f42b4ab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2690560697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b4597deddc6fd13552dd1047dafd05cec22dcbad1a8b9cc530ec01c876e72`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 01:07:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:31:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:31:29 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:31:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:31:35 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:33:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:34:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:34:57 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:00 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:adcec6ff907307155c0652222cc9b95a0cc964d4c371e02767e72a5c90472192`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92bdc410321db22d4cf09322869bd9fb2495788c3725624c86d76a6ab3d95d3`  
		Last Modified: Wed, 14 Jul 2021 02:40:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd169b67bc0adfc5e8226697e4b07a433d05f84e1f7980b215d9126986ac8c4a`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695a1183c47a024177260d6b0f7eff188406b4ab73009e842467f74341644a3`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf9174b261ac8925172304e0ac5ec195d9c6dffe5af096c1ed7184e214a5f13`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98392ef89b669613db784f731fccf1528b34957595fb1c683d489bd5761413c`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 360.2 KB (360240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db372963a1fbdd84f209e09c63d416d5a046688eac3586747db505d4aa5c5034`  
		Last Modified: Wed, 14 Jul 2021 02:40:17 GMT  
		Size: 4.7 MB (4740427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beaa69f0b720b237e52da8c8fe32c34a1f02bae8dcd52a610c9fbb01534c70a`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4ff7071a01299a4c43612bdcc5bf06555b7d0ed7e93f9aa5a043eda5d00102`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1a64510bb6ae1abc9697871026362c0c6481cc9f0c3c547fada800dcdb72c0`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0d00003e8fcfea5412c43907e3ed19bd73d18b392b24ed5607642abea515a8`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4530; amd64

```console
$ docker pull nats@sha256:491f727092d1f1cc50faa02fa4b0c23d1dec175367f55291964468853737ab05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6279205071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fec2ab6a3510ab48fb94d8e3122a4055cca848ef1c6e2560c443fc31346f2d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 01:14:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:35:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:51 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:35:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:35:57 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:37:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:39:29 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:39:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:39:35 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:39:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:39:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fed351b78c876c55ec9c7e75d3b9d1b146c5c5dfeb4b5480c0a7c384322df98c`  
		Last Modified: Wed, 14 Jul 2021 02:03:37 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf08cae8b8db8f3f89e1a9192d393f2da55b44efce4e778fdb58debe2d608275`  
		Last Modified: Wed, 14 Jul 2021 02:40:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301246d6a689a00ca80c879c7036294c7c08f9628a3f7e143d00600f5fae9a2`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1135fddfb2a7acb97ec630ed1c2c9c9f7c53cdc995ae9ce746a18b8b67463f17`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c522e9c4ef7e0c5d6366bc22e9dd4ccd99d4e97501eec8ee9d83a0584f452e6`  
		Last Modified: Wed, 14 Jul 2021 02:40:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f11d018be60739ca143906be9e8a5d7833e083c9e76f9b4c5ad679dd62e546`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 325.3 KB (325309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef654d127a05fa7be2581174b3af9056cd84a24b53d639b29790480363fd13a`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 9.2 MB (9235231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62edb8d00046240ed89b64b658216821381a04ad85d9e93148a87633dceebad`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af7ff0ca1393713d4ada7de795553fe6e3ba4c1eb050652a87f27fc1cc293fb`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034662c21f82b31e87a354b8351637cedaeae62586649149d223908bd4c06b62`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07aed375d2f1ee02071c44422a10de0afa5fa38501cb09fa40125ad504ad6bd8`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:de456b6d65e1ee5c7a2a23ed3122872764275185e5f749034e065b1e9cdb1ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull nats@sha256:ca5887b3ce3a2738a0cfef1b4fd7cef529463530fa913d9a5475dae6f42b4ab7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2690560697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b4597deddc6fd13552dd1047dafd05cec22dcbad1a8b9cc530ec01c876e72`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 01:07:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:31:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:31:29 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:31:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:31:35 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:33:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:34:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:34:57 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:35:00 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:35:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:35:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:adcec6ff907307155c0652222cc9b95a0cc964d4c371e02767e72a5c90472192`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92bdc410321db22d4cf09322869bd9fb2495788c3725624c86d76a6ab3d95d3`  
		Last Modified: Wed, 14 Jul 2021 02:40:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd169b67bc0adfc5e8226697e4b07a433d05f84e1f7980b215d9126986ac8c4a`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695a1183c47a024177260d6b0f7eff188406b4ab73009e842467f74341644a3`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf9174b261ac8925172304e0ac5ec195d9c6dffe5af096c1ed7184e214a5f13`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98392ef89b669613db784f731fccf1528b34957595fb1c683d489bd5761413c`  
		Last Modified: Wed, 14 Jul 2021 02:40:14 GMT  
		Size: 360.2 KB (360240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db372963a1fbdd84f209e09c63d416d5a046688eac3586747db505d4aa5c5034`  
		Last Modified: Wed, 14 Jul 2021 02:40:17 GMT  
		Size: 4.7 MB (4740427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beaa69f0b720b237e52da8c8fe32c34a1f02bae8dcd52a610c9fbb01534c70a`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4ff7071a01299a4c43612bdcc5bf06555b7d0ed7e93f9aa5a043eda5d00102`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1a64510bb6ae1abc9697871026362c0c6481cc9f0c3c547fada800dcdb72c0`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0d00003e8fcfea5412c43907e3ed19bd73d18b392b24ed5607642abea515a8`  
		Last Modified: Wed, 14 Jul 2021 02:40:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b192069a4cfd70392063967b2ce1090d6f8a094812fa4be622ffa35843463560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4530; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4530; amd64

```console
$ docker pull nats@sha256:491f727092d1f1cc50faa02fa4b0c23d1dec175367f55291964468853737ab05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6279205071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fec2ab6a3510ab48fb94d8e3122a4055cca848ef1c6e2560c443fc31346f2d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 01:14:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 02:35:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jul 2021 02:35:51 GMT
ENV NATS_SERVER=2.3.2
# Wed, 14 Jul 2021 02:35:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.2/nats-server-v2.3.2-windows-amd64.zip
# Wed, 14 Jul 2021 02:35:57 GMT
ENV NATS_SERVER_SHASUM=9278a3709c874f1dc5125fece7e7803e0cd4361cd97dc847826ef95838ea1e3e
# Wed, 14 Jul 2021 02:37:14 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jul 2021 02:39:29 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jul 2021 02:39:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 14 Jul 2021 02:39:35 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jul 2021 02:39:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jul 2021 02:39:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fed351b78c876c55ec9c7e75d3b9d1b146c5c5dfeb4b5480c0a7c384322df98c`  
		Last Modified: Wed, 14 Jul 2021 02:03:37 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf08cae8b8db8f3f89e1a9192d393f2da55b44efce4e778fdb58debe2d608275`  
		Last Modified: Wed, 14 Jul 2021 02:40:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301246d6a689a00ca80c879c7036294c7c08f9628a3f7e143d00600f5fae9a2`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1135fddfb2a7acb97ec630ed1c2c9c9f7c53cdc995ae9ce746a18b8b67463f17`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c522e9c4ef7e0c5d6366bc22e9dd4ccd99d4e97501eec8ee9d83a0584f452e6`  
		Last Modified: Wed, 14 Jul 2021 02:40:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f11d018be60739ca143906be9e8a5d7833e083c9e76f9b4c5ad679dd62e546`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 325.3 KB (325309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef654d127a05fa7be2581174b3af9056cd84a24b53d639b29790480363fd13a`  
		Last Modified: Wed, 14 Jul 2021 02:40:55 GMT  
		Size: 9.2 MB (9235231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62edb8d00046240ed89b64b658216821381a04ad85d9e93148a87633dceebad`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af7ff0ca1393713d4ada7de795553fe6e3ba4c1eb050652a87f27fc1cc293fb`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034662c21f82b31e87a354b8351637cedaeae62586649149d223908bd4c06b62`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07aed375d2f1ee02071c44422a10de0afa5fa38501cb09fa40125ad504ad6bd8`  
		Last Modified: Wed, 14 Jul 2021 02:40:52 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

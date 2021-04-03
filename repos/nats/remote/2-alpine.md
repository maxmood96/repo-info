## `nats:2-alpine`

```console
$ docker pull nats@sha256:f2104823b252f408a4e021715c6a020ebe27ce5d61e033c19cd66216e9e935a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:faf06335ff05259553a7cd85c508540576e73735f878f991bdb316639c5beba8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7278367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baae0ba3d35d13f1ab017cea5d7a4c34e55d533b5f83ee0887f4e46b9df6169d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:29:19 GMT
ENV NATS_SERVER=2.2.0
# Thu, 01 Apr 2021 14:29:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4dfcf480a32d9ba7098477387d96a657a036ef9ad495a008a83e06b22df63999' ;; 		armhf) natsArch='arm6'; sha256='b82fdb2c8f6e7c731254730043c145423b5c48a3b40e33ad6e32bce029a9f086' ;; 		armv7) natsArch='arm7'; sha256='cffc326c7faeb5ea0769d0f04787d9885d5b2baabd32000d3b18b1130742772e' ;; 		x86_64) natsArch='amd64'; sha256='764ee4a9761185f92904c21c3de204c8b898e9a6bad6afac8b1fe512ce887417' ;; 		x86) natsArch='386'; sha256='a8067d9f26007bed3df2a72eebd4a813035a473058db1451d615ef5e96b30577' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 01 Apr 2021 14:29:22 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 01 Apr 2021 14:29:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 01 Apr 2021 14:29:23 GMT
EXPOSE 4222 6222 8222
# Thu, 01 Apr 2021 14:29:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:29:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada4cf180db02bbf5a645d367b3c999bd2d866adfb6969b459025ab3a5f5865d`  
		Last Modified: Thu, 01 Apr 2021 14:29:59 GMT  
		Size: 4.5 MB (4465448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b817b47391bfd1cb047c312e74ba8c28ef3055a3f2610b6e1cac5fdb07d259`  
		Last Modified: Thu, 01 Apr 2021 14:29:59 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66852cd6a6ebc8a62018430b7b8048a2a6a6c95a33d89e73450ee3821b2eefb2`  
		Last Modified: Thu, 01 Apr 2021 14:29:58 GMT  
		Size: 413.0 B  
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
$ docker pull nats@sha256:0d0d69075781a3105d70b4607557c74d2c13430f137da5d4ad9b893ff47bbcc1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6560058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb0c3f1895fa95164aab25913ef37b6488bb4ef685b45fc7ea757d2028570cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 18:13:27 GMT
ADD file:56e92c06393237a87e0a1ff475e9c9dc80e897d69ec20f45359b587906da345b in / 
# Wed, 31 Mar 2021 18:13:31 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 09:52:30 GMT
ENV NATS_SERVER=2.2.0
# Thu, 01 Apr 2021 09:52:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4dfcf480a32d9ba7098477387d96a657a036ef9ad495a008a83e06b22df63999' ;; 		armhf) natsArch='arm6'; sha256='b82fdb2c8f6e7c731254730043c145423b5c48a3b40e33ad6e32bce029a9f086' ;; 		armv7) natsArch='arm7'; sha256='cffc326c7faeb5ea0769d0f04787d9885d5b2baabd32000d3b18b1130742772e' ;; 		x86_64) natsArch='amd64'; sha256='764ee4a9761185f92904c21c3de204c8b898e9a6bad6afac8b1fe512ce887417' ;; 		x86) natsArch='386'; sha256='a8067d9f26007bed3df2a72eebd4a813035a473058db1451d615ef5e96b30577' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 01 Apr 2021 09:52:36 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 01 Apr 2021 09:52:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 01 Apr 2021 09:52:37 GMT
EXPOSE 4222 6222 8222
# Thu, 01 Apr 2021 09:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 09:52:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:07389e51ea05e1c9a3cb0ef92d31181f2afa1e445207ad99ffd8a94d6d6af295`  
		Last Modified: Wed, 31 Mar 2021 18:14:57 GMT  
		Size: 2.4 MB (2424108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d72610fdeddca533a7fa8937e70712fae7aca0dcb07d6fbba1e43b20190fe8`  
		Last Modified: Thu, 01 Apr 2021 09:53:21 GMT  
		Size: 4.1 MB (4134981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12af5140a82cb853be34ad036db9ac6e67f64654816fb140706e62e9c49dec4`  
		Last Modified: Thu, 01 Apr 2021 09:53:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56601effdbab268d5f96f091e3ab569209092f832637c2f53712cdd0c4cb06e9`  
		Last Modified: Thu, 01 Apr 2021 09:53:20 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5e40ddf9a4d4f163f9f413a0a749d385b437a598d53ab8c462d21e6df734c97d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6822164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbc27f239e9627f70c924bbb76c70b230bfabe5e49e3a7d9df731e4f38f39a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:43:27 GMT
ENV NATS_SERVER=2.2.0
# Thu, 01 Apr 2021 13:43:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4dfcf480a32d9ba7098477387d96a657a036ef9ad495a008a83e06b22df63999' ;; 		armhf) natsArch='arm6'; sha256='b82fdb2c8f6e7c731254730043c145423b5c48a3b40e33ad6e32bce029a9f086' ;; 		armv7) natsArch='arm7'; sha256='cffc326c7faeb5ea0769d0f04787d9885d5b2baabd32000d3b18b1130742772e' ;; 		x86_64) natsArch='amd64'; sha256='764ee4a9761185f92904c21c3de204c8b898e9a6bad6afac8b1fe512ce887417' ;; 		x86) natsArch='386'; sha256='a8067d9f26007bed3df2a72eebd4a813035a473058db1451d615ef5e96b30577' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 01 Apr 2021 13:43:33 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 01 Apr 2021 13:43:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 01 Apr 2021 13:43:34 GMT
EXPOSE 4222 6222 8222
# Thu, 01 Apr 2021 13:43:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:43:36 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7065a6411f04b75bef4097e4ddf4951d84ad0bfe9c9d9552a92bf75a42c77bd9`  
		Last Modified: Thu, 01 Apr 2021 13:48:40 GMT  
		Size: 4.1 MB (4109274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db97b33cea8fa80f73c926008de131699a2fe7671dd699420d9c86a98a4c47a`  
		Last Modified: Thu, 01 Apr 2021 13:48:40 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c025cd8f41b22d6bda55a9235f10bf1751237ebff13e7ad89ed1325fbc9d86e2`  
		Last Modified: Thu, 01 Apr 2021 13:48:39 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

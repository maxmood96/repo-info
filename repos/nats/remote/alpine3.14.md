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

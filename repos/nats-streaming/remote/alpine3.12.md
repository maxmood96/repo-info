## `nats-streaming:alpine3.12`

```console
$ docker pull nats-streaming@sha256:5fb0383ced04d7e84dab475fe685f876705d419729f9469257026af6790b8f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:07e9ec26924214dd8e4f366251511fabc890e1b8ba37f1d74506c8a33c1cbc52
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6452416db7c1a60264a9c4d3b3f02c447ea078e951c14ee2b5d15db3523628`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:14:15 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Fri, 11 Dec 2020 05:14:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 11 Dec 2020 05:14:24 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 11 Dec 2020 05:14:26 GMT
EXPOSE 4222 8222
# Fri, 11 Dec 2020 05:14:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:14:29 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4775bb5a9ac47d892be5e5ebaea16d93247d5034bea3b043f273ccbf55bd2bd`  
		Last Modified: Fri, 11 Dec 2020 05:15:10 GMT  
		Size: 6.3 MB (6329913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f67a2f92965ea4e5871579ec878bd4d416b1352fc0b7f421a0a8fc30a9115d`  
		Last Modified: Fri, 11 Dec 2020 05:15:06 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:94d47e17958fa04b197d1d5fffa93135bfcad08f4602cb5c19fe0856e742a74c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4d10ac61333084353856c2ae8113b40511a7af00c7bed1a0d3631e442ad076`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 11 Dec 2020 02:20:33 GMT
ADD file:0e85952ec585d17378d9bb15a94ddc10c3ed8f766f275cf50fb36be1126f35d2 in / 
# Fri, 11 Dec 2020 02:20:34 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:08:56 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Fri, 11 Dec 2020 03:09:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 11 Dec 2020 03:09:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 11 Dec 2020 03:09:02 GMT
EXPOSE 4222 8222
# Fri, 11 Dec 2020 03:09:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 03:09:03 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f70c74f2e22556cebd0cbbff78c03d4f0560d76979bf799d67730340a639aa57`  
		Last Modified: Fri, 11 Dec 2020 02:21:18 GMT  
		Size: 2.4 MB (2405692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9882f91393d1d7307bade0ca7b48e562a1b079b03e1c516f1ff2003b83a5ce00`  
		Last Modified: Fri, 11 Dec 2020 03:09:37 GMT  
		Size: 6.3 MB (6324385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f79314a7ad747e7d1d653f6e767dbe5808c510e6947e3554549fc24c523a45`  
		Last Modified: Fri, 11 Dec 2020 03:09:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

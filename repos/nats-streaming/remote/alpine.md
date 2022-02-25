## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:6c06d99e350dfd64d6f90744011e606d51bde2f02fe0fbfdcaa0a7ee8105ad52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:e0b5c46db65c6031b96850c7750125ae972bacaf7acd500a342529587f78cdb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10163584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73fdc06ff9592dbaa07f7638b8ec5b77e29f0f50e5810e01addc1712d27b926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:19:43 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:19:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:19:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:19:46 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:19:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:19:46 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6d6be22662448ec27471291d386c2cf9e303b0c18135d61435ecab66e3d190`  
		Last Modified: Fri, 25 Feb 2022 02:20:17 GMT  
		Size: 7.3 MB (7344748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ef5642b30ec627703bbd9831a4eb2b34fbc32ce3af4c52751b3c13b05fa1f3`  
		Last Modified: Fri, 25 Feb 2022 02:20:16 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:16bfad93443d1e11ea456827a60788ffaaf287abd7a898abd66df24ce1973675
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9492160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7228f54cd28bbac00b2fd561e721cece5b97bdd93a8582be95db0a18ef521e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:53:26 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 02:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 02:53:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 02:53:32 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:53:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:53:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162bf98370c73025244b6844c0fb4795edd0cf2437d3ccedad11cf1e27309826`  
		Last Modified: Fri, 25 Feb 2022 02:55:14 GMT  
		Size: 6.9 MB (6860315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64992fd6ef19b0475e618937bb5276e19cb2e256048d14fefcd9ceea4334d758`  
		Last Modified: Fri, 25 Feb 2022 02:55:10 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:353aec3dccf8ecf1b39edab2415d3ea3c9281434ddf10db8c7a1f36df0be9f7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9285283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54087071c470d19a57112b054034098a0e6a491034a31578b6034a497fa0171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:55 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:01:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:02:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:02:00 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:02:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:02:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fa952029dc8a0c57ab16e41b9b4d9f7302794c501d3c481e6576062a23683e`  
		Last Modified: Fri, 25 Feb 2022 03:03:50 GMT  
		Size: 6.9 MB (6850097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360fe50d6904c4c5e840ab926f40c58df2a2e6b905c7493ae065c23b443f4188`  
		Last Modified: Fri, 25 Feb 2022 03:03:45 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2ee72ee2576a5cbbcc8b3cfb713c4f90292c80ec08ec0a3b156d8cd93c43de42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9484460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b04cc618c6bdfcbe7e945393204707f2b00244897ddafba37db190dbdac9854`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:03:39 GMT
ENV NATS_STREAMING_SERVER=0.24.2
# Fri, 25 Feb 2022 03:03:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8e64112ae12886aebb06422e587ebf89eecec6aef9e11a85e034b23f7ea4fba6' ;; 		armhf) natsArch='arm6'; sha256='1550060a4f076cb3be61a10ac41252449fb645dea09df2a5eea5ee1187f93beb' ;; 		armv7) natsArch='arm7'; sha256='29c5573fa8f1c196577d317494752496db9343b9d893db313ad3b7cc432c3480' ;; 		x86_64) natsArch='amd64'; sha256='1db336a63b6789142fde23d2d27e210ec618c018e6cc904af7533362888d01ec' ;; 		x86) natsArch='386'; sha256='819e4f7cb6bd408b9eab2ca193ec225aa5d48434ac1dddacd9642308e5cbdd1d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 25 Feb 2022 03:03:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 25 Feb 2022 03:03:45 GMT
EXPOSE 4222 8222
# Fri, 25 Feb 2022 03:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:03:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c940513d538449d692b24e2bad765ddf948bdac501988eb123df158ee291d31`  
		Last Modified: Fri, 25 Feb 2022 03:04:36 GMT  
		Size: 6.8 MB (6768603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6d2d9b3fc25f46965b7cf1f1633f11e7f4a2fd071e9b86c544f74b4279599b`  
		Last Modified: Fri, 25 Feb 2022 03:04:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

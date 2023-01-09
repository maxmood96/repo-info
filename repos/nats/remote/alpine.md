## `nats:alpine`

```console
$ docker pull nats@sha256:d52eefebaf803e3c84189eef5c651c837ada104319dd0fe121ffc1f70475459a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:508b341e189a64769a34054d034d835153ab7a27520ebd5e8a53d138b55770ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8585890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8333132a7c9a559bcdf54d6ddb9c171d92877d9df7a08bcd9265983c16b13d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Fri, 06 Jan 2023 19:19:45 GMT
ENV NATS_SERVER=2.9.11
# Fri, 06 Jan 2023 19:19:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0ff6e07f5cf211b643395132f63a69d69f0ed85ddcefd292b150574392e75edb' ;; 		armhf) natsArch='arm6'; sha256='d2c58d51c5050582ec1888107a6eea041745b287548a37e27569437a4725c3ed' ;; 		armv7) natsArch='arm7'; sha256='cef33d5b84473050e3dc0143117e336e90853e33d6329847612db88a1b8b139f' ;; 		x86_64) natsArch='amd64'; sha256='7491944084cd0128c1ddf9a313095817a2c558b0911581c98e65b84779110856' ;; 		x86) natsArch='386'; sha256='510eb4e4a32f1feba76232187767dd8ff0e021593f1cfbb6c5646343f3ca7a68' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Jan 2023 19:19:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Jan 2023 19:19:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Jan 2023 19:19:48 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Jan 2023 19:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jan 2023 19:19:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3005212e109bb7b48e59d2736267c699cbc65a820af3197e413ad8e69d35e948`  
		Last Modified: Fri, 06 Jan 2023 19:20:46 GMT  
		Size: 5.2 MB (5214184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab857ba92ee341443db07e27aa7bc1c5d4b67c59ca4ae6af06016dc46fe1a1`  
		Last Modified: Fri, 06 Jan 2023 19:20:45 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc1129fb3015f518c705c15fdf443aaefd039d0c5adc9cad3f6f0caf12de671`  
		Last Modified: Fri, 06 Jan 2023 19:20:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:7f370073ed44501cc78760b1ad096230e3a48d5aa2ccf617dc2ad3b49816967a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8086974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c7813b2266c292d24b2bc4e4e4d087b9cf371bb2bf42e0c5751d967a4504d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Fri, 06 Jan 2023 19:01:33 GMT
ENV NATS_SERVER=2.9.11
# Fri, 06 Jan 2023 19:01:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0ff6e07f5cf211b643395132f63a69d69f0ed85ddcefd292b150574392e75edb' ;; 		armhf) natsArch='arm6'; sha256='d2c58d51c5050582ec1888107a6eea041745b287548a37e27569437a4725c3ed' ;; 		armv7) natsArch='arm7'; sha256='cef33d5b84473050e3dc0143117e336e90853e33d6329847612db88a1b8b139f' ;; 		x86_64) natsArch='amd64'; sha256='7491944084cd0128c1ddf9a313095817a2c558b0911581c98e65b84779110856' ;; 		x86) natsArch='386'; sha256='510eb4e4a32f1feba76232187767dd8ff0e021593f1cfbb6c5646343f3ca7a68' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 06 Jan 2023 19:01:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 06 Jan 2023 19:01:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 06 Jan 2023 19:01:37 GMT
EXPOSE 4222 6222 8222
# Fri, 06 Jan 2023 19:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jan 2023 19:01:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9c430594153fe16619545b3691109f69f6b50cf249e56cb38ab103cde91ad3`  
		Last Modified: Fri, 06 Jan 2023 19:02:44 GMT  
		Size: 5.0 MB (4978864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d0ffb9f3a02579d3758c82718e4b876091b11f2de18ac61f7ce002fad3f39b`  
		Last Modified: Fri, 06 Jan 2023 19:02:43 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddccb2d2cc74e2bd876b7b9c58e3a7dae1a93a978ad86e0cf016a3b268cf250`  
		Last Modified: Fri, 06 Jan 2023 19:02:42 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:c3f54742a5204c7905541fa75a98a4e3b4d935d1743fc86fafca8cb45c690ffa
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7836628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406197ad7c8143a2bc8fcf46e8f6c4e07fccb1ec56a5861635d08f3b36d5e66e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 09 Jan 2023 17:06:27 GMT
ADD file:4696f25d0f019b27457c55b3b128b70bf153f38e3e4eb5bdfc21058543313e94 in / 
# Mon, 09 Jan 2023 17:06:27 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:42:55 GMT
ENV NATS_SERVER=2.9.11
# Mon, 09 Jan 2023 17:42:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0ff6e07f5cf211b643395132f63a69d69f0ed85ddcefd292b150574392e75edb' ;; 		armhf) natsArch='arm6'; sha256='d2c58d51c5050582ec1888107a6eea041745b287548a37e27569437a4725c3ed' ;; 		armv7) natsArch='arm7'; sha256='cef33d5b84473050e3dc0143117e336e90853e33d6329847612db88a1b8b139f' ;; 		x86_64) natsArch='amd64'; sha256='7491944084cd0128c1ddf9a313095817a2c558b0911581c98e65b84779110856' ;; 		x86) natsArch='386'; sha256='510eb4e4a32f1feba76232187767dd8ff0e021593f1cfbb6c5646343f3ca7a68' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 09 Jan 2023 17:42:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 09 Jan 2023 17:42:58 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 09 Jan 2023 17:42:59 GMT
EXPOSE 4222 6222 8222
# Mon, 09 Jan 2023 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 17:42:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c527615e4ffa2d5b9b777fd469b3b5ba7c1b1e9201c065be2c43569de48a3754`  
		Last Modified: Mon, 09 Jan 2023 17:07:17 GMT  
		Size: 2.9 MB (2865208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d73a336145882faccd34809875f895c5656f01fecee5e507eb3f66921153ab`  
		Last Modified: Mon, 09 Jan 2023 17:44:08 GMT  
		Size: 5.0 MB (4970447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a17bb42266b7bab68da86f2509863bd7b0ef2ff9f7394264c43a21e372353c9`  
		Last Modified: Mon, 09 Jan 2023 17:44:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fef1f1b4135d297a1a9a51450652100292d4907e3d8a675c5dea6b564a1d4b2`  
		Last Modified: Mon, 09 Jan 2023 17:44:07 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9547980b254de3266558a6ef1df24731f1b81394580999af7f8e0f56ac535b5a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8059465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137eb6cff01cf8a79a84220b858e16f5d6bfcd5d49a33c2e1fb3a600d106ff0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:13:53 GMT
ENV NATS_SERVER=2.9.11
# Mon, 09 Jan 2023 18:13:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0ff6e07f5cf211b643395132f63a69d69f0ed85ddcefd292b150574392e75edb' ;; 		armhf) natsArch='arm6'; sha256='d2c58d51c5050582ec1888107a6eea041745b287548a37e27569437a4725c3ed' ;; 		armv7) natsArch='arm7'; sha256='cef33d5b84473050e3dc0143117e336e90853e33d6329847612db88a1b8b139f' ;; 		x86_64) natsArch='amd64'; sha256='7491944084cd0128c1ddf9a313095817a2c558b0911581c98e65b84779110856' ;; 		x86) natsArch='386'; sha256='510eb4e4a32f1feba76232187767dd8ff0e021593f1cfbb6c5646343f3ca7a68' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 09 Jan 2023 18:13:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 09 Jan 2023 18:13:56 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 09 Jan 2023 18:13:56 GMT
EXPOSE 4222 6222 8222
# Mon, 09 Jan 2023 18:13:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:13:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5926ad44fb07bd1b6468b934276f66499dd403aaefc7e4a2425eecd6d1d6dee3`  
		Last Modified: Mon, 09 Jan 2023 18:14:25 GMT  
		Size: 4.8 MB (4799229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee0a9e6a9ad8eabb0f8a9c119f5396c1e80a46027b3a389592c31355c7292fc`  
		Last Modified: Mon, 09 Jan 2023 18:14:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c2354f9e90a43e060a732dde40a2101e83a9a005c7bc393617a8b1fe1ee5a6`  
		Last Modified: Mon, 09 Jan 2023 18:14:24 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

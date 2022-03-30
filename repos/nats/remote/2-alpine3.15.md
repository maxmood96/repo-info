## `nats:2-alpine3.15`

```console
$ docker pull nats@sha256:ea8d81ec5b1df3176e1076b44fb4c1effad2f0fd2a89ae0eaf22dde3a530609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:ddbbfa522c3602ac76b51284c184828f24be9fcb329665c8c835d0a0b5f71609
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33323e6971854b66bb8ff96bd008fee5ae9fea9f9118b96fd68ee148e42bef21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:04:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 12:04:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 12:04:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 12:04:39 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 12:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:04:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9a10b3bb713cc8101378783c4f52f75d8f834fa21f5fc136a30904bfcb4f9f`  
		Last Modified: Tue, 29 Mar 2022 12:05:12 GMT  
		Size: 4.8 MB (4783177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb87d96c1921472cce8519d8fb67b430106edf099c364e068ceecefd4ba7e00`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c21f97f27e2c9ba2af1a903b9062eb0b884a9a6992c9d8964ecd84a2348cae`  
		Last Modified: Tue, 29 Mar 2022 12:05:11 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:3fee8925082b25042ab9087ddcc5c293a612850d5244cb7775af22caca1f6d9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7070564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4e309ef1582f25174193504f16ecbc35a11f70c720953171928ee47ae18c5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:08:37 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 08:08:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 08:08:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 08:08:43 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 08:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:08:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433d34ffede9d0eff77eaf04849e4b79ec0f7e200a2d117f5e58a50e0b82217`  
		Last Modified: Tue, 29 Mar 2022 08:10:45 GMT  
		Size: 4.4 MB (4447623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df1c1e8b65688f71ac5b1bd33b8077ef7a6394d79c1ec7dffcbc7914484d48c`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da97cd054d0f3a42979a00c4d9c8a3255934903076031d8ecb9f73355e33cdc6`  
		Last Modified: Tue, 29 Mar 2022 08:10:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:e8f9eec7c4ba7fe1229f4ca2db3c561e8407efacb9de545387e6f626122582b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6866678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbd7e5cc5054df3236a9ee658006f41dcd1b877c5c3baa541d889f0fd0bfacb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 02:13:28 GMT
ADD file:8c959b80e3661beea7b3468017b88897d981bf52ed43c074e7c87ecb753e9059 in / 
# Tue, 29 Mar 2022 02:13:28 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 15:01:31 GMT
ENV NATS_SERVER=2.7.4
# Wed, 30 Mar 2022 15:01:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 30 Mar 2022 15:01:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 30 Mar 2022 15:01:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 30 Mar 2022 15:01:36 GMT
EXPOSE 4222 6222 8222
# Wed, 30 Mar 2022 15:01:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 15:01:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22b1e5a07a97d7af6fdc335e3b3a975b73908fa19b084289c408a00814da0398`  
		Last Modified: Tue, 29 Mar 2022 02:15:28 GMT  
		Size: 2.4 MB (2424303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af45d1acb166ea694d7b2181c4a0d38083a9d2296a77582386f62f0017e1aa0`  
		Last Modified: Wed, 30 Mar 2022 15:03:44 GMT  
		Size: 4.4 MB (4441379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a27c66556de317ddb36f0447692937578a021e751821e66df0f7434d828c214`  
		Last Modified: Wed, 30 Mar 2022 15:03:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a63392fde5610fbbcffd7e7f0bd9b7d3925022ab401a362c458f4728ed37a8c`  
		Last Modified: Wed, 30 Mar 2022 15:03:41 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e1d92c67b112506e1eba438169cabbae1e7df652747fced40ee09e49016709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc357f18f7318c9dd8b86a35d7f8ade6041903325fe61edd036d0423b4ac7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 19:27:05 GMT
ENV NATS_SERVER=2.7.4
# Tue, 29 Mar 2022 19:27:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 29 Mar 2022 19:27:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 29 Mar 2022 19:27:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 29 Mar 2022 19:27:11 GMT
EXPOSE 4222 6222 8222
# Tue, 29 Mar 2022 19:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 19:27:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6838fdfa81afc565c161c1fee30401de3a013bfb571f5be3c3a993badc92f3f`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 4.4 MB (4426412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dce858aad644833ca99f39e8757136a768b7f8ecfaae59ac4154e3823651dd`  
		Last Modified: Tue, 29 Mar 2022 19:28:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a6ab0d728bdc5bcab9e3d3e9236d289a5888dd54c1cd6cade53e1cac8f5c2`  
		Last Modified: Tue, 29 Mar 2022 19:28:11 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

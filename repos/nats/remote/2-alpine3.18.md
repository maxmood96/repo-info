## `nats:2-alpine3.18`

```console
$ docker pull nats@sha256:1b84cbfbd4a277a828e5c21e7cfc5c608fae5de37204e68abd8805bfae92d20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:23dc685e3c08196e1b7e062a062a0e297da560197192316ba846db109c8c9085
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9509686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9beb0f33b937617e04a3bece66962a00cd4f8a2e4da8fd6723e2af3135ec6531`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:09:33 GMT
ENV NATS_SERVER=2.10.5
# Fri, 01 Dec 2023 07:09:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Dec 2023 07:09:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Dec 2023 07:09:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Dec 2023 07:09:35 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Dec 2023 07:09:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:09:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a214d6eab35932b2be0106225c564b689dab8bf0c4f2d2657c63e48b2247b6fc`  
		Last Modified: Fri, 01 Dec 2023 07:10:15 GMT  
		Size: 6.1 MB (6106263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f423ec088dc856b962a5dd89c31ab09416457de0a5994922f51bef46d1945f5`  
		Last Modified: Fri, 01 Dec 2023 07:10:14 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93563c51811f1dc92fe243bd5b8721f10cf5060cfd617ed40a18ed8a840ab3a`  
		Last Modified: Fri, 01 Dec 2023 07:10:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:433db02abd4fb5d3266e2a31efa38ab3e9a4001d6d283a6365bb8f3db3b9f9bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e442db29bc05ffa28c62e15db2784c2a1b3ade9914a545f8290feeb4630caa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 01:11:29 GMT
ENV NATS_SERVER=2.10.5
# Fri, 01 Dec 2023 01:11:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Dec 2023 01:11:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Dec 2023 01:11:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Dec 2023 01:11:32 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Dec 2023 01:11:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 01:11:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80504cfc1cecd39ef7c596d1e80525e10c578bc8d65835984abcfec95e172880`  
		Last Modified: Fri, 01 Dec 2023 01:12:04 GMT  
		Size: 5.8 MB (5821536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1420095f4621d4d2753d25dc0b6c870266bc3ecd9facf8de634526017bda3f49`  
		Last Modified: Fri, 01 Dec 2023 01:12:04 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc87349e1b6315718248b69a24322186ed87d3a6e382433832fd9148d91d5ee1`  
		Last Modified: Fri, 01 Dec 2023 01:12:03 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:bfed901bdd71a5519fd48555b15a0453f057a4ff03c5f2d31ea1dd9a1713d601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8713112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15bb652001d2d6a7ab82361eec155510ebb43ab9482795f00aa25eeb8392d3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 23:57:32 GMT
ENV NATS_SERVER=2.10.5
# Thu, 09 Nov 2023 23:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 09 Nov 2023 23:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Nov 2023 23:57:35 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 23:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a95a8f9c7558ea674caed68789eb2aace9a0740df0198190efb5080264d9ea5`  
		Last Modified: Thu, 09 Nov 2023 23:58:15 GMT  
		Size: 5.8 MB (5812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602ac6cfac9e9ff1b75955330988f2cb69b662f35d4eff05dd7116827e4af391`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e88579aecffff9348231963bc6152cffaab105f56ff03fab980c0e6564c93`  
		Last Modified: Thu, 09 Nov 2023 23:58:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8e5a971e8f495d66ceb3215bbb5bc32695cc8729f0b74e40d4e07b2739452ced
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9013552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2b6e54efd92d20ab884320efcef229bbe42b713cfea4830f781914ed166673`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:51:45 GMT
ENV NATS_SERVER=2.10.5
# Fri, 01 Dec 2023 06:51:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='de560b8863ddceac5d765b1f99d4b8f0becf8488890253beafffb7cb730f1aa8' ;; 		armhf) natsArch='arm6'; sha256='b0ca5676f1b65a60dd7feb0b1be5b7ae35977a978ba21451d0165492c984a93f' ;; 		armv7) natsArch='arm7'; sha256='0b0695e6f4e90012021e5ef59b71d6a4e0a19df0c5852c83494d7e9776dc5085' ;; 		x86_64) natsArch='amd64'; sha256='33e9796344fcde53d1d9ab5fc3e2393d1f558aec53f5ea51f769827602a20225' ;; 		x86) natsArch='386'; sha256='f8d4facfc3735ea46ccaecc1e7815f2b755dd0697b0b7f7d83cff568e2ebd77c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 01 Dec 2023 06:51:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 01 Dec 2023 06:51:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 01 Dec 2023 06:51:47 GMT
EXPOSE 4222 6222 8222
# Fri, 01 Dec 2023 06:51:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 06:51:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4abae88c92dff604adc9b11de2e21a2c2c02d654f4b48a66b2480deaefb77cc`  
		Last Modified: Fri, 01 Dec 2023 06:52:36 GMT  
		Size: 5.7 MB (5679520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5f41ee96c82305810d14f374a00e3b7764c68a8fc801ef4a29c851a5b1edfc`  
		Last Modified: Fri, 01 Dec 2023 06:52:35 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1625e9baa02bfcee6445f104f2179734a956ea8b9e7dd0ed70c084ae33b242`  
		Last Modified: Fri, 01 Dec 2023 06:52:35 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

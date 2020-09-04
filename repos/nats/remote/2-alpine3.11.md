## `nats:2-alpine3.11`

```console
$ docker pull nats@sha256:973f73d42889d90339012de8af544f4f6b69bc5ea15a6ace5df989bbd6ffbce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:a6f914658a5f8a7a82c9005a3a36863628d331cb2cd4c0c0a3653e7e8a7c0d95
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7208222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96815e17bf1191cbfa7a1745a82f87b8fcc43fbd793da4d66c9fd175c136dd27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 04 Sep 2020 19:23:32 GMT
ENV NATS_SERVER=2.1.8
# Fri, 04 Sep 2020 19:23:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='567d5c7f80305b8876230204b993f0cf213411d006d931a036b26dd2288ac81b' ;; 		armhf) natsArch='arm6'; sha256='d76c1ed6f660e13faaa8b1c058723981aa59436ce7d4d4e208ae486395db458f' ;; 		armv7) natsArch='arm7'; sha256='e26f0eba9b065f9537986f88233f279f44c01487aacffe65d4d7440129a5d0a2' ;; 		x86_64) natsArch='amd64'; sha256='8ec25475ef1d49bf5e721de38deb11d689d1a9b2fa588540af78d56cbea2b49d' ;; 		x86) natsArch='386'; sha256='e8535179805573e9d684cc8aa6f79551ab9fcfacd45643d7ba2174e176997d9e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 04 Sep 2020 19:23:34 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 04 Sep 2020 19:23:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 04 Sep 2020 19:23:35 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Sep 2020 19:23:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Sep 2020 19:23:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f9fca7275bd535bd4680297f95f240c9b48d96d0b9b7f17dd38b73917d2b99`  
		Last Modified: Fri, 04 Sep 2020 19:24:56 GMT  
		Size: 4.4 MB (4393961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6905e1079d9ad73fb2f14b529adb1378cfaa4fcabf48ee0a819af4a49842a3a4`  
		Last Modified: Fri, 04 Sep 2020 19:24:55 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a148278ed7ad77a22a36b3ea6e6cdbcaa397edc556440f575992b8bbd8abfc9b`  
		Last Modified: Fri, 04 Sep 2020 19:24:55 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:fee67afb8a9c6c38c60a5b90f51b6a6dfdb607b13d04240cf4faae9f8235d69d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6717777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5af24d85d20ca2ddf1a257d6667c94e32ad6c1f381964f6ea48833ebc6eb39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:02:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:02:36 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:02:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:02:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0546a69fc010fc7d9fdae3cd6ff1eb8d7d7471a3561d782f6bb2bebcb079ad`  
		Last Modified: Wed, 29 Jul 2020 23:03:02 GMT  
		Size: 4.1 MB (4096870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc6927e9f4f4d185c4420481f8b1e06d55f058ad32ac4c0a9fc2ca3c2e0e64`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6963e293037e1e7ddf702b89cf5a9441918b610e877f1710001b055560f92901`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:645d9707a2e5fbd2330b6b7c87601978add8b5388e18c8a2dc988b2ae00bc7fd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6532999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbe66195f5f434137dc29427ce470c725a6d3a3fb47451c0608398ec12e0749`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 04 Sep 2020 20:01:21 GMT
ENV NATS_SERVER=2.1.8
# Fri, 04 Sep 2020 20:01:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='567d5c7f80305b8876230204b993f0cf213411d006d931a036b26dd2288ac81b' ;; 		armhf) natsArch='arm6'; sha256='d76c1ed6f660e13faaa8b1c058723981aa59436ce7d4d4e208ae486395db458f' ;; 		armv7) natsArch='arm7'; sha256='e26f0eba9b065f9537986f88233f279f44c01487aacffe65d4d7440129a5d0a2' ;; 		x86_64) natsArch='amd64'; sha256='8ec25475ef1d49bf5e721de38deb11d689d1a9b2fa588540af78d56cbea2b49d' ;; 		x86) natsArch='386'; sha256='e8535179805573e9d684cc8aa6f79551ab9fcfacd45643d7ba2174e176997d9e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 04 Sep 2020 20:01:59 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 04 Sep 2020 20:02:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 04 Sep 2020 20:02:18 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Sep 2020 20:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Sep 2020 20:02:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707b0a874f39e2d53e2283ffb23bd80599cd3de6fb4813b5d80b6a3576b9a285`  
		Last Modified: Fri, 04 Sep 2020 20:11:13 GMT  
		Size: 4.1 MB (4109958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cdb37890e6affd51af4e84cb645a7bdca5322a54690e7ed1ef70fd6e7f55b9`  
		Last Modified: Fri, 04 Sep 2020 20:11:11 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358a12bb7b0cdd9809f9bcd5bf1bdbc75c5a232db47e87757596eec47fea3396`  
		Last Modified: Fri, 04 Sep 2020 20:11:11 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:700235b690efc969452c359aa31b2b636e1001730ac02e9d67aec2f035b23370
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6819487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c44b6c5226c848ac88f68fb752a7650eec2ef1ebd3b91fba0e525f5903f7ee3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 04 Sep 2020 19:40:30 GMT
ENV NATS_SERVER=2.1.8
# Fri, 04 Sep 2020 19:40:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='567d5c7f80305b8876230204b993f0cf213411d006d931a036b26dd2288ac81b' ;; 		armhf) natsArch='arm6'; sha256='d76c1ed6f660e13faaa8b1c058723981aa59436ce7d4d4e208ae486395db458f' ;; 		armv7) natsArch='arm7'; sha256='e26f0eba9b065f9537986f88233f279f44c01487aacffe65d4d7440129a5d0a2' ;; 		x86_64) natsArch='amd64'; sha256='8ec25475ef1d49bf5e721de38deb11d689d1a9b2fa588540af78d56cbea2b49d' ;; 		x86) natsArch='386'; sha256='e8535179805573e9d684cc8aa6f79551ab9fcfacd45643d7ba2174e176997d9e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 04 Sep 2020 19:40:35 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 04 Sep 2020 19:40:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 04 Sep 2020 19:40:36 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Sep 2020 19:40:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Sep 2020 19:40:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3d1d8b6792cec2b145ec7c0c1b6107e3712804cbd65a93c4d6bc4f5a540ce2`  
		Last Modified: Fri, 04 Sep 2020 19:51:31 GMT  
		Size: 4.1 MB (4094087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c256e59f9e1973a41cd6c2d2af211bfb10c5534b990b63e9c81790cd3c1bdbf3`  
		Last Modified: Fri, 04 Sep 2020 19:51:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ea7fd4055fec9b7d9f52d74d616f372dbd367262c3cec827ce3ddc633e3efc`  
		Last Modified: Fri, 04 Sep 2020 19:51:29 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

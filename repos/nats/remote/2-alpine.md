## `nats:2-alpine`

```console
$ docker pull nats@sha256:d38a7d55d6aa111d54e9a66f62c1d21252b038c6a3b8d06f66779279aba47212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:aa8d6df107099e3d50f98a8bfe9f7e4c52023f0c0f5f0bc5ee89d775792e9ed0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01640f492e23993e18e6c586c03a9c23b9129a296e8d8e02b4d5422740863e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Thu, 05 Aug 2021 01:20:12 GMT
ENV NATS_SERVER=2.3.4
# Thu, 05 Aug 2021 01:20:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c8ba676a6c4ec9d3088e0b64ffdae36e2f2a9e1b89f030799f3efbb2923524a0' ;; 		armhf) natsArch='arm6'; sha256='d1f14441d1fbd53a7bff9623e8e572707d3e7024b42b6e925ad371d4dec0bc47' ;; 		armv7) natsArch='arm7'; sha256='2488706de91e94eba477ddbc3b293ec0b4d823509656cc101eec6a07e0319bb5' ;; 		x86_64) natsArch='amd64'; sha256='8c11abdeca4882888a8b6fbc45effe9fb4d1070eda3939b7299892c8c69a3e87' ;; 		x86) natsArch='386'; sha256='010bca73095d8a05495ef74a112dfd3919925b0ced10bc4c5f876f3858ca41f7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 05 Aug 2021 01:20:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 05 Aug 2021 01:20:15 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 05 Aug 2021 01:20:15 GMT
EXPOSE 4222 6222 8222
# Thu, 05 Aug 2021 01:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Aug 2021 01:20:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4bbee8f25494718730aa5ebff74dab60f38f303e988e4a7eab989ba0669a7e`  
		Last Modified: Thu, 05 Aug 2021 01:20:51 GMT  
		Size: 4.8 MB (4790007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae6ecbeb5464957754cc177cbd4fc5a4e8eff3ebda4089210368958dffbf88b`  
		Last Modified: Thu, 05 Aug 2021 01:20:49 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11c127bfb05be78a521551387911d85895dc91150ef7e5d40add61fe00d2dc5`  
		Last Modified: Thu, 05 Aug 2021 01:20:50 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d5fc2c9df074891880beadedf530ee3dbf0761259a14619e946c1cefa842cac3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7079723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f49351bac7a37d427b25fbdcc43daa3d1ea704fe96f3931802df83f01bf235c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:42 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Fri, 30 Jul 2021 17:49:42 GMT
CMD ["/bin/sh"]
# Mon, 02 Aug 2021 21:16:47 GMT
ENV NATS_SERVER=2.3.3
# Mon, 02 Aug 2021 21:16:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f8e04470165fdfba062442cf5975f22668ab20fb12df7e299734e16a45370bef' ;; 		armhf) natsArch='arm6'; sha256='6396531f34e99cca903cdd461a79f1b8255d0cc219e5186ea15284b5b5e7e5e7' ;; 		armv7) natsArch='arm7'; sha256='4353de84d9e42b24b73ba98a4ed2a9eaa7c4f945bd68e1ddb4fbde885020ab30' ;; 		x86_64) natsArch='amd64'; sha256='66703b81de34d06060eb2198dfb5a1087547d45e680dee4da1214198a8073ce5' ;; 		x86) natsArch='386'; sha256='e38b9c9eda279bc4eee9cf6a3d4b2b25774b692450421a16e2ff6602977e6571' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Aug 2021 21:16:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 02 Aug 2021 21:16:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 02 Aug 2021 21:16:53 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Aug 2021 21:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Aug 2021 21:16:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3313ef1b9ecd8d9e94997ae371b1c0aabda27773f0b2e12b4be7463517cf87`  
		Last Modified: Mon, 02 Aug 2021 21:18:59 GMT  
		Size: 4.5 MB (4454370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785fbb490293d9c2f8cdaed64735e76ea2a0dc1c40e13814102053f6d9c4ddc3`  
		Last Modified: Mon, 02 Aug 2021 21:18:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee9f0a3fdc78fe2942c2a3d6969418df884ad628f52adb50525f4022ed56ec2`  
		Last Modified: Mon, 02 Aug 2021 21:18:56 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:710b791217f5f7aaa1e1fbfbd41641fb8639f3c8b83b8cea464b7edf19e104aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6879235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b35042ddccc5d52436cfc80b044fc36c860661fff4dd2256df025c6b9644548`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Thu, 05 Aug 2021 01:04:26 GMT
ENV NATS_SERVER=2.3.4
# Thu, 05 Aug 2021 01:04:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c8ba676a6c4ec9d3088e0b64ffdae36e2f2a9e1b89f030799f3efbb2923524a0' ;; 		armhf) natsArch='arm6'; sha256='d1f14441d1fbd53a7bff9623e8e572707d3e7024b42b6e925ad371d4dec0bc47' ;; 		armv7) natsArch='arm7'; sha256='2488706de91e94eba477ddbc3b293ec0b4d823509656cc101eec6a07e0319bb5' ;; 		x86_64) natsArch='amd64'; sha256='8c11abdeca4882888a8b6fbc45effe9fb4d1070eda3939b7299892c8c69a3e87' ;; 		x86) natsArch='386'; sha256='010bca73095d8a05495ef74a112dfd3919925b0ced10bc4c5f876f3858ca41f7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 05 Aug 2021 01:04:31 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 05 Aug 2021 01:04:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 05 Aug 2021 01:04:32 GMT
EXPOSE 4222 6222 8222
# Thu, 05 Aug 2021 01:04:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Aug 2021 01:04:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd5cf7dc8e797a24b683019e084284bb92eec2adcab6a7db0e90c15c458ac94`  
		Last Modified: Thu, 05 Aug 2021 01:06:44 GMT  
		Size: 4.5 MB (4450348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e915c2aa290b8ce2d3d394e42c3c8ec082d1f0b2875c129e0b70acd24fb6b99c`  
		Last Modified: Thu, 05 Aug 2021 01:06:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa6f1d48cb8b2dab86b9fe103c5cf0f6fb0940930b0a618a474e66305a2b52c`  
		Last Modified: Thu, 05 Aug 2021 01:06:41 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f818c9007861b8440d5c89a859f8f20f483637ab3f3e7c7a7f89ef40afd23937
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7113993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc01fa8c08e4612961dfe7cf6c422a1a58b99637fd0297f9c3d811b95a32c185`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Mon, 02 Aug 2021 21:06:09 GMT
ENV NATS_SERVER=2.3.3
# Mon, 02 Aug 2021 21:06:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f8e04470165fdfba062442cf5975f22668ab20fb12df7e299734e16a45370bef' ;; 		armhf) natsArch='arm6'; sha256='6396531f34e99cca903cdd461a79f1b8255d0cc219e5186ea15284b5b5e7e5e7' ;; 		armv7) natsArch='arm7'; sha256='4353de84d9e42b24b73ba98a4ed2a9eaa7c4f945bd68e1ddb4fbde885020ab30' ;; 		x86_64) natsArch='amd64'; sha256='66703b81de34d06060eb2198dfb5a1087547d45e680dee4da1214198a8073ce5' ;; 		x86) natsArch='386'; sha256='e38b9c9eda279bc4eee9cf6a3d4b2b25774b692450421a16e2ff6602977e6571' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Aug 2021 21:06:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 02 Aug 2021 21:06:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 02 Aug 2021 21:06:12 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Aug 2021 21:06:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Aug 2021 21:06:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b71cb50e81b94a1183dec31a916ec92da12268c9d5c01358f63f093176829d`  
		Last Modified: Mon, 02 Aug 2021 21:07:22 GMT  
		Size: 4.4 MB (4403398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e71c9cdab2ba7a29d11ef463c8173ea1cdc1f4a0a549ee1d8bdf0a21392641`  
		Last Modified: Mon, 02 Aug 2021 21:07:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f4a027c87d570eda83fa005f1747518d8e6f172eaf1f5432d6073835418317`  
		Last Modified: Mon, 02 Aug 2021 21:07:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

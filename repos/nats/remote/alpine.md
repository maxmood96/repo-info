## `nats:alpine`

```console
$ docker pull nats@sha256:dfd8407f92396bbe19df492a8f5cea86bd1869320960e53572649f6c9d7369fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:f98772e0f2222bf626db93d8f4dab31459a0d859e901c5554cc076088bdc9f47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b229b8720408fa48ff27cb600c243a0ea34ae241af9a532a457dd1302ad60d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:47:45 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 05:47:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 05:47:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 05:47:49 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 05:47:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:47:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2de72945075aec3a93ecb6af12474a3623374dac5d6eb467826bb3f176d9db`  
		Last Modified: Sat, 13 Nov 2021 05:48:24 GMT  
		Size: 4.9 MB (4856278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7e2c9925a779c559f1381de66066f54c7545dd547ab50f181fdf5bad8b76a`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d123a218501888dc051dc9935a6248b5dc7f0ddad4256c03157e4ea9a4f76af6`  
		Last Modified: Sat, 13 Nov 2021 05:48:23 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a4fd7de980bb6490a47bcd0c467aee772f96096c57bb1cc724482627e8858a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3600d1d6d1896742ff5eec4447636481412e3bc1b57e8cbd60a97569dba12952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 22:58:24 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 22:58:29 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 22:58:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 22:58:30 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 22:58:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1253cc1a0f998799434cc5feb134e39c976d785e8abd825d4b70f7bc811e673`  
		Last Modified: Fri, 19 Nov 2021 23:00:36 GMT  
		Size: 4.5 MB (4521082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e38c6e4a411f96e627ed56d7d4604c289a6959fb5ce2f3da2962c900637e8a`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695fd12986a53d165bec7fcb2f87f7665233f1257568f6c9cadb7ba6f47ebe81`  
		Last Modified: Fri, 19 Nov 2021 23:00:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:927653b6f646dceb6d518c8d58652ae16f07a585f56e2083b8dc640aa54032bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed121c45beb860b69d68c3e2e94a2ac7015107c8968ea2a40307dc587a0756c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 10:49:53 GMT
ENV NATS_SERVER=2.6.4
# Sat, 13 Nov 2021 10:49:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff37771c0442e5921dd6867ef712c4029375a134f478b45469f5649b31ca06ae' ;; 		armhf) natsArch='arm6'; sha256='47b58410696fc2bbdd4b0c604f8a6df74b348bcf56efcff739a84f8c3da16f22' ;; 		armv7) natsArch='arm7'; sha256='071a52917aa7931dcce84d052e01310edd82d7399b5d699ddf9ad981af58fa5b' ;; 		x86_64) natsArch='amd64'; sha256='8a81d7c2c65f698875f5ed36cca842e37e51eb9bddb2374690d49bdc782aa6f5' ;; 		x86) natsArch='386'; sha256='659e085ed13d51acf52468e6e44257bf3dac3111ddf90ba065beb9a3c0a71b32' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 13 Nov 2021 10:49:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 13 Nov 2021 10:50:00 GMT
EXPOSE 4222 6222 8222
# Sat, 13 Nov 2021 10:50:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 10:50:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7667eb269dc08efac3da01b8675c36b733dbbe274c782a02e4a86b8361d5b942`  
		Last Modified: Sat, 13 Nov 2021 10:52:16 GMT  
		Size: 4.5 MB (4513136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e575668b5d7e7f7152f80542c775ccba3f377141e747e329fb23896bfe23e9`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528edb88e91f872a79a50cc2def03d40caacfed6b26567bb649719c78bcadf70`  
		Last Modified: Sat, 13 Nov 2021 10:52:14 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:997a3f7ffb28c81b50b72fd56de75846feeb26e3bc7fb84dafb6cf16021d2f08
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7191230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d42142abd80ea09ebcaf23e32e6f07df05bb7a0ff2b315b06974c8b84b47a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:01:35 GMT
ENV NATS_SERVER=2.6.5
# Fri, 19 Nov 2021 23:01:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='85b30b3511b4b66764d6b9fcf3c91937b778e8beb8dd44a179622b08869cfbbc' ;; 		armhf) natsArch='arm6'; sha256='c2b3a7d5e443b8c4d75f4268e8a3e302d1174b3cdb2daa45497869edc993264b' ;; 		armv7) natsArch='arm7'; sha256='66af4d04f5e963b93ccb259c6bd4e7532cc3126d1734781cbb5dbb14a01fdd8c' ;; 		x86_64) natsArch='amd64'; sha256='5f5799014b82a02433f4f6333ad84d45da16696f1bf294ce8f2740ea05ced10b' ;; 		x86) natsArch='386'; sha256='6bc66f8b5be8163d9ee1d3811e8907717538ccbe242b665962b38ead0a2e62fb' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 19 Nov 2021 23:01:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 19 Nov 2021 23:01:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 19 Nov 2021 23:01:41 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:01:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ccc03d25ac63e171bfd865f61964d69fd96ea152dd4815b71be6c4368e219d`  
		Last Modified: Fri, 19 Nov 2021 23:02:44 GMT  
		Size: 4.5 MB (4472588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068e4494ae13d5594c2de7cd17ec2ee17d2f4082f3591dfad74cc76496ba1957`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acfa78644ce575170cba7d1bcfdecd361469b3345c4d31c56683436b9f9db55`  
		Last Modified: Fri, 19 Nov 2021 23:02:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

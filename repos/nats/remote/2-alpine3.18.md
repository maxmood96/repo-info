## `nats:2-alpine3.18`

```console
$ docker pull nats@sha256:511f5c4cfc6fdd61eb66afab99dfb38bed69aae630d8d5b36bc9bfc716723cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:5cf5c3802d1e857d169a3f1d5cbe4799d4839fd6f55af788cedcb6e5a22378e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9195249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4997d3c6db9cae525d31602ba338a453ba4facd93e802fa29b3ba534475bd9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 19:26:02 GMT
ENV NATS_SERVER=2.9.21
# Mon, 07 Aug 2023 19:26:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c2906b5a3b930e842c0a88772b5f484e962ac342f57852a45b1c5a7e10f2197' ;; 		armhf) natsArch='arm6'; sha256='424576d72c1f3b5bd309254d0d0462e21b4aaf6b85defcf6663128294b15c16f' ;; 		armv7) natsArch='arm7'; sha256='3ee6e4db568311c6832b1ec4d76933cc8ee1a783281ed89da5ebe6f602d1c521' ;; 		x86_64) natsArch='amd64'; sha256='2bd2878a63efa5bc9b9c3f1d43fd953c7e14b22ba540f7dea19f7fb3a803215d' ;; 		x86) natsArch='386'; sha256='6eef61e4a81fb03f47ef8bfe08eab6909846a3404db28b4260630385dc27910f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 07 Aug 2023 19:26:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 07 Aug 2023 19:26:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 07 Aug 2023 19:26:05 GMT
EXPOSE 4222 6222 8222
# Mon, 07 Aug 2023 19:26:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 19:26:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd25bdbc8b4e243f7c3ffdffcc8115824b4b4cb2e9e73e3daadb257d79643d2`  
		Last Modified: Mon, 07 Aug 2023 19:26:33 GMT  
		Size: 5.8 MB (5792639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115edb875772e3386f7d2813cc6497fbdbaea0f7f9a39e552e3309472365aa90`  
		Last Modified: Mon, 07 Aug 2023 19:26:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279c31eb6dadb7f2e0ca227988e36fd0206af24465e2a207d488967470b3a63e`  
		Last Modified: Mon, 07 Aug 2023 19:26:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:5e07de3c322c8771519734bef7e466ac5028ab54275802d4deb77c36411e3cbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8700810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0fee524fb6e7f519b9ae3abd80976c1836c3f10c0be79daf8e035556935b24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 19:50:24 GMT
ENV NATS_SERVER=2.9.21
# Mon, 07 Aug 2023 19:50:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c2906b5a3b930e842c0a88772b5f484e962ac342f57852a45b1c5a7e10f2197' ;; 		armhf) natsArch='arm6'; sha256='424576d72c1f3b5bd309254d0d0462e21b4aaf6b85defcf6663128294b15c16f' ;; 		armv7) natsArch='arm7'; sha256='3ee6e4db568311c6832b1ec4d76933cc8ee1a783281ed89da5ebe6f602d1c521' ;; 		x86_64) natsArch='amd64'; sha256='2bd2878a63efa5bc9b9c3f1d43fd953c7e14b22ba540f7dea19f7fb3a803215d' ;; 		x86) natsArch='386'; sha256='6eef61e4a81fb03f47ef8bfe08eab6909846a3404db28b4260630385dc27910f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 07 Aug 2023 19:50:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 07 Aug 2023 19:50:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 07 Aug 2023 19:50:28 GMT
EXPOSE 4222 6222 8222
# Mon, 07 Aug 2023 19:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 19:50:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee480b732706005fa701c3c4028a724e52a4fae0fd1c0aa66e0c837002d561d`  
		Last Modified: Mon, 07 Aug 2023 19:50:50 GMT  
		Size: 5.6 MB (5555005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58f30a3786b4a2dc69c83b465d31a4f645160b79da0a61c29860cdc3972b214`  
		Last Modified: Mon, 07 Aug 2023 19:50:49 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e541018b825fe9c407a093e7cac7a09742ba147db4c9b701c8021337ff70ec`  
		Last Modified: Mon, 07 Aug 2023 19:50:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:c4769e1e475367da9b4fc5a660a6fb32b200d27a3d026495fdc5bf74f9388c16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8447620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9893408047cef17e55311c80520a2cceb027a6e9d68f7206dc77b1330526c23e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:16:18 GMT
ENV NATS_SERVER=2.9.21
# Mon, 07 Aug 2023 20:16:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c2906b5a3b930e842c0a88772b5f484e962ac342f57852a45b1c5a7e10f2197' ;; 		armhf) natsArch='arm6'; sha256='424576d72c1f3b5bd309254d0d0462e21b4aaf6b85defcf6663128294b15c16f' ;; 		armv7) natsArch='arm7'; sha256='3ee6e4db568311c6832b1ec4d76933cc8ee1a783281ed89da5ebe6f602d1c521' ;; 		x86_64) natsArch='amd64'; sha256='2bd2878a63efa5bc9b9c3f1d43fd953c7e14b22ba540f7dea19f7fb3a803215d' ;; 		x86) natsArch='386'; sha256='6eef61e4a81fb03f47ef8bfe08eab6909846a3404db28b4260630385dc27910f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 07 Aug 2023 20:16:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 07 Aug 2023 20:16:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 07 Aug 2023 20:16:22 GMT
EXPOSE 4222 6222 8222
# Mon, 07 Aug 2023 20:16:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:16:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fca2c62cfb95a8e21097e5398887f17729f82e97f22aba05b4a501ead7235bf`  
		Last Modified: Mon, 07 Aug 2023 20:17:02 GMT  
		Size: 5.5 MB (5547144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c778dd55b3c0df3d1fa0c07a38398ecd9605779c83aad61a071e63327b6077a`  
		Last Modified: Mon, 07 Aug 2023 20:17:00 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f262374e9fca7560e610908419255255f99f7ce00698f5da57b988be8a0827`  
		Last Modified: Mon, 07 Aug 2023 20:17:00 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:280523d3cd269840cf3ca0436eaf836b84057947803f07af5208ef8b7a1f765f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8689649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b733a68b85bf5e9f179e1363356f48edd81ae5fe656cf38413a97a99945327f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 19:44:08 GMT
ENV NATS_SERVER=2.9.21
# Mon, 07 Aug 2023 19:44:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c2906b5a3b930e842c0a88772b5f484e962ac342f57852a45b1c5a7e10f2197' ;; 		armhf) natsArch='arm6'; sha256='424576d72c1f3b5bd309254d0d0462e21b4aaf6b85defcf6663128294b15c16f' ;; 		armv7) natsArch='arm7'; sha256='3ee6e4db568311c6832b1ec4d76933cc8ee1a783281ed89da5ebe6f602d1c521' ;; 		x86_64) natsArch='amd64'; sha256='2bd2878a63efa5bc9b9c3f1d43fd953c7e14b22ba540f7dea19f7fb3a803215d' ;; 		x86) natsArch='386'; sha256='6eef61e4a81fb03f47ef8bfe08eab6909846a3404db28b4260630385dc27910f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 07 Aug 2023 19:44:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 07 Aug 2023 19:44:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 07 Aug 2023 19:44:10 GMT
EXPOSE 4222 6222 8222
# Mon, 07 Aug 2023 19:44:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 19:44:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7eb0af764262eda43da676eb6212706a1a5c91fc0745feec3c2a78b11feeb74`  
		Last Modified: Mon, 07 Aug 2023 19:44:35 GMT  
		Size: 5.4 MB (5357887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d47d30642d18189ee8bcbc7387c01d1eddb910a0927366bf969f74ba950073`  
		Last Modified: Mon, 07 Aug 2023 19:44:34 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ace711cbe0f8fc6e880cdb92d235a3031e40977634be3a9fe209f05e65a7b7`  
		Last Modified: Mon, 07 Aug 2023 19:44:34 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

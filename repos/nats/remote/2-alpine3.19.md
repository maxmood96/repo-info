## `nats:2-alpine3.19`

```console
$ docker pull nats@sha256:1983fb960c52b05c1b212d459943fb024dac5419eda36bf55bf64279de68499d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:ea36396a4460389cb144a9022eb5f3ea64591fb8a05f6d5d1a056db30fec8929
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6033b15096c9a633bd78cc2d815e6069d5b0f9f43e2d7208967ba46596f359d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:48:35 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:48:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:48:37 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:48:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f798ba46b67098bd15d5e60f4ba21bc7a74dea83bc32e096b2c4a69fcebd1c`  
		Last Modified: Thu, 11 Jan 2024 02:49:20 GMT  
		Size: 6.1 MB (6124277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa257ea47ccbcf0f4f7fc1790bf5eb92b3a0ae52e1ad2eeab796c971b4d8777`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3196725eed73232f06492a1060fdba1af514ac24a95ee83078183e9cd6e93b7`  
		Last Modified: Thu, 11 Jan 2024 02:49:19 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:f64cc78db496614d2464bc518395a9a9c18dcbced888bd246c53a5f607fb2798
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f43f54a537b58038fca151e541618e03368dcf372994c25b941d20ef6bb6dc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:54:55 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:54:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:54:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:55:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:55:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8e103dfb44072b9bbf2eba7aad94fd639e561a22768da2bb37ea7d6729bab4`  
		Last Modified: Thu, 11 Jan 2024 02:55:51 GMT  
		Size: 5.8 MB (5833322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faf32ab3656f6bddf90a09ced2d48b14b852842c566514822d55a40ed52361a`  
		Last Modified: Thu, 11 Jan 2024 02:55:50 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be21811ddbd891a760c2cc348a08f710ae14eeac84aa8d7d5af26c6581efc8e1`  
		Last Modified: Thu, 11 Jan 2024 02:55:49 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9244a34a1c67c86e4f309985a0c9ddc44c4a26dd32201cebc262d1a246f1e2d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4798f08bfc804e8b7077ab10105d2f686a6204a3f904209ec83f681962ea21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 02:49:45 GMT
ENV NATS_SERVER=2.10.8
# Thu, 11 Jan 2024 02:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d74bba93d60a6a9836f4b54e942b8d4c2c9f33855659584cc7f76fdf8b1c4f7' ;; 		armhf) natsArch='arm6'; sha256='63147f419cda88e2d6f508e7a93dcc35803ad07d3a25bd5bdfdf3830f22a096d' ;; 		armv7) natsArch='arm7'; sha256='bc87934be36709f6f8928e5d65c7f11e8e2c5660826aa6c9af87b3a69cb6b8c3' ;; 		x86_64) natsArch='amd64'; sha256='23f647b813f339f0c8c2ac545f75bebcb2821dce0f47eca50e475e44b5d663d9' ;; 		x86) natsArch='386'; sha256='1ae8582969e34ff731bf065c724ad742ba2a1f566ad8de169b87f9e97b52f5ff' ;; 		s390x) natsArch='s390x'; sha256='826735b8333787b27191cf201162398b530f417f2b80f224fefcfa9d21b480c2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 02:49:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 02:49:48 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 02:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2adfa7ed66cbcf98bfd19fd849cab6c342a8bf21efe1c363c1ec5d3c41ae0`  
		Last Modified: Thu, 11 Jan 2024 02:50:22 GMT  
		Size: 5.7 MB (5700378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c865cf9777bd8e4753ce89930261559591a9d2e030c0dbd995f82ba770e06f`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1071663058684a0e820ec88c736711fda64c374c9a2492274176aadd0ef9bf83`  
		Last Modified: Thu, 11 Jan 2024 02:50:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

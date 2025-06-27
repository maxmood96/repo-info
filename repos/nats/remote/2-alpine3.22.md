## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:d01fc7956bcde73411ae93b65ce5f0416787873edc18c6ab3490b1df02ce8802
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:3fa9fb2909a6d5fc3d03311c4eab7ef44d9d3b07d3060dc3ee09af31615177bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c303eb1d766fef145d081a6efe6667caecdc3d29274580e7cab2c86b555054`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f2d7c33042de7a2721cc7037921866dd5fd1aef06251cb3b52b803e099650f`  
		Last Modified: Thu, 26 Jun 2025 20:17:43 GMT  
		Size: 6.8 MB (6788052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23999ece2fd82b549915d209c1220df0e2118a8ba5002f08029344c1b4c11b0`  
		Last Modified: Thu, 26 Jun 2025 20:17:40 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473fef627e81d8cb609092fc5c8cf8b1c63b551ea1b7efabc4ada599bf6b93f3`  
		Last Modified: Thu, 26 Jun 2025 20:17:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2d087fb959da797f20ae030821cfc23d2ad4a64a60d6366c00c3f8688177c885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b415bcb886edb909afed1be06569934e7e858ecf295a54aeae89dc46df442b4e`

```dockerfile
```

-	Layers:
	-	`sha256:26b50ad7dfc22e733e46076788aac20cdb3cb8016ce575e3c885503970de2efe`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:c407538f141e101cffc6e93ccea6056debe88221abe2666fcea1e76e978812b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10006784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fa8e3a02d934ff0b1507d42fb94e003f944d9c99c410ca998b4f326cb18384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370714c9df343e678c36a394cbc10501b516beab6c5fce69b58b9bebf4249a9f`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 6.5 MB (6504885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126d04e62112930571ace072c0e66e0b6675f7baa4361daebdcc841a347d84c`  
		Last Modified: Thu, 26 Jun 2025 20:17:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c8f8539d59dec90772e674c4b9d02b82a9a630df9678a144bcdf9b36bfa563`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:110e8fc0265af245af68f4f13c82bbd22b526e04b3efed7ac6b206d8544346d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc7a4b99bc73e5fed3010341026e1d528fbf8f910430925d5aefad24bd4df24`

```dockerfile
```

-	Layers:
	-	`sha256:63caa9adf894da2e6e7743936db5d2d122c600e87b80f1315f63e09ce065c928`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:6beb24b9c5ebaf82aa943605e27bf9cc476073c8ba8a85cf1280e7f903933f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9713025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136c6734a14713ef2df657e7b0afeebc4cac53bb1534f54ef1aaf65d1496933c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b94f9506f9f064db25cf04c1de8c94a0f38399389559a320a9bd4bc11f36e7`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 6.5 MB (6492872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b158ea2e3a8384adabb2841e2c82603996443c7dc1a808409ac833bbb51029bb`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641e59c609640e45233cbb6721667b61baf5f41cff04c3aff825f166c256bee8`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:70765a6f52b790a1246aa15f97c5d982ac1713fa15c251166982d64ec0a5105a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf52f6b5f6952440758f161a0c7d3b81e299eb2dc579e6179005f62cec504fd4`

```dockerfile
```

-	Layers:
	-	`sha256:5cd3d0a59672dc8da2c92f06824e2b3654d7aeabd529807d6ecf94d9359b5b74`  
		Last Modified: Thu, 26 Jun 2025 23:56:52 GMT  
		Size: 14.4 KB (14423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:12f12a82b812d423ae207b4141ff201258813ec9f30a193037818728c969566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10418482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8374b467684dc7a7db213ff191ce7d1f2a1545e87c1ebaa2be4aaff0ba71a099`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75474851f507bad54fde1240afe8e8675cd3e4efc177feaebfd6827dc03b482`  
		Last Modified: Thu, 26 Jun 2025 20:17:20 GMT  
		Size: 6.3 MB (6281567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e96f64006c69ac5cd0996766a85be50bc52bda9d77638f9945484be8249ca7`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599c3b4a2c9816edaebe425e51b5e596ed27ce69bbe5dce0089042c23add9303`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5bcd0e65eb6744edfa21188c85939ea1d7cda6f477a5bbaeeaacf9a38f1ff062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de0c482c58bc50b5774f0872abe58b788bda3f26499322cbd7f38a109b0f0d0`

```dockerfile
```

-	Layers:
	-	`sha256:f51693de89b45487e48ff77661b758d94f3f9e18c237c375453017a1231744c2`  
		Last Modified: Thu, 26 Jun 2025 23:56:55 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:ddd473e4e868ef144ab2d5f9abcf42c5aceb876bb300e0462eebdce5b5f4365d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9993129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3072336f828630ea7d0a85fddecbc6eabebebd8559b6776f8c147644cd82c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159dad19c10b3c7682120f345b7e0bea109f9dc391d3a6298d08bb73333d0d59`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 6.3 MB (6261972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a7da33fc1b61ecaa43d6f5263a61080be1abe619a070602456f19bceb387f9`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247bf6ec9ca48ef6c50947528477f4c16fe8962572e753fa9eedf239e7a401d6`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1e62dcb2bca95114e545acb0e8eff4519f82ce2c57e19687417b288fdbba243f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461b3c37868ee7b203fddfa4880a0d115e7eb39dec597e967526e3e5fb7a1c4b`

```dockerfile
```

-	Layers:
	-	`sha256:6350f0107c438cca60d4c50ae102aa1fe39670abe71ee66abb23ef856a39ff57`  
		Last Modified: Thu, 26 Jun 2025 23:56:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:676fffad9a719885389d89b25e2658f6b2ffa7ebf49d017b66ae4a959ebd289a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6813d2b43b6ca6d4ac54bbb01882cc4ba4237439563dab91499d3ffaf82f9e5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a12b839b5ac673697b1e2b1c5a3d8e70bc89003735107be2f7098d9a78cea3`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 6.6 MB (6627459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc76d719b63c12d9d553830608ff5b6d62b6b8850a3c833d5f108a4e723e1b92`  
		Last Modified: Thu, 26 Jun 2025 20:18:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44f6461fda1985f859fa469248cbde00cb5b9a94c750d36727a4fa2fa821f14`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6bdcd1a152276665c728f50c64b1ccd43dbdfa0f1532f221e6b409ba7bdb4550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68f9b5a91c52b3b977a6297761fe63e35ca66d3a969f7d123ac4f67e5dcd7fe`

```dockerfile
```

-	Layers:
	-	`sha256:a25179590d118b79e69af92d0c626fdfe45bf30c8a60c73d2c9e29dcb0f145e0`  
		Last Modified: Thu, 26 Jun 2025 23:57:01 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

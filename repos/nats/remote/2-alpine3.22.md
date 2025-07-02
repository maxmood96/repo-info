## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:3a20655148432a13ed0a3fbcdc877c2836cc66cd02255a4ee28351a1087a8840
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
$ docker pull nats@sha256:75dcd845381f2ff712a122a843666a0ca928750763b6d130d5c84a2f6b1ba7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10593402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c16c62680673b9b182f52191271c12304d9f77db1979e6c77b90691bdc3c4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.11.6
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4fe3c40bddc58e31012f55865df0dcd24012995d2893a4d64a0ae5cb147d7a36' ;; 		armhf) natsArch='arm6'; sha256='247ed4cd1682d5a77d93add9ebc806a9bfcac39981a9f0048678006895d3146d' ;; 		armv7) natsArch='arm7'; sha256='85044d4a4c13f910820c6727b8e748b97a6c73a6b4cb206cd77db9cab62be074' ;; 		x86_64) natsArch='amd64'; sha256='5e5272dd1bdb8da020aedc8cf883fb26c128441809a992f156e0b1ccb28ac5b7' ;; 		x86) natsArch='386'; sha256='0d601a8bd963f32597d3534a884e3a90f43400f730b666e407a0b59d16f09db9' ;; 		s390x) natsArch='s390x'; sha256='80f6cdc098aaffec4133204a0e83f9866ed379fcc274c07b129201e0e7e47e3f' ;; 		ppc64le) natsArch='ppc64le'; sha256='97ff93f6a3ef10d1bccb583d204848d93d30624dc328de8579f77e9c6c96f8f3' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122cdb2399d6870975f441bf1a1ca2f1969e34f5ca431e008f9059fb82bb971d`  
		Last Modified: Tue, 01 Jul 2025 21:10:08 GMT  
		Size: 6.8 MB (6795586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f594d6d0eae1a514a4146a3f4d2ea10ebd2c114bccedec6f8cc830ab7ef5e3b`  
		Last Modified: Tue, 01 Jul 2025 21:10:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2bc4a4407bca8cc92ea4747e15cde643a9aab963385ac0a8d160bcb8e86a9c`  
		Last Modified: Tue, 01 Jul 2025 21:10:07 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:252c15540e1a42be5f9185087393955a927ab3ddf37956138bf6545bf27d9673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157c61e718c588a74cebae0dc7ec2ae40563a315963c8ce91dd31ea7dfbe1224`

```dockerfile
```

-	Layers:
	-	`sha256:a7d7771ae564700e5c82333bf1e0d99fba68e5a6d861725012772152c66ab4b5`  
		Last Modified: Tue, 01 Jul 2025 23:56:36 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:4a4f82202485c53aacbf2950c084ac72f34ff70af36c3bd346f391f6c3fa556d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10011290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e56d77aa9d84cfe7b7c54a56716babdc93718f7db549d0ce088e0f62cec1bfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.11.6
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4fe3c40bddc58e31012f55865df0dcd24012995d2893a4d64a0ae5cb147d7a36' ;; 		armhf) natsArch='arm6'; sha256='247ed4cd1682d5a77d93add9ebc806a9bfcac39981a9f0048678006895d3146d' ;; 		armv7) natsArch='arm7'; sha256='85044d4a4c13f910820c6727b8e748b97a6c73a6b4cb206cd77db9cab62be074' ;; 		x86_64) natsArch='amd64'; sha256='5e5272dd1bdb8da020aedc8cf883fb26c128441809a992f156e0b1ccb28ac5b7' ;; 		x86) natsArch='386'; sha256='0d601a8bd963f32597d3534a884e3a90f43400f730b666e407a0b59d16f09db9' ;; 		s390x) natsArch='s390x'; sha256='80f6cdc098aaffec4133204a0e83f9866ed379fcc274c07b129201e0e7e47e3f' ;; 		ppc64le) natsArch='ppc64le'; sha256='97ff93f6a3ef10d1bccb583d204848d93d30624dc328de8579f77e9c6c96f8f3' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7573cf6f09253f2d23a95c68432252c3516bdd5f017077283eb236194d395507`  
		Last Modified: Tue, 01 Jul 2025 21:09:37 GMT  
		Size: 6.5 MB (6509390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c278f70099da334c4fb180cfcf7b9ca9f5e9d3889f744486b48769dab6edfe81`  
		Last Modified: Tue, 01 Jul 2025 21:09:36 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8870638321a087f6503918e6a3b08ba86f690318b40dbabbad3b8b906d3ff9d0`  
		Last Modified: Tue, 01 Jul 2025 21:09:37 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a3418d1b3cfffa0e42823b4a527de00e4f4384fbd537bb8f48dc808d0c5e4781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc0c1466b0286b726df52d2ca8cb8bd137eaf190b5eb98c66238fbd72344264`

```dockerfile
```

-	Layers:
	-	`sha256:83108a602a7dd082d5177d25ed19282b366db9ba037f7c550757872794dd6934`  
		Last Modified: Tue, 01 Jul 2025 23:56:39 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bb6c9e9a9c23927693038cb68c18c457588c789fbbbf401608187500702d0d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9718952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d14453815892434a4003fd658e5e732952f52a9fbf207317f234c54342c7ef5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.11.6
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4fe3c40bddc58e31012f55865df0dcd24012995d2893a4d64a0ae5cb147d7a36' ;; 		armhf) natsArch='arm6'; sha256='247ed4cd1682d5a77d93add9ebc806a9bfcac39981a9f0048678006895d3146d' ;; 		armv7) natsArch='arm7'; sha256='85044d4a4c13f910820c6727b8e748b97a6c73a6b4cb206cd77db9cab62be074' ;; 		x86_64) natsArch='amd64'; sha256='5e5272dd1bdb8da020aedc8cf883fb26c128441809a992f156e0b1ccb28ac5b7' ;; 		x86) natsArch='386'; sha256='0d601a8bd963f32597d3534a884e3a90f43400f730b666e407a0b59d16f09db9' ;; 		s390x) natsArch='s390x'; sha256='80f6cdc098aaffec4133204a0e83f9866ed379fcc274c07b129201e0e7e47e3f' ;; 		ppc64le) natsArch='ppc64le'; sha256='97ff93f6a3ef10d1bccb583d204848d93d30624dc328de8579f77e9c6c96f8f3' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa336515092c07bf57a79b626615bec6f622fef783734d3ddfeb62e7c193617`  
		Last Modified: Tue, 01 Jul 2025 21:35:41 GMT  
		Size: 6.5 MB (6498800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d6deef78122ae71071ab9d79cf240af1d0555c22fc8df562c840dbb7411783`  
		Last Modified: Tue, 01 Jul 2025 21:35:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37efc8ed03b431f1d21d3c60802d1a90f92bea4217b2c717b5fc3b72d69a445`  
		Last Modified: Tue, 01 Jul 2025 21:35:40 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:68f407575e4521e710533b0d9c0a2a784154433d9ed94d47c0ea0431d71906e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757c4f522c053aad6d42d96ec122c41b35e01cee37e2e7f19523883880d045c0`

```dockerfile
```

-	Layers:
	-	`sha256:de3afdd0d44d6b55b79554f95f93677ca04b6f698bd18f5cd5d9398289e413e6`  
		Last Modified: Tue, 01 Jul 2025 23:56:42 GMT  
		Size: 14.4 KB (14425 bytes)  
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
$ docker pull nats@sha256:975da4a9958739d97bf4f876a44c0f9f6921c1e3d152fbdb5e02f6ccbff787bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9996748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52954dc3e1110ece5120b69c9b791e691720ab50459ecac2810c8f09f157827c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.11.6
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4fe3c40bddc58e31012f55865df0dcd24012995d2893a4d64a0ae5cb147d7a36' ;; 		armhf) natsArch='arm6'; sha256='247ed4cd1682d5a77d93add9ebc806a9bfcac39981a9f0048678006895d3146d' ;; 		armv7) natsArch='arm7'; sha256='85044d4a4c13f910820c6727b8e748b97a6c73a6b4cb206cd77db9cab62be074' ;; 		x86_64) natsArch='amd64'; sha256='5e5272dd1bdb8da020aedc8cf883fb26c128441809a992f156e0b1ccb28ac5b7' ;; 		x86) natsArch='386'; sha256='0d601a8bd963f32597d3534a884e3a90f43400f730b666e407a0b59d16f09db9' ;; 		s390x) natsArch='s390x'; sha256='80f6cdc098aaffec4133204a0e83f9866ed379fcc274c07b129201e0e7e47e3f' ;; 		ppc64le) natsArch='ppc64le'; sha256='97ff93f6a3ef10d1bccb583d204848d93d30624dc328de8579f77e9c6c96f8f3' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a9a3eeb4fc05c7967af38a1710c5312c1a303542862d223f6818681835ca5b`  
		Last Modified: Tue, 01 Jul 2025 22:11:40 GMT  
		Size: 6.3 MB (6265589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db52d09318a0b4f27998f5f03c8c30aa55bc76d6b6c64249273f56a4802ae82`  
		Last Modified: Tue, 01 Jul 2025 22:11:38 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee66bfb428e85e9271b4f3cd70f90ff50c449fbf78c720cff2d7c554b9f88ef`  
		Last Modified: Tue, 01 Jul 2025 22:11:39 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:61ad2d9e707c2c44b60adee93abc5320cbce4e604e492e38ec065685de0da51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261848922d13bffd1f3d63b9fb5d08b5e34f9c09ccfd4a954d679e416cb6639d`

```dockerfile
```

-	Layers:
	-	`sha256:36a777d5bcaf7d57b3df059b915f72db841ccb06179b5b506f01aef69f378fd5`  
		Last Modified: Tue, 01 Jul 2025 23:56:48 GMT  
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

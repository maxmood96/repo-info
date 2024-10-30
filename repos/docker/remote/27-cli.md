## `docker:27-cli`

```console
$ docker pull docker@sha256:ed9cea613c166e05d8a4f467b0cb46d498bfe5b1cfa5ada3befb68124ba95abb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-cli` - linux; amd64

```console
$ docker pull docker@sha256:6f6c2f0be09997d41fb82bc66252cfcdd0bd5dd740a93b02244f261975373ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67633760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cd86e644b718f3af3a7358fd64b2549eb1c32f2e9ee1049d569912dabb6f5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 11:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 11:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1c78a611a6a25c282aea219caf7ae860410c08f5bd16b1d3e5790c7111986ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720b80106d2e0a2ce18faeecb8e5fd246f8f23c92351cf3cd8a3cf5d6eb9d8b6`

```dockerfile
```

-	Layers:
	-	`sha256:c86d7940f28917f3cd6bcd3f4e5f909c257e512b5877825edcaa1b9ab02206e9`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d371ebc3ea5ee713d92c710b479f084b3cfeff73615cc801da2fb7785f23a29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62882755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d038449f0accbc0cda483b07a3e22c67ce0a27be7a11d6aff421e2fbbf607fc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 11:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 11:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff65a1a41eeb4563c703da9df32ffde2d094c0ae65f82d2bcb7cf0356cb5044`  
		Last Modified: Wed, 30 Oct 2024 18:00:08 GMT  
		Size: 18.0 MB (17959761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab934ba2ae656f2d2940efa56165da37f05e243c1e83ca803e8de17973d003`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7148bd9d1e03160c3b2a1345fc3b1226245e9aba5fcae314396269c10e8d05c`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa2aed80a613f5df144510ecbb05b4dd3aab51c62a2444a213a0c1022e3534d`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:31f2cd1c2e409947510040b9de02891fc5fedce058605402066ca261c815cbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e109cf29049012042401160b4058d85af4046800cdd8035a4833131b093696e`

```dockerfile
```

-	Layers:
	-	`sha256:5edf06bef4f2ff3713d28a40cf02b08bdd516140d8c323afab3edc145d1d3a55`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:a6a3d8caa3ea6624c5103c34a4020967b20f45829e86577ae8569919ac645bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61916664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50e4c799822a0f54da177af4cb622a670fae9713cac7b3b510dc41367544e4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 11:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 11:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbfcbb8839fbfd6fdb568cb769e6f6260bb2b51da3add7c8243f21fa9365ae5`  
		Last Modified: Wed, 30 Oct 2024 18:00:05 GMT  
		Size: 17.9 MB (17939171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657c8762285139ce86e75531f7d61b224ab645645166fe0a0068e8df2d91e6fa`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb36e8c6823af1e364b99044bfd3e4bc8cf75477c04a886e7ab89610c6aa71`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001d4fb539565f10104ba8e77f9b51f8920384869e943c64a4cb459906eeeb0`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:060e749c6d57c33999c0644becae8a5282d83d970de879b1d1137fb2c742644d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7324f056fd668204e883c26fca1def8e884c8dbdada4c166537ebb10b22e08`

```dockerfile
```

-	Layers:
	-	`sha256:7a767fe4c51a95426ca93d4564a5c1f16bc9631dd0b9e30168b1823e9f738b43`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4839e29cb7f58c308c333423f07ca7d3c683f0d83a40ab8a7362f8cee2c1302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63894902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42131ab95cb0f60ff82078a2a1fd8d42bfad273c6f3d2c78510d547043a32524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 11:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 11:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 11:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 11:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:56433901e7dd4faa8f00e04ff9ff2c030ddabf0b57039450e3852e247ac9f10b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d74f6a63a7aa749f2a1a8caea425c496ffe1a9ab861820b9c612cd69f40c02f`

```dockerfile
```

-	Layers:
	-	`sha256:36d18b86e13e78f4e94b5f07386150b8ea9c9a4d08d1af0d10abc1791fd8dbef`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 38.2 KB (38152 bytes)  
		MIME: application/vnd.in-toto+json

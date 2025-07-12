## `docker:28-cli`

```console
$ docker pull docker@sha256:13f8f54e0410b262768c3f9ec6fb987abd385ef2b16d43cfe44b93f2042ba399
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

### `docker:28-cli` - linux; amd64

```console
$ docker pull docker@sha256:ad955c02a8c8608a9a581c545b93b9d45023986553a9188da71ec2192ff9e2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75423937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29b7161492868d2bdab426c00ecf1a97e6d4249e4ce3e9e9ed98bae0dbbe7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1c4894165cfb9aaa1d2b37c50b551c31e17f71611b0ff43994110a9b460af8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b9edd62480bf1994af5564b8ef182210d1336ff8892988f674ac27eaa5409`

```dockerfile
```

-	Layers:
	-	`sha256:fa1e8a11e4b8700fd3f91f6b363c3d23547ee308f1f0d69290d84031153575c7`  
		Last Modified: Fri, 11 Jul 2025 23:07:32 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:8b4a77177bb41dfbc484ffe2ca57773c9b8db3500a60596c0c259046d921d9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70384659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba833a381a4a0c18807371500fc2aba2f2538af694704e84f6be80a939ee3647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8d3de6ba8edd719f37c314ec9cb77ea92b3d9d7f3f43c4c8ccea5eab52d8bb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2de72b3b92515f3652b0c952bfd400180132ca92a98560966b78338b05a665b`

```dockerfile
```

-	Layers:
	-	`sha256:5d3aff152b821f9c64b37aa8c52a44adc9ee1104f48e48fc42bf63f8a0b7bf05`  
		Last Modified: Fri, 11 Jul 2025 23:07:22 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2dfe76be879889721d4578609d8e57a681a1fb944f4ee8652de2f7b18fc04ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69389623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fa5a9d9861537caf7e62f6e3199c9cb97e9eb11907b3db24c2abb801d6e6f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f79f1a874c76d5e4b265a72dccb83bc513d7ff7f30bb0ba963bbfa5b82b9742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f65cbf035a05096f98a920c5dc0ba5979f0b9ce6ab023e58ca0ed9fe5f104c3`

```dockerfile
```

-	Layers:
	-	`sha256:6d694569211f0463fc2fa67fce30fbf7c91f557b6dc9aac14c0c6b9596e073fa`  
		Last Modified: Sat, 12 Jul 2025 02:07:45 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:29a155d2b64ee1f8ea9f51d52d109a94ad34178e8b4b9d62e645c96927a3119c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70970597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713cb7ebce506a192fd70fdda571e5ddf72f0815bed6363d998882208650b019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ca067feba0aa873cd74f3722c31ec7bf2065db5e8bad3bcbb2c0bbe4865da7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7747c774e4dc3eb0e4be57c7b98e8671a22cc51fcb182bc1a244be14f544cf30`

```dockerfile
```

-	Layers:
	-	`sha256:bbfb6f21e3789c8273c69cde35a76a93414d225c4f06c24482a778ab4dd42681`  
		Last Modified: Sat, 12 Jul 2025 02:07:48 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

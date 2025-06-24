## `docker:rc-cli`

```console
$ docker pull docker@sha256:cec00f8c556496614576fb002a9d743936835b5a11fc2168e7d701315bb8de8c
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

### `docker:rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:e9f37e412b02c5169a6ec9de4da058e89e07e8b02c4879eff0b180da3444617f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75383899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e9d87bea79d20dc49837bc33646191d90633337597f3a604bca41e190e1f2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_VERSION=28.3.0-rc.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-x86_64'; 			sha256='95db7bb2ed5d5fc790a12559b9092d641637c2d0190939c282b52a7af572a8a7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv6'; 			sha256='863412d376cb1341e2a6889aa58dc4b674a58350ceccc357c71284109a5cb4a2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv7'; 			sha256='33aa26709150e835992a8af58d590e32151473f78daea549ccd70bd5f96c3bbf'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-aarch64'; 			sha256='d2c195cf553e55d06761c192133a6a7b4d67d275c7f5ce673bbf8ecf20814061'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-ppc64le'; 			sha256='6c72243b9585cc741c8e90937fd28ca2c8f2fee8a7636b30d1bbf312df27e157'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-riscv64'; 			sha256='8448828a5fa46170b92fec62d928b753ba91e86cccace24a04187324b65836ac'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-s390x'; 			sha256='39d47d8aa2cec059b4dc5e9b627a1176bcce33d9090f237806cf59264fe55e89'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Jun 2025 17:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9d79f8211ca5f0ae319dd670ed871de8854629c84d10d10a509a74ea71a120`  
		Last Modified: Mon, 23 Jun 2025 22:43:37 GMT  
		Size: 8.2 MB (8207450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dd1c3fe042ef8c0b31892371d122ab71a3531aac39c36990641881d5c775ff`  
		Last Modified: Mon, 23 Jun 2025 22:27:06 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491a95b3e7e4594569a69d79611329fd849b4550a78887833d19b66878adefe3`  
		Last Modified: Mon, 23 Jun 2025 22:43:37 GMT  
		Size: 20.5 MB (20460214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2052eec1fcdfd51e52eb33466259175cb3754349653c558b4da839ad60857c2`  
		Last Modified: Mon, 23 Jun 2025 22:43:37 GMT  
		Size: 21.7 MB (21664161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2891f97182d20dcefb7f871b1bd7780ce831bc5c005bb1dc44c9f2da5e671f6`  
		Last Modified: Mon, 23 Jun 2025 22:43:36 GMT  
		Size: 21.3 MB (21253077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ac2a2bd86dee4e9a6511d9fc00935fb504452c468892b5a6b6639048eb8579`  
		Last Modified: Mon, 23 Jun 2025 22:17:52 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9334a663f6014177b797e46f1ac25aeac8622400c2284a31f2490cac85fe1f8`  
		Last Modified: Mon, 23 Jun 2025 22:17:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d7f75badbcca98d88f6930538405d39877707cb617b5517d2f8d8a101e2e07`  
		Last Modified: Mon, 23 Jun 2025 22:27:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1b30f2b3d25c7c1691f9ec7546bd08b425690235466aa02e3b893c4e8020766c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd98aef02d30f551cdb4121a8627828c20d97cd429b12f32ca0132b33804323d`

```dockerfile
```

-	Layers:
	-	`sha256:712abbd597e2e8b1177d304863e898e0e8b73116e6f220083bbd65559f93e8e1`  
		Last Modified: Mon, 23 Jun 2025 23:07:50 GMT  
		Size: 37.9 KB (37911 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:5bd6cd7fe6887f61f311d7f129c5286c33a7e4348b60d4de1cac67c071e7b603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70361280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3365afc0d83d41b552e0356170d95263710ea02bf56d68621e9bc94186ef7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_VERSION=28.3.0-rc.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-x86_64'; 			sha256='95db7bb2ed5d5fc790a12559b9092d641637c2d0190939c282b52a7af572a8a7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv6'; 			sha256='863412d376cb1341e2a6889aa58dc4b674a58350ceccc357c71284109a5cb4a2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv7'; 			sha256='33aa26709150e835992a8af58d590e32151473f78daea549ccd70bd5f96c3bbf'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-aarch64'; 			sha256='d2c195cf553e55d06761c192133a6a7b4d67d275c7f5ce673bbf8ecf20814061'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-ppc64le'; 			sha256='6c72243b9585cc741c8e90937fd28ca2c8f2fee8a7636b30d1bbf312df27e157'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-riscv64'; 			sha256='8448828a5fa46170b92fec62d928b753ba91e86cccace24a04187324b65836ac'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-s390x'; 			sha256='39d47d8aa2cec059b4dc5e9b627a1176bcce33d9090f237806cf59264fe55e89'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Jun 2025 17:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
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
	-	`sha256:5b2281c641e0de8eb8b7ec7c84c71df62fad9a9632a697e1a208c9d668be097b`  
		Last Modified: Mon, 23 Jun 2025 22:44:17 GMT  
		Size: 18.5 MB (18451269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fef49d56e1271163386b8af9dde5468e6b3428f7c90ddb1c7cc8d1b7d10f4e`  
		Last Modified: Mon, 23 Jun 2025 22:44:18 GMT  
		Size: 20.3 MB (20295406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ac1acc178ba67f713270fe97d865676866ff0395f2988a3254e3e05e7f461e`  
		Last Modified: Mon, 23 Jun 2025 22:44:17 GMT  
		Size: 20.0 MB (19996847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65a1531a3f3d593d7f50ee549c9a688399cc7862b82c43e59215ad0f9a38131`  
		Last Modified: Mon, 23 Jun 2025 22:25:40 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a191dff3c1446b6c0796143c4e27ff9a4af69eeb73dc05507d6c4dbd03e51b`  
		Last Modified: Mon, 23 Jun 2025 22:25:42 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31622548211e6f9f475e5552c950f4e38692f510721cb83c6630f6464fafb561`  
		Last Modified: Mon, 23 Jun 2025 22:25:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:034e04c6cb7f1f4b31339e6ee0a0c8160934ad6d556441479ca29fedc954b488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b76a3d2e901b795ee9c548f038352eea7717d6a0b8484246a1a6bc9e5cd5ad`

```dockerfile
```

-	Layers:
	-	`sha256:72d090c18a52c932f51323121ee56b723df58aacb1faf37494c0a19dabc74574`  
		Last Modified: Mon, 23 Jun 2025 23:08:03 GMT  
		Size: 38.1 KB (38065 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:72e837915f760f84996839b5e5cd945aa8078bc29736dea7fecc76461cca1e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69353654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56adba2dbd5c84baecf85714369d288e13bf795616b1127f3ae4b87f7e8075`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_VERSION=28.3.0-rc.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-x86_64'; 			sha256='95db7bb2ed5d5fc790a12559b9092d641637c2d0190939c282b52a7af572a8a7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv6'; 			sha256='863412d376cb1341e2a6889aa58dc4b674a58350ceccc357c71284109a5cb4a2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv7'; 			sha256='33aa26709150e835992a8af58d590e32151473f78daea549ccd70bd5f96c3bbf'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-aarch64'; 			sha256='d2c195cf553e55d06761c192133a6a7b4d67d275c7f5ce673bbf8ecf20814061'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-ppc64le'; 			sha256='6c72243b9585cc741c8e90937fd28ca2c8f2fee8a7636b30d1bbf312df27e157'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-riscv64'; 			sha256='8448828a5fa46170b92fec62d928b753ba91e86cccace24a04187324b65836ac'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-s390x'; 			sha256='39d47d8aa2cec059b4dc5e9b627a1176bcce33d9090f237806cf59264fe55e89'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Jun 2025 17:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f034cf5cbb8b182c27094ccc628bdc2119d78915c0f51cbaae5687f639b92a`  
		Last Modified: Mon, 23 Jun 2025 22:17:13 GMT  
		Size: 18.4 MB (18436007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa8f044e40f23a2f6eda0e546e32e6b4e5f2ac8e29e8f234d30eb4231bafa3b`  
		Last Modified: Mon, 23 Jun 2025 22:17:13 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cd530f514402571b10e0dbeefeb5674f299072efdd18967f62e38848ce0bbe`  
		Last Modified: Mon, 23 Jun 2025 22:17:13 GMT  
		Size: 20.0 MB (19972897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8608ed12060c2620d03e1c120903b83fd166587ea847178ee58e3e3522757c3c`  
		Last Modified: Mon, 23 Jun 2025 22:17:11 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed5430b0f2272bc539665886de53b48303a575f6ba94572d1e87042b2b38082`  
		Last Modified: Mon, 23 Jun 2025 22:17:12 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beac9f814c5afb6239eded97a9af90c15d4670e4548493c5ff08fcf8cf824bd`  
		Last Modified: Mon, 23 Jun 2025 22:17:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:58190ea1a39af4f3aafa196c44ee4a1cf6f976bce17bb5852225cfe094452ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4c123ba07165d71b0f20f308d4cc8de0ab923dd9c7ba901e93c8f72e25a532`

```dockerfile
```

-	Layers:
	-	`sha256:c733c462926e5694225ebdf5b7ba118fbbed238431162c541baebfdd3880a6d6`  
		Last Modified: Mon, 23 Jun 2025 23:08:17 GMT  
		Size: 38.1 KB (38064 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:151edd4c6011d9356d12053b0ce3d3ce3940ccf7681798b42251b98cfce8de01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70941241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57d3c402eaeff297513e888d0c38b13ee5166458f45d344ff5a6c06798359ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_VERSION=28.3.0-rc.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-x86_64'; 			sha256='95db7bb2ed5d5fc790a12559b9092d641637c2d0190939c282b52a7af572a8a7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv6'; 			sha256='863412d376cb1341e2a6889aa58dc4b674a58350ceccc357c71284109a5cb4a2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv7'; 			sha256='33aa26709150e835992a8af58d590e32151473f78daea549ccd70bd5f96c3bbf'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-aarch64'; 			sha256='d2c195cf553e55d06761c192133a6a7b4d67d275c7f5ce673bbf8ecf20814061'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-ppc64le'; 			sha256='6c72243b9585cc741c8e90937fd28ca2c8f2fee8a7636b30d1bbf312df27e157'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-riscv64'; 			sha256='8448828a5fa46170b92fec62d928b753ba91e86cccace24a04187324b65836ac'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-s390x'; 			sha256='39d47d8aa2cec059b4dc5e9b627a1176bcce33d9090f237806cf59264fe55e89'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Jun 2025 17:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97387c91ee3c7373fcee444a1b646ca70965b590344120d317908c147a2b1ca`  
		Last Modified: Mon, 23 Jun 2025 22:17:14 GMT  
		Size: 8.2 MB (8229009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dd6fd942c69d848277a60172548feb0fa2621741c486ffbfea35c861a0b6ba`  
		Last Modified: Mon, 23 Jun 2025 22:17:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2fae78b07b72b55406cc9af117544dab46fca428d0a5bba5b14d8a585838ff`  
		Last Modified: Mon, 23 Jun 2025 22:17:14 GMT  
		Size: 19.3 MB (19267905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8bce1b6cf15a61d47b8888b5714ea47d844d46c355a5f154f7735d18603c24`  
		Last Modified: Mon, 23 Jun 2025 22:17:14 GMT  
		Size: 19.8 MB (19819446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beab20993d24bc858c2c5a5172f2996980b66aed8d0e004cfdcf056df6f33694`  
		Last Modified: Mon, 23 Jun 2025 22:17:14 GMT  
		Size: 19.5 MB (19486789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af553b5792cc05d1e2713d1fcd588572300a08ab5a0be3403423b3ba1c97b84`  
		Last Modified: Mon, 23 Jun 2025 22:17:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133afbf723fb46838c04b12d78546b52fa59100bdf4d900b0d0a20f645b578db`  
		Last Modified: Mon, 23 Jun 2025 22:17:13 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dec9abfd3cc049bc95f125f1a628efbba68a7450da771ee5a217c0860379e8`  
		Last Modified: Mon, 23 Jun 2025 22:17:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7d48dd0f4009b5db8e6281384f21e00a224aa380ed58aca9513acf7f4a9b2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0ebdb551c3986aecf7c6f174b6734503ef15cd0f6f62246358d4e8a856a10b`

```dockerfile
```

-	Layers:
	-	`sha256:a935efe0345f64ef7c5895e4b0115557d767cbaf0967a22be16d2da6b697a43b`  
		Last Modified: Mon, 23 Jun 2025 23:08:31 GMT  
		Size: 38.1 KB (38105 bytes)  
		MIME: application/vnd.in-toto+json

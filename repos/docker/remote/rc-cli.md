## `docker:rc-cli`

```console
$ docker pull docker@sha256:e3ac863cdee5b9995eb4786f3ac35c16b8bf6a49a618f75920fd677f64d91a90
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
$ docker pull docker@sha256:b21f7e3eb6994c1a3ddfabd7e41347b0c3a14305e38b680d783d6c8e85299fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75373128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee866979e73a2481a3ebad0621c40b7fbaae61624843c2aa9906f04134f8f40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 20 Jun 2025 17:06:07 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-x86_64'; 			sha256='95db7bb2ed5d5fc790a12559b9092d641637c2d0190939c282b52a7af572a8a7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv6'; 			sha256='863412d376cb1341e2a6889aa58dc4b674a58350ceccc357c71284109a5cb4a2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv7'; 			sha256='33aa26709150e835992a8af58d590e32151473f78daea549ccd70bd5f96c3bbf'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-aarch64'; 			sha256='d2c195cf553e55d06761c192133a6a7b4d67d275c7f5ce673bbf8ecf20814061'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-ppc64le'; 			sha256='6c72243b9585cc741c8e90937fd28ca2c8f2fee8a7636b30d1bbf312df27e157'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-riscv64'; 			sha256='8448828a5fa46170b92fec62d928b753ba91e86cccace24a04187324b65836ac'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-s390x'; 			sha256='39d47d8aa2cec059b4dc5e9b627a1176bcce33d9090f237806cf59264fe55e89'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Jun 2025 17:06:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Jun 2025 17:06:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24b25e004d4867df8e9bf0324bf4d49a3ed9d26c566af3c69a6ece667cdd4d1`  
		Last Modified: Fri, 20 Jun 2025 19:46:35 GMT  
		Size: 8.2 MB (8207454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed7b3b3424b2f3627c5c7b88bd9dc656167d18358b1211de725e224aede6ced`  
		Last Modified: Fri, 20 Jun 2025 19:46:31 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf79ea00eefa87bf1fa4bdae44f4d91182fc627123d4a7a58d95a5e9256c4bd7`  
		Last Modified: Fri, 20 Jun 2025 19:46:32 GMT  
		Size: 20.4 MB (20449419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51146fa69b36c259dc9d3d4982b64d97e0aba79940cc20e463604ee2f76ee30f`  
		Last Modified: Fri, 20 Jun 2025 19:46:34 GMT  
		Size: 21.7 MB (21664160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a6e3bb58f0ed305c3089d1005149354b86e045a63d53eaca8bd21b242db46a`  
		Last Modified: Fri, 20 Jun 2025 19:46:35 GMT  
		Size: 21.3 MB (21253094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78ac15c753d03fb45dc128620313c5a6255b9fddbe608dea405ac40dc3a0db2`  
		Last Modified: Fri, 20 Jun 2025 19:46:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267183a39bafcd62e9ec9c6903f7b92837941af2459e45683c6c2e7611aff7e1`  
		Last Modified: Fri, 20 Jun 2025 19:46:26 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117b6b5c9054f6422e5e9544a562400d561ed596bb77ec953701bdc4e37a985`  
		Last Modified: Fri, 20 Jun 2025 19:46:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a80ccc63f94fbd80364f8ceca1feffb01189929ee87ab31e95b05843ac439492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12b5c547a3da3cabc151b6a307bdbc2771f7e18ad0bc152c814a06dd639486c`

```dockerfile
```

-	Layers:
	-	`sha256:e821a0d80f6183e061acdc50cc526138e209ff4e3cd43140fffe8951d0c8694e`  
		Last Modified: Fri, 20 Jun 2025 20:08:17 GMT  
		Size: 37.9 KB (37911 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:91493573c3eda9d6590b58d1c7e4ca6cf77c44a2dd190217cce2012bfff728a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70349749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2377c05eb8cf3f457d615b02716598a8e58cd5865b55990e5d5a2bb0c56f2fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 20 Jun 2025 17:06:07 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-x86_64'; 			sha256='95db7bb2ed5d5fc790a12559b9092d641637c2d0190939c282b52a7af572a8a7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv6'; 			sha256='863412d376cb1341e2a6889aa58dc4b674a58350ceccc357c71284109a5cb4a2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv7'; 			sha256='33aa26709150e835992a8af58d590e32151473f78daea549ccd70bd5f96c3bbf'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-aarch64'; 			sha256='d2c195cf553e55d06761c192133a6a7b4d67d275c7f5ce673bbf8ecf20814061'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-ppc64le'; 			sha256='6c72243b9585cc741c8e90937fd28ca2c8f2fee8a7636b30d1bbf312df27e157'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-riscv64'; 			sha256='8448828a5fa46170b92fec62d928b753ba91e86cccace24a04187324b65836ac'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-s390x'; 			sha256='39d47d8aa2cec059b4dc5e9b627a1176bcce33d9090f237806cf59264fe55e89'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Jun 2025 17:06:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Jun 2025 17:06:07 GMT
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
	-	`sha256:97f99a1571c0a4c2a8c2870a2345fc187c92332a6b9e629596a05ba4a9e470dd`  
		Last Modified: Mon, 16 Jun 2025 20:08:12 GMT  
		Size: 18.4 MB (18439697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6581ea897732bcf50ebfc1e7579e515885b0684f6b2be4dab5a769a7505002e`  
		Last Modified: Wed, 18 Jun 2025 16:46:18 GMT  
		Size: 20.3 MB (20295407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731ed116bd1d0e7b6bc53a15af909e6022642c4c06c39ef859f9dae6d6a752e6`  
		Last Modified: Fri, 20 Jun 2025 20:04:22 GMT  
		Size: 20.0 MB (19996878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de19a6687a2cd26893cdf9fbe66c23418f25e09e1b3b5dec925920db3340710`  
		Last Modified: Fri, 20 Jun 2025 20:04:20 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4e01a80764e3d0ee3274d05504e11adad1b4a9269f80758a8ab927e912091`  
		Last Modified: Fri, 20 Jun 2025 20:04:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428118f9ca719709ecda39a13ee64c778189bf55ce6d5314f82b72caf197dc08`  
		Last Modified: Fri, 20 Jun 2025 20:04:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dd386b2641f000b9ce399ab68b9745bd354237fd5d68c6ed6ab4364abbe480b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb3fecbc83a89c4ac8c83669ee2c2408b606a033861efab52324183939a552c`

```dockerfile
```

-	Layers:
	-	`sha256:6a587adce1526636a2089138c49b58fbd40e2d5a41f3d05661d988aa54a5939a`  
		Last Modified: Fri, 20 Jun 2025 20:08:20 GMT  
		Size: 38.1 KB (38065 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:968d32ca8d4f0e96f4f0643b2937ec6135afd2497e2280d1244a26bdc8a26782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69342804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a73fa49e10995de1bc42717ca7029f6df2d28bef78c2c8ea849e9453da5ece5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 20 Jun 2025 17:06:07 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-x86_64'; 			sha256='95db7bb2ed5d5fc790a12559b9092d641637c2d0190939c282b52a7af572a8a7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv6'; 			sha256='863412d376cb1341e2a6889aa58dc4b674a58350ceccc357c71284109a5cb4a2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv7'; 			sha256='33aa26709150e835992a8af58d590e32151473f78daea549ccd70bd5f96c3bbf'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-aarch64'; 			sha256='d2c195cf553e55d06761c192133a6a7b4d67d275c7f5ce673bbf8ecf20814061'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-ppc64le'; 			sha256='6c72243b9585cc741c8e90937fd28ca2c8f2fee8a7636b30d1bbf312df27e157'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-riscv64'; 			sha256='8448828a5fa46170b92fec62d928b753ba91e86cccace24a04187324b65836ac'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-s390x'; 			sha256='39d47d8aa2cec059b4dc5e9b627a1176bcce33d9090f237806cf59264fe55e89'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Jun 2025 17:06:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Jun 2025 17:06:07 GMT
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
	-	`sha256:9cbd793afb45678a56953ca06564d25edce92df36302f47aed10537bf8a6dc87`  
		Last Modified: Mon, 16 Jun 2025 18:08:14 GMT  
		Size: 18.4 MB (18425152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083c38f65dd00533393ef5bdca2314d20f63160bc0ebc5069be0d652dfd051c3`  
		Last Modified: Wed, 18 Jun 2025 18:09:57 GMT  
		Size: 20.3 MB (20282776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4fef19a28c5ba4e4e77fd8d92c2c7ea9763ee1e8211eabd63d46506c8c2df6`  
		Last Modified: Fri, 20 Jun 2025 20:04:29 GMT  
		Size: 20.0 MB (19972905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd91a5c37c1d9d640f2d8afe2c7b77323f73ee691fe68d84dacc55514209bc9f`  
		Last Modified: Fri, 20 Jun 2025 20:04:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8e3a2e247f46f6069e7ac92f828dd62e0a5241ba7853fd400f08eb23b07c33`  
		Last Modified: Fri, 20 Jun 2025 20:04:28 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d27217022cea1b614a58a48fb3519552cc7a0addfb7c0f72a06d440f186fc9`  
		Last Modified: Fri, 20 Jun 2025 20:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6d75432345f541782cd20b8ef0e612c4b4a49936d48d780bf9e18005d0b839d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ae00ae4fc0867918f25bd77a1a74147af68fb81bd889ca742543a61e864f98`

```dockerfile
```

-	Layers:
	-	`sha256:37916fe44fe36c5b1fd42c58a2249d304d324a3ac93a59a2f1126d09db339ef3`  
		Last Modified: Fri, 20 Jun 2025 20:07:31 GMT  
		Size: 38.1 KB (38065 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:213248a1ffc0891fadf9bfe055028bdc5fa96ae496cb4088f6c126c1c985b33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70931879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb65a0f87cd91961c228b444a2c8f2da36397b00e0c9c1c1d8fd79ec2aecd4c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 20 Jun 2025 17:06:07 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Fri, 20 Jun 2025 17:06:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-x86_64'; 			sha256='95db7bb2ed5d5fc790a12559b9092d641637c2d0190939c282b52a7af572a8a7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv6'; 			sha256='863412d376cb1341e2a6889aa58dc4b674a58350ceccc357c71284109a5cb4a2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv7'; 			sha256='33aa26709150e835992a8af58d590e32151473f78daea549ccd70bd5f96c3bbf'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-aarch64'; 			sha256='d2c195cf553e55d06761c192133a6a7b4d67d275c7f5ce673bbf8ecf20814061'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-ppc64le'; 			sha256='6c72243b9585cc741c8e90937fd28ca2c8f2fee8a7636b30d1bbf312df27e157'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-riscv64'; 			sha256='8448828a5fa46170b92fec62d928b753ba91e86cccace24a04187324b65836ac'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-s390x'; 			sha256='39d47d8aa2cec059b4dc5e9b627a1176bcce33d9090f237806cf59264fe55e89'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Jun 2025 17:06:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Jun 2025 17:06:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Jun 2025 17:06:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dd1a3f6c33f5cb4f37f8a56f360f53067b0e0c52a924ced150a71eab35066c`  
		Last Modified: Fri, 20 Jun 2025 20:04:23 GMT  
		Size: 8.2 MB (8229008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7ed8201efef3688d822f65774ebbec704be1fc5c71723142c2628f11933482`  
		Last Modified: Fri, 20 Jun 2025 20:04:22 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e78bf25dca30752d82e6bddad59edc9899c6fdcb877d7a16d85f0f38cce0369`  
		Last Modified: Fri, 20 Jun 2025 20:04:25 GMT  
		Size: 19.3 MB (19258549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d7a71f18a9bfeb3b114e6e1a961e864dad04504c6a90f0437ff8f7695eec14`  
		Last Modified: Fri, 20 Jun 2025 20:04:25 GMT  
		Size: 19.8 MB (19819435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce0534fae0833a84160e165b0eda0a2f609736bb468f1f0df36eec2f01b4fe1`  
		Last Modified: Fri, 20 Jun 2025 20:04:24 GMT  
		Size: 19.5 MB (19486792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f76b94e03cee9aeaf6952edd25fb087b82db9f71d7e705d84e0a134a439bfa9`  
		Last Modified: Fri, 20 Jun 2025 20:04:23 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3d6e68218c305c7763fc5dde69d9f85cde732d7a25ecce44ae55f02e82d038`  
		Last Modified: Fri, 20 Jun 2025 20:04:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb123f0f3894ccb3286ad43cf84efe72bbbb7d16227006454d96ec7fd7ccdcf`  
		Last Modified: Fri, 20 Jun 2025 20:04:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c6ea5d6d1857a9845cfd321b67558c09f56a7aecb9a9677cc443cfad05ceed9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32ca38c82be68d05437bbef0968b2036dacf2925488feb5164aba8c72ae8733`

```dockerfile
```

-	Layers:
	-	`sha256:ff7f57e6e5388b54c57d3efc111b1396462093e753030824f9d9d74b755d0f30`  
		Last Modified: Fri, 20 Jun 2025 23:08:20 GMT  
		Size: 38.1 KB (38103 bytes)  
		MIME: application/vnd.in-toto+json

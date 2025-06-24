## `docker:28-cli`

```console
$ docker pull docker@sha256:280d9e6dbdeece0237d9ead6e5fbd59141ab1bce1ee7987760448809b8ea27aa
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
$ docker pull docker@sha256:00e4668f36d0d12ab86fd41ea7a10bd62f1c1802ccaf2240d00e845ea5c3c39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75009771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c085980853fedaf2da07bd7dc5fd7a26fbdef2dc119c1d798b0b088ed5ef2c9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 17:04:19 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_VERSION=28.2.2
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 24 Jun 2025 17:04:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Jun 2025 17:04:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cc65efafcc08e79f71dae731e77e28d1d80b4e8ada17ff88b5734eddd8b2a5`  
		Last Modified: Tue, 24 Jun 2025 18:25:51 GMT  
		Size: 8.2 MB (8207465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d63cea5f093cb52e5db9c867ae989a06e7aa8da3e8b641acc40e3852a0b4a33`  
		Last Modified: Tue, 24 Jun 2025 18:25:51 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fb40a929fb94e74bfc7e12be73679efd7271a4a832ad71824a755c5fb98d52`  
		Last Modified: Tue, 24 Jun 2025 18:25:53 GMT  
		Size: 20.1 MB (20083032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4342d14bbc36cd4e7aca95e3da1601d37ac7d360ab3d1d2bc560921c779ac753`  
		Last Modified: Tue, 24 Jun 2025 18:25:53 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d7f0dca0e6ae8d3a54dc81a69eec3ed30d6f55304e7773186be2189f138654`  
		Last Modified: Tue, 24 Jun 2025 18:25:54 GMT  
		Size: 21.3 MB (21256113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33796bdf7104804d345eff4b4d83b52dfb7df5a630e8b745206114b8c3f0d83b`  
		Last Modified: Tue, 24 Jun 2025 18:25:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559fe81ecb98d50e6277594d9e182689dc4b1171a719ea5c67e66b714df0ac2e`  
		Last Modified: Tue, 24 Jun 2025 18:25:52 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34494de11e2361be041ad92d059656cb7c6769e655c88af2fea2a8ea9eb01f3f`  
		Last Modified: Tue, 24 Jun 2025 18:25:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9d5485e6806ab42a6078bbf961d1d87f91cc0bc676434bea10c7b5192851cd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9349e5cdf219ca403e927934e1fe3d75f5d1296fb5eda327e4878c1eb3f00526`

```dockerfile
```

-	Layers:
	-	`sha256:20643c29235dadc70db628886bc3922fe49c9202d1575ea6b907cd8997791db5`  
		Last Modified: Tue, 24 Jun 2025 20:07:35 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:0e34eaa89655735ffc6ed841defd4d628f7ee36e444ea6f666cc117f9fdfcd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70010101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd0d3efffd785dab36ebf3a0b0f43a76d480c66c7005d2cba2c23214c22f049`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 17:04:19 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_VERSION=28.2.2
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 24 Jun 2025 17:04:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Jun 2025 17:04:19 GMT
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
	-	`sha256:3156c3bcd5598f721d5e807804df7256e282bd2897ea9f9f029b3cd93a5ff79b`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 18.1 MB (18101909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7e0b043c733ae1aee347b8ba6a9aae25fafbfbfec6a59a5f4b8f169a3e7aef`  
		Last Modified: Wed, 18 Jun 2025 17:07:51 GMT  
		Size: 20.3 MB (20295382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6791281677ad3a20edccf9a75502a82c53c75abe55f36d8cc828c1b63cd2b9e1`  
		Last Modified: Tue, 24 Jun 2025 18:26:18 GMT  
		Size: 20.0 MB (19995044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70a2bc248784a99fe9e1747e9710a08d3916a702ff6049aa1c3ee46f244ba9b`  
		Last Modified: Tue, 24 Jun 2025 18:26:17 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6050bd39416a4f9fe6e5c2aa5a58ee97059983f6e8e2bce7d40354a7abc33a6b`  
		Last Modified: Tue, 24 Jun 2025 18:26:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a15373bb534c20c24fbd5c44c84308b8b0a4983b9ad5bffe6418752bde420d8`  
		Last Modified: Tue, 24 Jun 2025 18:26:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bd3d6d7b8de084d757e4dfb4e5f2ccefe5856717fb569cc52c2551f8595b94d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c10794426735a8a781478b469582029c61cf68033067d982de9c3d63182b52`

```dockerfile
```

-	Layers:
	-	`sha256:d391138e58ac64b6aeba7b794af9100b011f48cd4d9c620c08485860e17c0a2d`  
		Last Modified: Tue, 24 Jun 2025 20:07:39 GMT  
		Size: 38.3 KB (38275 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:22a8a6cda54f2b3859923a3eaeaca107f1170c0ddc2b1646fad4131fdf939e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69007264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9543f18dc46e5ef934cd15e666be5459919b3c3c31c738493cc65e4fa184ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 17:04:19 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_VERSION=28.2.2
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 24 Jun 2025 17:04:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Jun 2025 17:04:19 GMT
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
	-	`sha256:c706fc5902012930a32f06fbb17943253a98c5d34ba1ad212a51f277228a4837`  
		Last Modified: Wed, 18 Jun 2025 20:07:54 GMT  
		Size: 18.1 MB (18089392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37448d2ec3f7bad1f74af640d2ae105cdfb0ca3d2aef3eadafd768d84c0bcda8`  
		Last Modified: Wed, 18 Jun 2025 20:07:55 GMT  
		Size: 20.3 MB (20282789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0d187aae514b10703ab1b0032917f17f5b2c50bbd966331ff3d2152350c47d`  
		Last Modified: Tue, 24 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19973112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee73f9f30f09898800d3553b2b4e548a4cdfc3c90bd1f27d8af26779a3176aed`  
		Last Modified: Tue, 24 Jun 2025 18:43:27 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6da77713c8a8a11bae4eab959383da3268a9a140bb02227c9b6a2bec4794d9`  
		Last Modified: Tue, 24 Jun 2025 18:43:30 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4003bd771529ce054c3a559298f8ffa88ae507c72de81bbb1d2b661b742529`  
		Last Modified: Tue, 24 Jun 2025 18:43:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9cf6c4ddb1a0ad5c3978befcaef14c073cd769941c2da309f481e3c79bbfc10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c0d6a3efc8a0c556ec769076c8b3f6e8ee85c43e47bfb52e7e6a0d49db3072`

```dockerfile
```

-	Layers:
	-	`sha256:d05d3186d6cbac3e904d6abae4c6c0dc2212bafafd439ca69d2e07f60a9532e9`  
		Last Modified: Tue, 24 Jun 2025 20:07:51 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:484aeff3e1e644ed141a6587994f0210751908fa331e2c271b52cd57a469eae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70575487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e9762dcaac7e19c228dffad117c8d51974fc5d03a543521ce6804426524f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 17:04:19 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_VERSION=28.2.2
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Tue, 24 Jun 2025 17:04:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 24 Jun 2025 17:04:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 24 Jun 2025 17:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Jun 2025 17:04:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c09c12dc876098db6faf127232f099623dbbbd3cf517f8246c8e5a8693e4f0`  
		Last Modified: Tue, 24 Jun 2025 18:27:47 GMT  
		Size: 8.2 MB (8228991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9495848de01826cc1e9f97b4397c76a8e5a50477e0ec7feb5d771d0911cc3918`  
		Last Modified: Tue, 24 Jun 2025 18:27:45 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a4c5587a885f488c1b2f7bd2d5d32c10b81adac78c6f4cae59b7d3ffacc4c0`  
		Last Modified: Tue, 24 Jun 2025 18:27:58 GMT  
		Size: 18.9 MB (18902603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0440c711470911bab6b20e4bff43ae46bc807cfb50baad00736c85ef6ee037`  
		Last Modified: Tue, 24 Jun 2025 18:27:59 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfc89a1b69a15d2139349e50f73a98ddb63456d8d3b225411d135bea009a5b`  
		Last Modified: Tue, 24 Jun 2025 18:27:59 GMT  
		Size: 19.5 MB (19486365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7784f7f21537b654c4293cc583ba7c3d9a18e7acd718257c48d94bd517286fe`  
		Last Modified: Tue, 24 Jun 2025 18:27:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bf71c0421d5c63713f96809b651570077f7fc8485542df3ed287ba4166a3ad`  
		Last Modified: Tue, 24 Jun 2025 18:27:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854c48005dea8fe0d9b72fccbcd05edf5bce65fdd68e88de3341f581e3864b54`  
		Last Modified: Tue, 24 Jun 2025 18:27:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7d1ee120cf53a35fa476df51880745ebb1dd7565d8311406c44657b8b493a451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e349cc8f91cf072e5717fd9120cea3decfe30aa5605ddda46de57cc5ee4a33f`

```dockerfile
```

-	Layers:
	-	`sha256:e910c90d40268974fdaf394a2a45ae1caebd04c489736e88990e92399535f1dd`  
		Last Modified: Tue, 24 Jun 2025 20:08:05 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

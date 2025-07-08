## `docker:cli`

```console
$ docker pull docker@sha256:e7af7b563daef7d716da1552508222bbd343d628341059ed448f7e6b18a62b98
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

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:85b2b37853090b68f2bec9b58a28c514aa4a92821231590662d961ec69ca3bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75408319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0884f72ce3334bfac5c84db32abe1dbd7d6d3b0eaeda1735e8e1c5017582741b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6e8ad138fd78450c30c813f8090cdde12769d5d73beb9c3074783e319a24839d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bceb0017eb30fe94b56cfaebf3348fa544b1440eda09cd6afd8a01f4111633`

```dockerfile
```

-	Layers:
	-	`sha256:665d67252df18d6a5da27a11150b2176a16e3ccfa6892683968a9bd2c30e670c`  
		Last Modified: Thu, 03 Jul 2025 20:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:421b24c664ccc9c46483294ec3299a5fad9a7f3ded990bfe0188b98a6182076d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70378329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e44ee7b4f850245305887902a5b250f4ae7947b9ac82d2fd0d5fd628c6d8713`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 11:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 08 Jul 2025 11:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 11:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 08 Jul 2025 11:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Tue, 08 Jul 2025 11:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 08 Jul 2025 11:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Tue, 08 Jul 2025 11:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 08 Jul 2025 11:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Tue, 08 Jul 2025 11:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 08 Jul 2025 11:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 08 Jul 2025 11:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 11:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 08 Jul 2025 11:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 08 Jul 2025 11:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 11:04:15 GMT
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
	-	`sha256:b45e9c4687f4eb78899e7672cc62ee2f8eaa63968fbfe447a1091cd17cb92822`  
		Last Modified: Thu, 03 Jul 2025 17:29:09 GMT  
		Size: 18.5 MB (18450895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3da38cd300c2b3d25ee4c4938add161be30b3de0abee333693a65c160180e`  
		Last Modified: Thu, 03 Jul 2025 17:29:10 GMT  
		Size: 20.3 MB (20295391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650bb4a064e2c3d22ea4894a295bacf750836a3ef836da21703497e9af4d3e4c`  
		Last Modified: Tue, 08 Jul 2025 17:08:01 GMT  
		Size: 20.0 MB (20014278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e471b6b955d8e0a284c9d381bc75b8d2046f28c457ea05c09139e884d0887019`  
		Last Modified: Tue, 08 Jul 2025 17:07:59 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9de1a1ebb1e54bb853281cde4f730618161c9da19df13bd46f80ec60c7f2ca`  
		Last Modified: Tue, 08 Jul 2025 17:07:59 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030dd11ff5a262be29ec501f1f1a21c6cc06018b0a67fd4761d257a92dcb5fdd`  
		Last Modified: Tue, 08 Jul 2025 17:08:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4e710e291602b3ec6ef4817cd58a2b05e2a01f541b03878623df6ac027c28db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b312c2543647677d9533f8d9c072eb268e13c41a5f4eeedf19b142e31e078255`

```dockerfile
```

-	Layers:
	-	`sha256:0114924814640bb18482ba9e070e52b07831b310e8dcfe3cde165abb988fc78f`  
		Last Modified: Tue, 08 Jul 2025 17:07:43 GMT  
		Size: 38.3 KB (38276 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c6088237d22ce9f1c74b09f299ffc9f660ae3d9b0b05cf68e70974559ef0b72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69376189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10eeb922114f57e5118d438eef0c96af65407b628eafbe137c8fdb51fcad1d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
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
	-	`sha256:578d791b7466926edf1238dd99429c213ec1bc4dcee36747439294e42932731d`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 18.4 MB (18435301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b8306d49bf56c0996011a7dbf14a35d285e478f4759c1daf58d9519ece2ff`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.3 MB (20282785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6addef9f87ba5b01ac2e58c96320abc7a1bcd3ff669d3c9c0b93395622b2e9c5`  
		Last Modified: Thu, 03 Jul 2025 17:22:39 GMT  
		Size: 20.0 MB (19996149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a00c2ad465791389c845386cc36b1aba8e0ab1364976a7917d07ccc7e5cc9f`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b39761abe87c4aa32d3b855e397e05f3de49cf9f3309059d1e50bcae1beced`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e18e98353951397b33bf6cc1c3e7177799e6c6a29829dfbc5a1e3c18dbe67`  
		Last Modified: Thu, 03 Jul 2025 17:22:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4620cfbab6b718b6d7608e646d78fee8bd24e4a9e3998c00d2cdb9fc500a4d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0119c9efe61eb4c2a2315fc24b97f0186bdecc9db92ff39c084e27c154054af`

```dockerfile
```

-	Layers:
	-	`sha256:5ab8fb7ac3eb539be8a1207dcaf14c686d92029c58cf5144592f402daaafb75b`  
		Last Modified: Thu, 03 Jul 2025 20:07:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:345329b66e3b117cfabf618ee56c67a4ce9ee4226ed3bf4b2b62d98e8d15e90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7302f18f8f6a2df7421bf64634eb1a82bab0d8397a5cfeed34f49ad79288594d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6972a69e584db7ee5fb8279874ef80ea710672907c48d4e75432ecec12a692bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36eae856160dae536d39b9a3894bcdd53e6a8515faedf00b3ed1d0b03dff1a6`

```dockerfile
```

-	Layers:
	-	`sha256:1202a1d5f73476f0c58ffdbc17ef1175dc800026e4e305fffb0e8a8f847c4234`  
		Last Modified: Thu, 03 Jul 2025 20:07:57 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

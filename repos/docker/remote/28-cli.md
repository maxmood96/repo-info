## `docker:28-cli`

```console
$ docker pull docker@sha256:9346c5506bb395e8d543072b8a42e55b6ac4c1ee2bb49ea1e6dbcdae058d6413
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
$ docker pull docker@sha256:d5eea7f642a97e37c6cfb144bbf1c621a921d6bd6770925ca46083b6022e72ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76252652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5318c07034b1070773327332274ae100cfd2b187005a9b16f0560bcaf24f6374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.5.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-amd64'; 			sha256='d02d47061bede1b90d34bf6562a5f39e686773e97cf9d00e7114b3c1e269e524'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v6'; 			sha256='7a90b222d33f2b70540ac9fa0d2d7feff02accb83a22c557c78f2ad924807ed5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v7'; 			sha256='4af7949022b2f5228990d7b9faab5cea8ac93edc6faf284d115fa33bbb367778'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm64'; 			sha256='14e50940aef67c4b46f6b03a5ccc3851a30f883e751a61048a4bc80b8832a840'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-ppc64le'; 			sha256='eaaa77de28c79306be25ad992a1fbd537113bc3543ccac2a3e2e1855a752a665'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-riscv64'; 			sha256='16fcd25ec8ca6f15d6264133c3dc93cdce211fb2028b8cb529c0ea7b880c3818'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-s390x'; 			sha256='dec5db787903debb0f83012a416421e4119d7f28837ae7aa6ae5b689750285fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f4121261305cd808f866e5cc468c62c7b691048458ce84c73cebc8744a0f5c`  
		Last Modified: Fri, 03 Oct 2025 15:42:57 GMT  
		Size: 8.2 MB (8206013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacb763c34fa98faf157ad30ac845055c7e17d6bc356a735dd34979b2ca3dcd`  
		Last Modified: Fri, 03 Oct 2025 15:42:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82baaa61b0bd5e833b9bf0dce2a5ba042e651d1dae98dcecd76a54d85245f705`  
		Last Modified: Fri, 03 Oct 2025 15:43:00 GMT  
		Size: 20.4 MB (20429721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c233148e55acfe21ab7559acf33645c62cab15c2786fb755b117d0f761692214`  
		Last Modified: Fri, 03 Oct 2025 15:43:04 GMT  
		Size: 22.2 MB (22158310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a01365128829f855670516e240e079aaa07cca78da2106a03fe8cc88723c3c6`  
		Last Modified: Fri, 03 Oct 2025 15:43:10 GMT  
		Size: 21.7 MB (21656766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d97b7b769f0ef0ffff5fb8721b8852aab640d625cccad858457c7ccdc01909`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c252ca38c80c99c59f88eb9177337a5d1e1be51a71bca74077ce10d0e2db2ff6`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f710bb1cc914e30eac705c8d79e2b6fac559197d538c0a843bfdd992a69bfe1`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b0a855e3980a26a067b2d2a0781a2320c0ebb0b95cdd8969e3d1e63c41977d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9a5a518442282d243de3bf9659aab9d1324488d38cf20df6f68901e7a70638`

```dockerfile
```

-	Layers:
	-	`sha256:b23b75fb095cd2bcd99a74b495c36431098c714483d3aee226f206d2f69e78d9`  
		Last Modified: Fri, 03 Oct 2025 17:07:47 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d7381fa06c8275c17d5e128e8ffe09b5da39eb3e8af48dd9b249316673239c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71190674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f458ec5b7496b07e3c6124e1edb26f921eb5e0291749ec9f7fb91d2be49adcf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.5.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-amd64'; 			sha256='d02d47061bede1b90d34bf6562a5f39e686773e97cf9d00e7114b3c1e269e524'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v6'; 			sha256='7a90b222d33f2b70540ac9fa0d2d7feff02accb83a22c557c78f2ad924807ed5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v7'; 			sha256='4af7949022b2f5228990d7b9faab5cea8ac93edc6faf284d115fa33bbb367778'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm64'; 			sha256='14e50940aef67c4b46f6b03a5ccc3851a30f883e751a61048a4bc80b8832a840'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-ppc64le'; 			sha256='eaaa77de28c79306be25ad992a1fbd537113bc3543ccac2a3e2e1855a752a665'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-riscv64'; 			sha256='16fcd25ec8ca6f15d6264133c3dc93cdce211fb2028b8cb529c0ea7b880c3818'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-s390x'; 			sha256='dec5db787903debb0f83012a416421e4119d7f28837ae7aa6ae5b689750285fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e741fecb89d2db47b037f78cdb8490877b12c4d1e828f80f3b1293a401b20878`  
		Last Modified: Fri, 03 Oct 2025 15:43:07 GMT  
		Size: 8.1 MB (8113304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346499d5a12a0d1eeb76f29fdae7d39b3ed1691d2970b7b4241a85a0e2e3bef8`  
		Last Modified: Fri, 03 Oct 2025 15:43:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afe8024aad7ad6596057655d9b78201ae0e584574468ac179036133c2567840`  
		Last Modified: Fri, 03 Oct 2025 15:43:09 GMT  
		Size: 18.4 MB (18419890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4bb5235a7e0f14da9eb4e2ea6fb77c0065d5f84a49d54b08906ec0ecdd9f2f`  
		Last Modified: Fri, 03 Oct 2025 15:43:09 GMT  
		Size: 20.8 MB (20759307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef894bb2a7c2d67015665f6d2215a2827e7e83b54c9faacc27a95226e77785e`  
		Last Modified: Fri, 03 Oct 2025 15:43:09 GMT  
		Size: 20.4 MB (20395111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e560df71363b222435e64e5d5cb6b7c662012dcaf8e3aa6e0e6d48b51e402be`  
		Last Modified: Fri, 03 Oct 2025 15:43:07 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f6e2a7bf9e1086d0da4efd3d4ef8b63976d2d5b8b312ff28faedbc78a2326c`  
		Last Modified: Fri, 03 Oct 2025 15:43:07 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7f4fcb9ac33ee3406f8a2e0a0a7f9e8d49f7d284d569d0fd29dd6869ba6800`  
		Last Modified: Fri, 03 Oct 2025 15:43:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:288801d6b3cdcdd95811bed6b33669ba7e4a9291f0803185af8cba15f3a43326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c159a7f1feae003fde9b008e8ea0a16bb293f6dc4a2131b493431ba075f28d4`

```dockerfile
```

-	Layers:
	-	`sha256:fb2fa30f269ea814e093ddff016eaecae13a50ff05d306e058913baf73667f5c`  
		Last Modified: Fri, 03 Oct 2025 17:07:50 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:bb7ef8a43ddb42bea13ec4c076ada0fb84a1187d43d5a485d1857244574d25dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70181198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b28aaf2092e123a0a50c48ec059da72a6b792fc5ad10d81c3c61e0f4f57e412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.5.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-amd64'; 			sha256='d02d47061bede1b90d34bf6562a5f39e686773e97cf9d00e7114b3c1e269e524'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v6'; 			sha256='7a90b222d33f2b70540ac9fa0d2d7feff02accb83a22c557c78f2ad924807ed5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v7'; 			sha256='4af7949022b2f5228990d7b9faab5cea8ac93edc6faf284d115fa33bbb367778'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm64'; 			sha256='14e50940aef67c4b46f6b03a5ccc3851a30f883e751a61048a4bc80b8832a840'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-ppc64le'; 			sha256='eaaa77de28c79306be25ad992a1fbd537113bc3543ccac2a3e2e1855a752a665'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-riscv64'; 			sha256='16fcd25ec8ca6f15d6264133c3dc93cdce211fb2028b8cb529c0ea7b880c3818'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-s390x'; 			sha256='dec5db787903debb0f83012a416421e4119d7f28837ae7aa6ae5b689750285fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d657a1bd6673b13a869dd3aef9cb3bf6e77a13d7fbd88af33a7bd58887072018`  
		Last Modified: Fri, 03 Oct 2025 15:42:27 GMT  
		Size: 7.4 MB (7437667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfff8f3e04fb650d0573a6e389dd188a26cba26951c74c1394ec977fe1ef58bf`  
		Last Modified: Fri, 03 Oct 2025 15:42:27 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f2efb09e78c3d501b901d46bd087f1a612e3e10f89869cff4521a5c9c2b6ae`  
		Last Modified: Fri, 03 Oct 2025 15:42:28 GMT  
		Size: 18.4 MB (18402988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48db8f4416a857355de94fb9f102ee288bc32a5b53c5ab11905115a9a5994bea`  
		Last Modified: Fri, 03 Oct 2025 15:42:31 GMT  
		Size: 20.7 MB (20743372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92347015b38c861670eb924808eab074eea9dcf1673973127cca5beb673dfdf`  
		Last Modified: Fri, 03 Oct 2025 15:42:28 GMT  
		Size: 20.4 MB (20375979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ad4c72b2e8eebe227682353ea38c6836bee64dfe34120bb0978a6a1b2c877e`  
		Last Modified: Fri, 03 Oct 2025 15:42:27 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4668ed29abe41847a4deb43b28b6a5ed5e091640d9ec945da223020b6f00ea7`  
		Last Modified: Fri, 03 Oct 2025 15:42:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1598b4284b6ec18f8af59189933ad4ee519d64618bd695ca79acc5d939da33`  
		Last Modified: Fri, 03 Oct 2025 15:42:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b53b2a0dfffaf54e3c1624ca1acfe05f386da5c9a30462d4f81b2ac6efbad288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e3716ca95c952691eb8a96e068b1721637e70962ee86e71f5249766dc0ce19`

```dockerfile
```

-	Layers:
	-	`sha256:fda163a204484dc73af895db49f72864ac1701fb57029233d7ddc220474c8610`  
		Last Modified: Fri, 03 Oct 2025 17:07:53 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c0724b17cc1213826a3286add14ace28d271de874fa36db2ee89bd4dace4f3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71652939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dffc628b273a3882ea3e3ba84bb32e497b0a22f0c102b4d59362d4fe31fcac6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.5.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-amd64'; 			sha256='d02d47061bede1b90d34bf6562a5f39e686773e97cf9d00e7114b3c1e269e524'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v6'; 			sha256='7a90b222d33f2b70540ac9fa0d2d7feff02accb83a22c557c78f2ad924807ed5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v7'; 			sha256='4af7949022b2f5228990d7b9faab5cea8ac93edc6faf284d115fa33bbb367778'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm64'; 			sha256='14e50940aef67c4b46f6b03a5ccc3851a30f883e751a61048a4bc80b8832a840'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-ppc64le'; 			sha256='eaaa77de28c79306be25ad992a1fbd537113bc3543ccac2a3e2e1855a752a665'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-riscv64'; 			sha256='16fcd25ec8ca6f15d6264133c3dc93cdce211fb2028b8cb529c0ea7b880c3818'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-s390x'; 			sha256='dec5db787903debb0f83012a416421e4119d7f28837ae7aa6ae5b689750285fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befee8c2b0ad40f8afec285692dd9de306244ab77849362b32f364598f4dd856`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 8.2 MB (8227655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81db965703fb492a9487f0707728f846ca5016cffbe4cca14a9aaedf3fe47be`  
		Last Modified: Fri, 03 Oct 2025 16:10:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae023da43925318e9d906c7752c90968e4e76401eff1a13c13a02dfad260775`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 19.2 MB (19238158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d084ed095dcaaa56e75d1464d58172ca160961091fd6c2110b81301c1c8d144a`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 20.3 MB (20274240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5cbf3334db63fb72ebb37340a3158221d6151607e4b01c5be6b44f4c2a1f35`  
		Last Modified: Fri, 03 Oct 2025 16:10:10 GMT  
		Size: 19.8 MB (19779981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a37c322750556c7e8922a42c05e513ce640dbe5059b406843b4285c15f28be`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ee98d68b79d3a825b7c3d7d4492c505cae7e7ee829b8da41259b5372f704be`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06880fc24b1d74868cf537077a0bd0cc09b9cb315d6f2e5ba9ae3fe57405085f`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:522c2cc4ffb9267687aef6f8d72730ea70ceca998330ee32f74c9816c9a1acbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b98ac9778851ce1834f2ea2b1f14805861737c19429ba5d5ad7902bd7ded272`

```dockerfile
```

-	Layers:
	-	`sha256:bb5f4b80b573216b93fcd1b186a648d54c90b671162a8e1cf7cac20bc8679899`  
		Last Modified: Fri, 03 Oct 2025 17:07:56 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

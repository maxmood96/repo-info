## `docker:27-cli`

```console
$ docker pull docker@sha256:d08bc41323f2f8fb380b9f7fc61b3e7f7ec20e7f72f3fb563d812b86e579f4a6
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
$ docker pull docker@sha256:fa603bf43501a560d67718e728b2526168606de711a4bf12ab15fd1ff86bffa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70090991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88aa18bc6d8b37961633d4caa5a84d75aebb18df78cbb784ce0a967f06b2dd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801c156d65c0aeafe6b1a50d17dce7947e296b8fa44a6f61b29fd90340de2a8b`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 8.1 MB (8060157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee732ce35dd1e51492f282a0c7ef7e73647fb49a9ff7b4a73ea0dce9eecbcf8`  
		Last Modified: Wed, 22 Jan 2025 19:30:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c08ea579adb388e937739d6ac2bce4549fd6d1d9d4f160b022f0d83b6db49`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 18.8 MB (18848908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e4ccbb97d35015ae98ca78294633e09f357302575730f38bb64bc8b9cd6c`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 20.2 MB (20234415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a5106f63a86a14bc85c80b165dc2ad58a39eae39e157778184efc9d7ecc0a`  
		Last Modified: Wed, 22 Jan 2025 19:30:17 GMT  
		Size: 19.3 MB (19303649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41638cca9601ce7fa95715d48ec743b166ea78faaa7df26ce82c2f900e297e`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c950bcb24715f9ce44b4706a422d4d45494bcc016eccf92f00205351de438`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2418f03f869a76a445737be06791ef57eb536fe39cafcfbf9358c6eda1a8db30`  
		Last Modified: Wed, 22 Jan 2025 19:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c2fd3985e093f76357db4eb0edb7366da63abcd4d886d4ce468a57f2a9d61cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f63757cf097dd6a2cd103777f6e5a9c61b6835fda4758002fd4d7715ca5a9`

```dockerfile
```

-	Layers:
	-	`sha256:01f24a240eee3855c43902daac2c5a81598710850b9ac3b0e2785ff83bc7f81b`  
		Last Modified: Wed, 22 Jan 2025 19:30:18 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:9058c2456bc7e9e57b56ef987e17032a60ebb9b0ed3f5397fcf2a49a2489c36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65161011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb8e3e5dc76ab096d8bfe47b7c4fc2dfbec6653cbf715a6e77e2410cb4b224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 00:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 21 Jan 2025 00:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 00:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 08 Jan 2025 18:20:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c3b358e07f1cde10fdeeae613643ac5681ba773983f9f8026030b046726785`  
		Last Modified: Tue, 14 Jan 2025 01:36:25 GMT  
		Size: 16.9 MB (16866213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06b3967b4e642b2d6cb98ddda55dabc4993a3899194dfb50645801f28a2de4d`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.8 MB (18843467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e167d9a57b137b11ef1469f2536ba9c09315dd6e1858686fed99b317c474b`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 18.1 MB (18112380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746625955b5ebca8aee1d3e40c90c535484d1d6e5dcb2f3af36d50293db19d9b`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778bb8e57da23192256e4be8f68202f6916ae3d97cd410afd26a12c5157d2351`  
		Last Modified: Tue, 21 Jan 2025 20:25:55 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f6729763aa7494d8f2673d92eaee47a0d1ff164b4022dad21403edbb87ac5`  
		Last Modified: Tue, 21 Jan 2025 20:25:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:cef2c039f429175c5704e4c107c36f2bd6441432c5799d6c14d91b7a04a014b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be43822735795833e6a7cb91e6725da48bbf41d5813bbb8a8db9f8dd1276152`

```dockerfile
```

-	Layers:
	-	`sha256:1139d69aac6bfa1ae449cb3a916c864f21e25df7351ad2134f9dfbfb194ac645`  
		Last Modified: Tue, 21 Jan 2025 20:25:54 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:0091be5184eae4250fc1cb11a01fe5ea066d1b7a846c67a6d23e817d010260a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64176388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7773e8edbbc039cd622aa68e12968928793e28dc0fd375c732981a7e42162a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 00:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Tue, 21 Jan 2025 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 21 Jan 2025 00:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 21 Jan 2025 00:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 00:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d04febd7f7d8a507ee9f0b3e686f63959da9eba7f9c44aacc0c4760e6b8eb`  
		Last Modified: Wed, 08 Jan 2025 18:35:55 GMT  
		Size: 7.3 MB (7293917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da18b0856209e09ddb1746d60b57bafc68fcbeaa264f0dfab0a99340b19e366`  
		Last Modified: Wed, 08 Jan 2025 18:35:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5996ab38076f0774003f44724032451fe6ca5dabac501d8d7c3c5fa97e0af314`  
		Last Modified: Fri, 17 Jan 2025 01:28:03 GMT  
		Size: 16.9 MB (16855885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33248751ec9a79f58a4b5b036cbf06d54ce37e0337b057fe5feb29d5576c54`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.8 MB (18827879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe30b6cc54a36bcb0b47969de63a47bee866698b3335e056bea81d1f547300f`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 18.1 MB (18099434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb99b6ce2a5d6c24986aa65b46e2672a77c8786cd542e0f1cc0967e176b9730`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470915df3823069dd34a72bb0ab32165b071326af067df85e9a6e1e4f27915e5`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fee2110e481e5f9251d6258c88fe9cfe286d091a0bcfe656ffabe01cc0920`  
		Last Modified: Tue, 21 Jan 2025 20:25:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d503a1f6ea902951cfe37f5418137ffcd9c643beb7df1964bd2e45c83ef6f07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d161766fb8c4a9cb705ff2b79fe8c2fc98c84779426e81316089633605422d`

```dockerfile
```

-	Layers:
	-	`sha256:79bd3d5210a7b1bf892a818f3142ff8a95fb47d2845f0667fb2b28d4ed3d1b6b`  
		Last Modified: Tue, 21 Jan 2025 20:25:58 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a6f1a1a24027716e44d9b7a08b7252bf33c60403dd92c77bf863d625a15bf302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65972403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581c2c02c852d766afb66b604dbd45f44c1bdd42eb5cb2c127663c9e3954b41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_VERSION=27.5.1
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-amd64'; 			sha256='8b21d3ce1011c4c072d64d4a7311c591cf1c2eb6b35bfdfe28f8e0b76e51621b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v6'; 			sha256='94aeb8e6d6f56a162dee85f9f88af33e93cd0c39cc60d4453998e876a4652381'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm-v7'; 			sha256='eab0a7d7a2ae87593827a6267f02c9144e2e12dad1a62fc7d53b12e3f931e331'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-arm64'; 			sha256='838f009f34da70a74cf3c835178b8686bc1e5f47509add274a6ee22f70620521'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-ppc64le'; 			sha256='eb0a33ebb7f1353524eecc962b896307f718cf7b753b490918e0f22c087e0636'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-riscv64'; 			sha256='ce65046624f3da234030f7f4d83f345e0879403c7980cfe6937b88ad6ecd1f36'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.linux-s390x'; 			sha256='01f1ab8d3c1ffaf8b84422a820a54a296c41f6af9753a975a29f5d8918169a1a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Wed, 22 Jan 2025 18:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-x86_64'; 			sha256='ed1917fb54db184192ea9d0717bcd59e3662ea79db48bff36d3475516c480a6b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv6'; 			sha256='1e9c5c4cbdda569164a067ce9246c3a969bac253192526ffe0d0e3a99a4cbd0a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-armv7'; 			sha256='c12bb3c23db5c409a15dbb13be4b61faa74c881d5db5f8a2816f60c19c35251a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-aarch64'; 			sha256='0c4591cf3b1ed039adcd803dbbeddf757375fc08c11245b0154135f838495a2f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-ppc64le'; 			sha256='23adf27e7637fcb65b37d8a214712c4a83d1a3cbc6be0fefd7b6e5cdfd89cb79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-riscv64'; 			sha256='392f705e6b1ad99b8bf761f4be8211d531fbacbcad1326f14f1cdcfc68c25a6b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-linux-s390x'; 			sha256='fe2d32c99c34c39a5156fb3bfb73949be746644a3f887b628bfc971c37fa1b90'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 Jan 2025 18:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 Jan 2025 18:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 18:04:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20a21d400e81f258665c9fa5849d2c7ba24b4de03a742e8538c1bef7e27a91`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 8.1 MB (8074433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096e83f3bf8d9c9663050fffbf6001a4b4c64063767caf6034435482946e868`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81d88fa93e9698f02174fedda46b7e4d4a7848fb4becc244b4d1a555dd8310`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.8 MB (17794934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb6a03fdaacc664f430ce86287a4271bee03d19bb128b8a7213b99a6f96f481`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 18.5 MB (18458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7858947f86175049e46b646baae6b31030133aab3b8edff362fb088fc4f8e`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 17.6 MB (17649724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d26eff37b83930827b77743baadb558085a649ead199f07714b954eb0dd51`  
		Last Modified: Wed, 22 Jan 2025 21:05:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1de09753b3d0b8f79e3432cdce068dffbda225f2e81c2957533f3327035213`  
		Last Modified: Wed, 22 Jan 2025 21:05:23 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73304a9727a8fc131f990495c4cab698bb7ec30ea44994cde426b7ae97f6e36d`  
		Last Modified: Wed, 22 Jan 2025 21:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d47d71a04452163577e439ccf4d91457ac4ab2f7fa68cc32517b973eae562185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bbc8c969ef865647e5cf02166f155e554bf917314e431725c57c35399e34f1`

```dockerfile
```

-	Layers:
	-	`sha256:15793555fc85eacaeec2b45b37d648b58e45b2ba5fcb0e42884c619c7eb12885`  
		Last Modified: Wed, 22 Jan 2025 21:05:21 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

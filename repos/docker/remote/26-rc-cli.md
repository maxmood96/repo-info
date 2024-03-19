## `docker:26-rc-cli`

```console
$ docker pull docker@sha256:934764863124251d2ee48a3e421a9f225a65a1436aea86afa407cb50282418f7
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

### `docker:26-rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:ce4b82d46cb82c2c560402330d41498797d5b8314dd6ceaeb0fe9b07d278dbbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58562875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a630d0a3a656699032ed83df59b0c4b728b1172c0b9b4a9cc490edace057e83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 17:08:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Fri, 15 Mar 2024 17:08:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 15 Mar 2024 17:08:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Fri, 15 Mar 2024 17:08:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 Mar 2024 17:08:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Mar 2024 17:08:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc1ada2515f4bd254c5d0a05da6e49153cfab57c096440e5c4990c6cdb8ae48`  
		Last Modified: Mon, 18 Mar 2024 22:49:05 GMT  
		Size: 2.0 MB (2026139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb700276c1d7fd5fb6d780a6f52f8ceba8a39f889780b9880bf246044a6e697`  
		Last Modified: Mon, 18 Mar 2024 22:49:06 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c507df818463d4a9cec85f1e77b37ee9ee800092eed22d8cbb5f4ad7507be818`  
		Last Modified: Mon, 18 Mar 2024 22:49:07 GMT  
		Size: 16.9 MB (16921404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5254e960e2a1218272cddffbacc1e498e8f907f858787d8267df379890c427`  
		Last Modified: Mon, 18 Mar 2024 22:49:07 GMT  
		Size: 18.0 MB (17982283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9f7d62e8d6369630b1d6b7880c29b169cfd160138bca93f3800719e03fbbb2`  
		Last Modified: Mon, 18 Mar 2024 22:49:07 GMT  
		Size: 18.2 MB (18222064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08650e921823712bd26d7713a76369f2f2b7d78639e0154dabcc48dcea51c382`  
		Last Modified: Mon, 18 Mar 2024 22:49:07 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d573214ea5f88f71efc093b4505d1bc4c2cd661a052e46d899d83ebb998c7e1`  
		Last Modified: Mon, 18 Mar 2024 22:49:08 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e7cb23ff52006ff570b109f55d40fa8c47407f7c69fbe61809ed4769c8e9a2`  
		Last Modified: Mon, 18 Mar 2024 22:49:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ea2a84a58e6315daa92fb57c16121ebba1044999778588490f2c4e6b0447dead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.6 KB (443595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa41810305550e8f1ef283864893be623a5266ae500ade8560d6dc2dec91161a`

```dockerfile
```

-	Layers:
	-	`sha256:29ad24c6bf47226719d4f7a2db5be53365f0a522b3186688548ace91c58428f0`  
		Last Modified: Mon, 18 Mar 2024 22:49:06 GMT  
		Size: 405.8 KB (405777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd6c5b70912c095df7ccd6db42f8cdf6868f471f38c2b4e90884955c44566b9`  
		Last Modified: Mon, 18 Mar 2024 22:49:06 GMT  
		Size: 37.8 KB (37818 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ca7e195c974c771258e32a1b97dd6fd571772c249518f72f83932f2bd542e836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54612816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c18f8144931729693fac2bd4d8706a76d3cddb5126328758d909410c211ca1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 12 Mar 2024 23:18:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 12 Mar 2024 23:18:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 12 Mar 2024 23:18:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 12 Mar 2024 23:18:59 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Tue, 12 Mar 2024 23:18:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 12 Mar 2024 23:18:59 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Tue, 12 Mar 2024 23:18:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 12 Mar 2024 23:18:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Tue, 12 Mar 2024 23:18:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 12 Mar 2024 23:18:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 12 Mar 2024 23:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Mar 2024 23:18:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 12 Mar 2024 23:18:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 12 Mar 2024 23:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 23:18:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e27822c73b25aa0e0a23a1efeeeedcdffbe4c10fe4a3692b84b94ae5c25191`  
		Last Modified: Sun, 17 Mar 2024 19:10:36 GMT  
		Size: 2.1 MB (2108651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f6950c460cb7c97ee78b38ea4b89fcd66c428e66e30f39f449726dc412bd43`  
		Last Modified: Sun, 17 Mar 2024 19:10:35 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d53597d22ee5b3fe3e99f4da528f1062547f291a8ad32f5ac5e7a11eab671e`  
		Last Modified: Sun, 17 Mar 2024 19:10:36 GMT  
		Size: 15.3 MB (15304765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d1fc5f71b4aaf93b1c1b0cf0d5c024564bfc23dfb3a3a1689f250067b35deb`  
		Last Modified: Sun, 17 Mar 2024 19:10:37 GMT  
		Size: 16.8 MB (16818350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9055f8a83d1673012d6ef795747d02c04208338287428b2be4a37803eff40a`  
		Last Modified: Sun, 17 Mar 2024 19:10:38 GMT  
		Size: 17.2 MB (17213397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df44dcde98090350062a6ea148b5b599e4e76befc424b0d90d7869c143031bae`  
		Last Modified: Sun, 17 Mar 2024 19:10:37 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f036467c02ef7029ebbcfc52afc450d5122d7bde328fb65bbd197f3e267f86`  
		Last Modified: Sun, 17 Mar 2024 19:10:38 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6710e5d16dbdc8c30855483c95725a52ad867688f4aedf56297722a5f0e5c657`  
		Last Modified: Sun, 17 Mar 2024 19:10:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f2f83285c63269748b7bbf88937f7526defc36a0a6ecaedbe574e65d4c24eb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac8dff054b75112ef4ef550c8f2ee2b36a5d52ffbc3acee2835377703ab7e7b`

```dockerfile
```

-	Layers:
	-	`sha256:f65a384e5b11940659667b409ba2fdeeac8941887db04d987b921d123c8b4430`  
		Last Modified: Sun, 17 Mar 2024 19:10:35 GMT  
		Size: 37.6 KB (37585 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:272602d1d74e302308c344fb5d45a8b91c20a3a2450c8e3a5260b1958dd7f091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54125604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0046c2ac87acdcc99520467dd2b6cf8f7856964b570223833e76bdf1fe96de8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 17:08:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Fri, 15 Mar 2024 17:08:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 15 Mar 2024 17:08:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Fri, 15 Mar 2024 17:08:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 Mar 2024 17:08:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Mar 2024 17:08:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62203ebc003cf77a4ff92a3c67a89cd14dcf1adf84fb125d2f3329ad08ad9a61`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 1.9 MB (1896160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8418dd6a88f431ade9efd4277500a4c6483d9ac98459ff95a86dbfde7d02e2a`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fba55846ac9a8fbb3783b4a07e9bedc5bb0cfc0993947a5a752d36c3a67a91`  
		Last Modified: Mon, 18 Mar 2024 22:49:24 GMT  
		Size: 15.3 MB (15295882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aad74d43374b5b4f102cc0673478ccb73bfb77098f5b6576c837a219f19ee83`  
		Last Modified: Mon, 18 Mar 2024 22:49:24 GMT  
		Size: 16.8 MB (16804615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b30daf0e3e93300adc0bef611e08d508b1ac830b432f13616160a5db268b2e`  
		Last Modified: Mon, 18 Mar 2024 22:49:24 GMT  
		Size: 17.2 MB (17207788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee1f56212fdf356dd543ca38ebcee40d2335bc9c40f9d9bb204fd2fdc4cba72`  
		Last Modified: Mon, 18 Mar 2024 22:49:23 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acdc26ad25fe00035a1856662688b03ee133bc690aa9f09e6b2e99d50479e6d`  
		Last Modified: Mon, 18 Mar 2024 22:49:24 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79de40673b087d1978d39b0a957a945ad73c4a8c34b48d021b7649aae36182b3`  
		Last Modified: Mon, 18 Mar 2024 22:49:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3c60ab4ea5a8f89abfc6f2447628ced299d9b4f052db2531f3bab9f5acc2e797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.5 KB (438536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5830e750d268fabbee38daf593fbeb39c36859cb2a377d7540c26700710d805f`

```dockerfile
```

-	Layers:
	-	`sha256:c4cfb87cb4d138df89765174fc8b72da87f8c1e4aeb7942e089a8ea4db7cccd2`  
		Last Modified: Mon, 18 Mar 2024 22:49:23 GMT  
		Size: 400.7 KB (400736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82c6c0a1151dad7f29cca3024a4b66e1909ce944ff1532dd7e9a7198e98d5095`  
		Last Modified: Mon, 18 Mar 2024 22:49:23 GMT  
		Size: 37.8 KB (37800 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5666d35ab78c6bddf665e56eeb058ac7338d03c41afb72a9af2bf2c3b0319d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54302162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361b345158a2e779ec275d600f8879a2bb63b356865bdcaed57c3136d2c9ca4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 17:08:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Fri, 15 Mar 2024 17:08:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 15 Mar 2024 17:08:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Fri, 15 Mar 2024 17:08:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 Mar 2024 17:08:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 Mar 2024 17:08:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Mar 2024 17:08:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b275a3377f65492f727dc46aa2b70be6ec8ff96583fcd9a7b699692b5170bc`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 2.0 MB (2019704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c53acdebd8fb391eae546ed72149f049f8ab4d594f12c74c49be04cc3b9708`  
		Last Modified: Sat, 16 Mar 2024 04:06:08 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1fd8107a0166ec2911f8f43a2a5e067961d5963e722b47e61856820dd946c8`  
		Last Modified: Mon, 18 Mar 2024 22:51:05 GMT  
		Size: 15.9 MB (15936587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f3e440238097c0c767248819bba9d596e55a79b8eb3e25da8bd16e03ea05e5`  
		Last Modified: Mon, 18 Mar 2024 22:51:06 GMT  
		Size: 16.3 MB (16349514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f677fe87a3f5798ccdc2e06a7e8db90c3afbe88459e3dfd23707f0cc9e47ebb`  
		Last Modified: Mon, 18 Mar 2024 22:51:06 GMT  
		Size: 16.6 MB (16646385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540ce7efad7a51b0915b014a5e04762666981161df191f26548e78f51be5a318`  
		Last Modified: Mon, 18 Mar 2024 22:51:05 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ad2a99d95baf2767c815ab3a5a825daf12e9d9308d31461a91d1282c5d2375`  
		Last Modified: Mon, 18 Mar 2024 22:51:06 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dc950dc93070da3a2b5d02565dae19fe24e817c4dd9ea11a52dc68fb132adb`  
		Last Modified: Mon, 18 Mar 2024 22:51:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c899f0afb94def0a5cb5ee4d977de2c3077ff1775554c91cdfbc14c268e40f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.5 KB (438480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303da2b5d427045c3eb5ae7868fec04809696f96d3cf48f9d5e2139e3f941e70`

```dockerfile
```

-	Layers:
	-	`sha256:076757ef5b1afb21efe05b55fd10ad0101eb5a57c75fa53bbdf9d7b8adfbbab2`  
		Last Modified: Mon, 18 Mar 2024 22:51:05 GMT  
		Size: 400.8 KB (400819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f39f3c987e0d8521637a9c5b7432a4a34d79c6f580093ef32ef8d309256aa63`  
		Last Modified: Mon, 18 Mar 2024 22:51:04 GMT  
		Size: 37.7 KB (37661 bytes)  
		MIME: application/vnd.in-toto+json

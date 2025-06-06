## `docker:28-cli`

```console
$ docker pull docker@sha256:c2e49a065e45c462dda70b65b1a50a74c75804091fae15b7e4fbec6b114996d1
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
$ docker pull docker@sha256:29ac2aff504532e72efca1a58f229c0e05f928828e62156fb304d391e82f7f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74471875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd02548899f2c001be05193b91d116511f57fb7e8f5cec5f7b58cce36fed0303`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e3c92c354188244e1e651ab7c9384326a36594dbf3e27427328aa209be1c1e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de64116684520fb5473d5fee53d9f710a283fa5926d23334bbeb9a13ece30127`

```dockerfile
```

-	Layers:
	-	`sha256:9f1baaf1f40a67141a0489af913841dd7e9427be207fe398702581c569cd1c20`  
		Last Modified: Thu, 05 Jun 2025 23:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6f76795bf488400672b314ad95bc4add17d3871c369454a410a6072cd1f7fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69497654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4905167d30157f311983a0f0fbb87d96647db6c5478ae0071e5e9d717c22247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
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
	-	`sha256:225abe8edcfa38ed05c3678afaa3fc7019381a300f823c874d6fdfd2a372c345`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.9 MB (19943271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18e44e663f768131c50d79640817a860ca8c20877f41bfc7e788ede7276f121`  
		Last Modified: Thu, 05 Jun 2025 22:44:12 GMT  
		Size: 19.8 MB (19834728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7cf9bb5cb3a10f219b307b2ff9f67f54ab05208492bbe13e06a74ca78e54d`  
		Last Modified: Thu, 05 Jun 2025 22:44:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7393d30c6bcbe757d4919545933b9de1b6f48c9a46a3ed4a0ae9281792fbd51`  
		Last Modified: Thu, 05 Jun 2025 22:51:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe877f07f4d94074494db81efb5c5e890ab77b7ce09fa3952f972953a436545d`  
		Last Modified: Thu, 05 Jun 2025 22:51:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9c9ad38782ad3e5c053ed8c736f10e9589825748a8c4233619fb70a2ec23af36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca6472c159b81f34510b55fdadf12635ed814ad061552012b01cc7622021dd`

```dockerfile
```

-	Layers:
	-	`sha256:c58766a24b3303a1f1acf7a634a2134383f4aa8fc7b6223cb9497695c7739a5f`  
		Last Modified: Thu, 05 Jun 2025 23:07:47 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:1e48b83f7392bb14bec910d025f2b5ba1a759fff65845d925284236bc07d4fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68494484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61de327c238ebb7ad778ea80f8124ffd3e79271ceb1c162b0fbdfb43ad4a56f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f8c32f216879f685817a9e63a48cdc0223d0bc7c7d0c751a4be6ba6c73ef5e`  
		Last Modified: Thu, 05 Jun 2025 22:43:53 GMT  
		Size: 7.4 MB (7440639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66719bdda62b905eb93e4b3587c931c7f3e7f93eb8bff6205afb0552b6f21256`  
		Last Modified: Thu, 05 Jun 2025 22:43:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c925984b3abe923d5073eae366d96685c0e5c02bf2dbe8bd39c7b5c93b19a090`  
		Last Modified: Thu, 05 Jun 2025 22:43:55 GMT  
		Size: 18.1 MB (18089380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872d44dab7a46cdfe4e81d3b251341852e01d42db0576ce272955bf05096acf9`  
		Last Modified: Thu, 05 Jun 2025 22:43:56 GMT  
		Size: 19.9 MB (19927228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97e0d61d6c40b7aeca6fd9316eb34a635930bf7207daacfcd95d282f6227147`  
		Last Modified: Thu, 05 Jun 2025 22:43:56 GMT  
		Size: 19.8 MB (19815903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67724918cd46ffc0aa34973255dea8af10db6b7323f9e59e0544286ee79cbae7`  
		Last Modified: Thu, 05 Jun 2025 22:43:55 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3051e0388231088407c785de69833b01ded126cc9d32135dd70c03c9628e2f`  
		Last Modified: Thu, 05 Jun 2025 22:50:48 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0ae88edd91c6844cf8c45543adc21d1ebfbde0cec16cf22f72c34ca47af411`  
		Last Modified: Thu, 05 Jun 2025 22:50:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c13cadb351384ad992f27483f70dba162d9c5b57e6643cec3c37598aebb9ff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef1b27ab22635d8c650664a7ff740383003126f39daab1972f0db14de9fe5af`

```dockerfile
```

-	Layers:
	-	`sha256:efca98ea4b9f81656feedd1b0eb5f97c37873667b5a92fa941594dad0570afc7`  
		Last Modified: Thu, 05 Jun 2025 23:07:51 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:050e38ffb61f1a397a300e2c027858126865eb5c53026a10a231ea8c71637cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70083597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049c11c099d31b1b16a8eec2d4744a8baa44341b7f6489e7c2a70a8c597e17d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_VERSION=28.2.2
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Thu, 05 Jun 2025 17:36:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 05 Jun 2025 17:36:11 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 05 Jun 2025 17:36:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:36:11 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3d9117cfb4076144f396a04008c8592792765eb725010db68b4fc6a3e9d07a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f618e6cdf0288b0248e4b6b48f1bd5324300dfd40ccfdcc2698737d569f539`

```dockerfile
```

-	Layers:
	-	`sha256:07a44b113f5c5d8eb65a6af4b53f0ae0869dcbfdd809ec06739500831432a0db`  
		Last Modified: Thu, 05 Jun 2025 23:07:55 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

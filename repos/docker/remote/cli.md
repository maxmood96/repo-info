## `docker:cli`

```console
$ docker pull docker@sha256:0b928cff9f8f13b3475054da4af345db6b21007865f4fa3e0602b4422fea5f99
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
$ docker pull docker@sha256:73e41535043067691a7c87773c5185aa2d2bcf70da2770f878b1e31e13054980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76019659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056e2811a4634c5a0f25fe0954b56f24c25f926aeb1223b8952570b6c8713db8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a0840f7bf2e2704309e6a8a5ca57391dd2830e8251ca58b1cf1ae87626564e`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 8.2 MB (8198103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95049519907f41ed2c17b5463d9a1e85c06d0d49a5e77591784efaceb65b8a`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2755065130b74435c967201d109bf95047368125c8bc5d45ea6d59991e6ad`  
		Last Modified: Thu, 04 Sep 2025 16:37:54 GMT  
		Size: 20.4 MB (20431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4c19ce784844b190985f48ad98be14f17f3d2238a270994fe9ac775fbbd8e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:55 GMT  
		Size: 22.1 MB (22129705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd018bd997bf5935457fa2cbd229bb26f83622c716e7f4f541331edfbcad35f`  
		Last Modified: Thu, 04 Sep 2025 16:38:35 GMT  
		Size: 21.5 MB (21458861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a03ca2766b80f7717cf00d58d9f92921ec19b62c58e89f926b94c0f42ac69`  
		Last Modified: Thu, 04 Sep 2025 16:37:52 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62947a7621bd39db0eb18266ac26296b8f066e67fbe915088cb76571481fdd9d`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135fdd68f415aec172a197f78dae4eeb43fc7a4d241fb17a50bdcf9bfb2520a`  
		Last Modified: Thu, 04 Sep 2025 16:37:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:1bc58cae8b64023ff83a66e3e6c7a010244c2d0b37b31569b7410a3d0f160572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e4aa4c316414f5fda3df8b4df63fb46aa181d21ec0e7d5d2fd69b2b2a2deb9`

```dockerfile
```

-	Layers:
	-	`sha256:9949e013047bd65e547eba6bfd2cee9632caa48928b88b2cd515523f27aeb42b`  
		Last Modified: Thu, 04 Sep 2025 17:07:51 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ad6e8b9bcb81416a9db3d34d65430e10e47acbcf37a4c9cf0db5c9a955a4e2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70947926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32618647e86987ce8f9b539cb4d3214f258794be577a61c143929f86609d52be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646b85fbc166bf78a7939801aeee66f958e48d0f698a7cdcfc85cdfaaf3a075a`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 18.4 MB (18421683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253dc75b66cad51fc942ef700ac4e9aae3f7605f85a342e8bfa4479599f02c0`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.7 MB (20735453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8d5e88ea33737d4f3fe897149d46ebaca6eca0c40373c9ee0c3715130ea222`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20184042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c76d87e304966f4e325049bd5cf00dd4b9a36ea69711dd117ad6e8d6c52566f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a533b17dfb625199aab85c633e90b69c4f52eed01827fab773f25ce19cac5b`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5708be19288e519cb9cedc3d6669bce2b05d4a2f9bfd71b60717c73ebc54f`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:2421e5297d31e7232bf7c1ef83de638ab7a70e69240db127e82a42cc6255de18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1df48c0d35c4804846bf1c564dbdf23bbb014a90287637c98881ad47ad389c`

```dockerfile
```

-	Layers:
	-	`sha256:be8f9e60ee07824b3be12bd4898912592e94f0206efe05bbd40ca108856b2fc6`  
		Last Modified: Thu, 04 Sep 2025 17:07:55 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:36a89a541df1c76536798d2c70834c2a684fc40cd367da1991b38773b6687879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69940868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a8ff797b7c1f2e5c72cd2e8eb9736e52a036027dd8d9aac4ffb3a8fb99675b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1b3a2ee728ffc8bb335e862238bf61a040a4ced0d6f6c5b71edeb56d9ec`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 18.4 MB (18405275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fc60ba38874d8166f35f0ba173677dc3d4d49dbd9651a90a41e00b236b5d1`  
		Last Modified: Thu, 04 Sep 2025 16:37:18 GMT  
		Size: 20.7 MB (20718512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70514835b2d11511c5cc2c5a706b160d6555888f1652cbc60d6f084321a24081`  
		Last Modified: Thu, 04 Sep 2025 16:37:17 GMT  
		Size: 20.2 MB (20165921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09ea7344cb9a4b872b115e187863ef36a72222904bf3f99d6a736535d8d97d`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf973c3a94e674f8da39840025a76ca515062e47fc552bcc58cd3425db2745e`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb09e4539c49caf1579d704b6df721b7b60b4dffd37f74fd77f685a2553824e5`  
		Last Modified: Thu, 04 Sep 2025 16:37:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6f52417beefc84301e134d1e6074194516b2daec77852e0c383b8c6cb8f3b6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcd14439dffea87510fd977e9a07dbfaf9bfcc03d46cb079c0459510051a3b`

```dockerfile
```

-	Layers:
	-	`sha256:442e4a644798d56efd70101e28ec5051f693ae9aa65ad0cb959bdac4c1ee77e7`  
		Last Modified: Thu, 04 Sep 2025 17:07:58 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:124a8198af1cac6c30a13ea821f254b8699238d1c4d70212f689a2925b545233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71511020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb87a098f7d537ae39f72ab097a2a832e6ac09952042f6ee35eb0f760a16cc4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_VERSION=28.4.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Thu, 04 Sep 2025 05:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-x86_64'; 			sha256='a55a8cd4ef103aac282812554e531aac8df7e914a287ee81e14d695556a22902'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv6'; 			sha256='a9fefb9f377d11416db7d653fac3c0ed8c61a0ef99c8e17369114b88ac48ab50'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-armv7'; 			sha256='9d1376146e42bf964f9efa8444935bc20accdc1d72a6ea44881b8d86c9ccfda9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-aarch64'; 			sha256='54488fffb60782f3c8787a48b95ed15f49f5a3a85f4105304bd46db5edd9db61'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-ppc64le'; 			sha256='83a02be63cb047207a6efbd39af13d05b8d38065617764dddc3f6e5d36161d03'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-riscv64'; 			sha256='911f9a00366a619e15bb56fe37f6a09eddc30dc1d9f704309185fd2eec0fb3f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-linux-s390x'; 			sha256='af607a5add4d6d0600bece0c6b50ce7fece516e449b17ded33be3445902edce9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Sep 2025 05:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Sep 2025 05:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Sep 2025 05:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008a0eec8464716732d94ec069377311c3fb7dbd02c15efb6188425fddd9999`  
		Last Modified: Thu, 04 Sep 2025 16:38:12 GMT  
		Size: 8.2 MB (8217747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a8736ade1519307f92d03c81af35fbaa17a03ec009d13af008b962f69987ab`  
		Last Modified: Thu, 04 Sep 2025 16:38:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59120ac4f3444beddef9d19d3d31cadcac14a915b90a1ea81b8a965f35b7ec0`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 19.2 MB (19234788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef484a23d4f49506de7132941f3bf9e85755af9c86315c82faf6d829eb7024c4`  
		Last Modified: Thu, 04 Sep 2025 16:38:25 GMT  
		Size: 20.2 MB (20248417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84ccf36201f57f18058f2c11620f29196f7a707dde8f42ae58da0ab92207e0d`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 19.7 MB (19677164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd3edf39aaa280bfc7f0c52ff388f3c3e84e5575063302d211ebf1da28cdcd`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f43469ae500997d74478257526750850e142dfbd9803769d1091780d39a40`  
		Last Modified: Thu, 04 Sep 2025 16:38:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecfa28f8d85c6f2cc4a53231f846bb79b8d612e955eb5040219d6697500cdf3`  
		Last Modified: Thu, 04 Sep 2025 16:38:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:90e3a9d1cb67f41875d2444f7b9cd67305425a82209e5debc8b0619d8b1c503b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7386a491cf42f7a37851ceb04365b5fffec1b7efd6a6d0a3edb63fa41b885a63`

```dockerfile
```

-	Layers:
	-	`sha256:8ce75e56843ed96155ce89b112cae5e76e26f78cac99fea643694ce2aedc3459`  
		Last Modified: Thu, 04 Sep 2025 17:08:03 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

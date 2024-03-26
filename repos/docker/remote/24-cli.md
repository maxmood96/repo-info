## `docker:24-cli`

```console
$ docker pull docker@sha256:dedf65febcc1b68b53343210061b87b29c88f60d1dfc21ea60b69378e8a3f34a
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

### `docker:24-cli` - linux; amd64

```console
$ docker pull docker@sha256:89ab624fbd17810cc639900622a8a3ca1b4b640a3acf87477dd1b4cfb973f5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58499792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab56abaebf2df02847db33adfd1a7912ad8d693430669f4cec16bb9ccd19e79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 22 Mar 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 22 Mar 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 22 Mar 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Fri, 22 Mar 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-x86_64'; 			sha256='59c6b262bedc4a02f46c8400e830e660935684899c770c3f5e804a2b7079fc16'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv6'; 			sha256='97dac0aa10961ea30a79f6fe2c4a13bfe4da562926365a63042fcceb88d9d125'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv7'; 			sha256='d607ed69f5fe92ee1fd831cf764f977174c86192957a4de678c01db671c3dc52'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-aarch64'; 			sha256='6f00ed24a846046b441c0f0a0f8c1e00194f4b0e33f2433fac0d2dd0e486fc80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-ppc64le'; 			sha256='e3afa6956f6cd4fdbaa8fe19781ae07a1bb8fb2f4d54a1aac857090d6fe1710d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-riscv64'; 			sha256='1d080f5bc04b4b97c61ce3f57ff4a7bd11299f486bc287833f162360be201a7d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-s390x'; 			sha256='5f302fb8e7d973b53f1f9dc808d2b1af08f94687cb14b3f26cc7b358854184b5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 22 Mar 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Mar 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db287e1a31efcf9777aad3e2c2c3f291dcbc6699d6f724c84e214dc0c115480d`  
		Last Modified: Mon, 25 Mar 2024 19:12:09 GMT  
		Size: 2.0 MB (2026164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e831544aa5c9d57189049c63ea52987f006bbb75724b9deecb0726779e43b47`  
		Last Modified: Mon, 25 Mar 2024 19:12:09 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb4489284b20da66de816b146752624ad53d3eda0e70a9d76dc7ddf939c983b`  
		Last Modified: Mon, 25 Mar 2024 19:12:10 GMT  
		Size: 16.4 MB (16410668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0468f26daa7d03bebe8f89ebccf4f8f3be57535a189c1b55bd421c992063c046`  
		Last Modified: Mon, 25 Mar 2024 19:12:10 GMT  
		Size: 18.0 MB (17982274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3995726f3782ab957cc5185b026052ad131d846d69d6d4d7bd501541488294`  
		Last Modified: Mon, 25 Mar 2024 19:12:11 GMT  
		Size: 18.7 MB (18669704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec7527505c01a9ff1503f472842cb806973fe24e89ced47e2a6c981bb6d0d23`  
		Last Modified: Mon, 25 Mar 2024 19:12:10 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9503abbf3673059fff872da078d8b27f029454b55109ad29e4a24d2c22bac7`  
		Last Modified: Mon, 25 Mar 2024 19:12:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76772a122dd0128244aa2ff6fecdd261df83eb325cae7b3ee80f2839730032ef`  
		Last Modified: Mon, 25 Mar 2024 19:12:11 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-cli` - unknown; unknown

```console
$ docker pull docker@sha256:fca99a75ef4bf4145733e9539690687df0a89fbcfba478b40f0f947df1e122e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.3 KB (425273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebb45d968231ef52d6731c294da90e36e2851af507ead1dea4d2c413c24b756`

```dockerfile
```

-	Layers:
	-	`sha256:df66f6dce0d0814afc407d3725f20cef89214a79ce1dbe1ffabdcdf2a88d0b3e`  
		Last Modified: Mon, 25 Mar 2024 19:12:09 GMT  
		Size: 387.5 KB (387522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0891db7a40b4db4cb4b83e72e99acdc9e5bbfd66d2ff1f2e4372c2e87fb52f0`  
		Last Modified: Mon, 25 Mar 2024 19:12:09 GMT  
		Size: 37.8 KB (37751 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:4220c50543118805771503f135a3c620420a95d9b79e3087f8d29bb72db3a87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54867156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bf35da5657d1dd22a83119adf66c0078269c816614b0df5ece0414dc173218`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 22 Mar 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 22 Mar 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 22 Mar 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Fri, 22 Mar 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-x86_64'; 			sha256='59c6b262bedc4a02f46c8400e830e660935684899c770c3f5e804a2b7079fc16'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv6'; 			sha256='97dac0aa10961ea30a79f6fe2c4a13bfe4da562926365a63042fcceb88d9d125'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv7'; 			sha256='d607ed69f5fe92ee1fd831cf764f977174c86192957a4de678c01db671c3dc52'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-aarch64'; 			sha256='6f00ed24a846046b441c0f0a0f8c1e00194f4b0e33f2433fac0d2dd0e486fc80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-ppc64le'; 			sha256='e3afa6956f6cd4fdbaa8fe19781ae07a1bb8fb2f4d54a1aac857090d6fe1710d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-riscv64'; 			sha256='1d080f5bc04b4b97c61ce3f57ff4a7bd11299f486bc287833f162360be201a7d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-s390x'; 			sha256='5f302fb8e7d973b53f1f9dc808d2b1af08f94687cb14b3f26cc7b358854184b5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 22 Mar 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Mar 2024 23:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b118eac215e4599e4010c9e5f0a1e8d36da6b557f5f7ff6cac0b485c2f1aeb3`  
		Last Modified: Mon, 25 Mar 2024 19:52:24 GMT  
		Size: 2.1 MB (2116777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487abfe1cd292c85e2f7bff0176655656a8cfb029d981b200971d5a138a7f45`  
		Last Modified: Mon, 25 Mar 2024 19:52:23 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5301b42da6d861647ddfc3b0d09cecbbab954362d40834f05a27263f99770830`  
		Last Modified: Mon, 25 Mar 2024 19:53:42 GMT  
		Size: 15.1 MB (15132927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd96011584977ee239b0fa6a2b1eb252ba89c810abb180a6d1411bcbbb52773`  
		Last Modified: Mon, 25 Mar 2024 19:53:42 GMT  
		Size: 16.8 MB (16818351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d549fbbdfa07152c9c9ca0cbbebb9dafe0a9aedc10450d6770561a42fe8f7cef`  
		Last Modified: Mon, 25 Mar 2024 19:53:42 GMT  
		Size: 17.6 MB (17631446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b39ff9786f0e336f4cdf4a91745aab6db64287bfcd940580c6d05e391739630`  
		Last Modified: Mon, 25 Mar 2024 19:53:41 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4138dd4277360a1e0be6c90d52c44e6daca90937f271cf5e25f38debbf619479`  
		Last Modified: Mon, 25 Mar 2024 19:53:42 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed529f263af8c05c8aaa26bef70433f895bd905afa4fbfd4914a6375913cb38d`  
		Last Modified: Mon, 25 Mar 2024 19:53:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-cli` - unknown; unknown

```console
$ docker pull docker@sha256:fc445a941f271c3d29dd2a40ebfa24197b2ee6c3f66254db7e66998753191170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5fe077226122e209836eb6661173a2d2576e2a587d7a04e43519aa16caf631`

```dockerfile
```

-	Layers:
	-	`sha256:bda0fdbfc8c658e38c5a056e99f0018409820d7cde5abd09cfd8a345874915ea`  
		Last Modified: Mon, 25 Mar 2024 19:53:41 GMT  
		Size: 37.5 KB (37518 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:a4e8460ebdbb81de6209afd08299f7cd30ad93f3985a82c77e0672b18c922269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53958923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58af860b4fbf8193c529c98b826a67ae28024af571d71dbb4c8f1fb940e48c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 15 Mar 2024 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 Mar 2024 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 Mar 2024 17:04:15 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 15 Mar 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 Mar 2024 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 15 Mar 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 Mar 2024 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Fri, 15 Mar 2024 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 Mar 2024 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 Mar 2024 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Mar 2024 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 Mar 2024 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 Mar 2024 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Mar 2024 17:04:15 GMT
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
	-	`sha256:ce8cafec6b550d963e5bc382529ada61abf96cd399412c7e2fd100417257b6a5`  
		Last Modified: Sat, 16 Mar 2024 15:29:41 GMT  
		Size: 15.1 MB (15129219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae6802d0c1ec3f2352b6a3a357cea342d8193b226555358473919d18c1c69a7`  
		Last Modified: Sat, 16 Mar 2024 15:29:40 GMT  
		Size: 16.8 MB (16804624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51029c41a9a83ba7e42604a1512b2162230fa00eaaf905a6c6fdb72048877d2c`  
		Last Modified: Mon, 18 Mar 2024 22:50:50 GMT  
		Size: 17.2 MB (17207758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918889663f8d6f0a6d883cdd72d4b35210027eac7d7ad18751e516a016d387f9`  
		Last Modified: Mon, 18 Mar 2024 22:50:49 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c413941ebd6725db6bba79be5784f7e0438dd09d95e4c907bba2909b9fd5d588`  
		Last Modified: Mon, 18 Mar 2024 22:50:49 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d985ba40d165906552c799cf945866e541363fc468a378f45b5a749ef00ffc`  
		Last Modified: Mon, 18 Mar 2024 22:50:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-cli` - unknown; unknown

```console
$ docker pull docker@sha256:557bd6a3d8bad5f89a2f42bb2cea6004a7d6c4b661fa6dfcaedcead6ea98112b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.2 KB (439196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f75d345752ab2bfc1630302d2923d91e050d4e6d6344f1de372ed3f42ff6c8`

```dockerfile
```

-	Layers:
	-	`sha256:a95554af0099fe2f38b780186efc6a6222b3f7cb8d7dbdf26ffdf06fbea77499`  
		Last Modified: Mon, 18 Mar 2024 22:50:49 GMT  
		Size: 401.5 KB (401463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4966e4c4537d7cd5edf1a89c7e74ea35cacde4415342d8bef02db4f6fc8c7c8e`  
		Last Modified: Mon, 18 Mar 2024 22:50:49 GMT  
		Size: 37.7 KB (37733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:df2a8285bb417990b3d3f99cc15fc1c6b3116438255605b06835b883cbd584e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54224501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9914701871113da05024a66c5744662c668f893990238dba9bcd9935a258dcfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 22 Mar 2024 23:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 22 Mar 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 22 Mar 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Fri, 22 Mar 2024 23:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-x86_64'; 			sha256='59c6b262bedc4a02f46c8400e830e660935684899c770c3f5e804a2b7079fc16'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv6'; 			sha256='97dac0aa10961ea30a79f6fe2c4a13bfe4da562926365a63042fcceb88d9d125'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv7'; 			sha256='d607ed69f5fe92ee1fd831cf764f977174c86192957a4de678c01db671c3dc52'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-aarch64'; 			sha256='6f00ed24a846046b441c0f0a0f8c1e00194f4b0e33f2433fac0d2dd0e486fc80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-ppc64le'; 			sha256='e3afa6956f6cd4fdbaa8fe19781ae07a1bb8fb2f4d54a1aac857090d6fe1710d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-riscv64'; 			sha256='1d080f5bc04b4b97c61ce3f57ff4a7bd11299f486bc287833f162360be201a7d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-s390x'; 			sha256='5f302fb8e7d973b53f1f9dc808d2b1af08f94687cb14b3f26cc7b358854184b5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 22 Mar 2024 23:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 22 Mar 2024 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Mar 2024 23:04:14 GMT
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
	-	`sha256:21e243595b6a4a5354eda3c1c4af2133475005f29ef8acc4da4821fc7fff21a2`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 15.5 MB (15459111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1ea7a6c39e124859c5e26c544d7aff02e08d3965595d626d90a9d54bb420cd`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 16.3 MB (16349525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5568a95453f2b6e3edaa3ab635303f5abba35cc86ba88c58809c0e36ac599aa`  
		Last Modified: Mon, 25 Mar 2024 19:12:25 GMT  
		Size: 17.0 MB (17046174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51731ad0253429313c84581f38908df4e40d82f8c5efe4e6cf42ca30368ac1b`  
		Last Modified: Mon, 25 Mar 2024 19:12:24 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f49db769fc4c8fd37bb2871e8d36fb7615fbee1272ea898460fc37e6106984`  
		Last Modified: Mon, 25 Mar 2024 19:12:25 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd516a23a418482ef60df4eaf7ba5944d464b15a4096a31569ae2c57851bda`  
		Last Modified: Mon, 25 Mar 2024 19:12:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0b16fa96f0778c4140fad39c2a33f600e6bb6dfd43effce310f531ec9cd05ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.2 KB (420159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1864f9e1683de74008cf477ade3669d4fb8e1ff4bef1b620c5e360979dd8079`

```dockerfile
```

-	Layers:
	-	`sha256:a3e0ae3cded460a8b49717a91e474cf6680be30f303901e0cfb32d79a2713a3c`  
		Last Modified: Mon, 25 Mar 2024 19:12:25 GMT  
		Size: 382.6 KB (382564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a911a34cb608d2aba1b54f85b082896b1f064b0db39ed3ea2b9ec4fba8114af`  
		Last Modified: Mon, 25 Mar 2024 19:12:24 GMT  
		Size: 37.6 KB (37595 bytes)  
		MIME: application/vnd.in-toto+json

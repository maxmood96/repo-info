## `docker:cli`

```console
$ docker pull docker@sha256:c5e0b27a15f49b571f968defe19cc9a072d531ee90300ba5a1d2ea4dffa760e4
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
$ docker pull docker@sha256:23b5b1a900c5676eaee32c38dbdf727a37a6ace0c5980885a9ec21da619608f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74456477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6539186f04a7291f29d299010b9ab4b55d15e95c6b0e5a7ed5343225ebaeca47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:1133514976c34d263934880176c7466336c52b261e542275beeba2b0e5917292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966754ba178f5be30b512dcf67885f9543d39a53d5299d73a475f5f65ab3c216`

```dockerfile
```

-	Layers:
	-	`sha256:45b02f14e5b651223c3c46b95436ebab9917894f4d446223811103debafdf45f`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1c3cb277d90221fcd05b69ef6a0f498fe66939317b75f5018c1cc3ca76387ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69371203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a418a759b70319d7bb3094bb667c222c2e70891d056076f8f9348a047f66c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b03cfc87f30735938381fcba67b7d48fb8e172a0426952a5c613717a6ba5126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0842d83a60027d875a0955c917c99c19935a96ef9827c37e655d72673286f2`

```dockerfile
```

-	Layers:
	-	`sha256:75aa001f9acf4b60bb11607334f3dfb7fc38dab3bc1b6fc5d19c4e11403b62a1`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:a38772a4376f984332843064dcd64529345698a31a522d9e743987c6e9fcf062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68383198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272d56ce0b6289e34fdc69a110e200627da4edddfd7d75df5a3d35e50091e40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a80bd51374d59cccbe39550e29f3c75a4898d5c2b280388e8af740da9b07164b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f168959aace97d67eaf1304c91ac8dfbee2d113d5d8603c5813758c285776`

```dockerfile
```

-	Layers:
	-	`sha256:2810d6f734119f2a44d1165a8f025decfb025d213521b3e85924d093fb8f1354`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a00c0bc47f8908b1a966cb40ffdd06470593dc098b4d6c7ac356c7f7134f9de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70172005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0075144f78e3fc8d804eb929c2cf866a2ae0295c47f80dd57a7074863ba2736b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:c97d9cee1f1276f1b5c4f148387ce7f92a0f69d5d5805e39bf0a839fb8305949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7899ba69a193c95da9272216327b56babf9364894e32734aa60a0fc96bd2c0`

```dockerfile
```

-	Layers:
	-	`sha256:225c9a7352f7eb6df35d3bd7852ecf7eb0f840312b66c6ae6e88d4847326bf7e`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

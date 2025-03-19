## `docker:28-cli`

```console
$ docker pull docker@sha256:d533232e66e7eb5c53f17210103cf738a0086a1efecec65b1589a217e4b05ec5
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
$ docker pull docker@sha256:043c259759666d273afa94a9c9175a87a11f16cde2f613f4c527e4395b703a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74401810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbbfa15156e45896ae0baa0291763d59cbe8e9197af9396b1ce4d1c3fa92030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa37ed387892ef0f453b03d3be844e1fcd5b3376c34d2e70e69da817bf44`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 8.1 MB (8062987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381596a02f6002b958b16c5e04e29d01db01a1485b673b77c2cb01e6bcc58343`  
		Last Modified: Tue, 18 Mar 2025 17:44:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c0eed6cc76454ff387c474bd923c76c78e127a9ef88ff68a6b1b0be78bb256`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 19.5 MB (19500669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75aaeaa106b9bcabe2448d5e66f3bf7e15b2c2e12daf19a415da9af9453ee4`  
		Last Modified: Tue, 18 Mar 2025 17:44:56 GMT  
		Size: 21.8 MB (21836665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d64378582a376de4f734ef70971e34646677ee7f468e3b3cd3f2841018351`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 21.4 MB (21357089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf2b75a6acd2154d8d8939cdb9641da6a68edd09dab174b2fad7a6e36b48e7`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f13a3048c854b126d4474825f72c5b7e88b7f20db6e2b20804ae255f67dec7d`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f041ff7f4b86cd37deccb75ed8eabb72375f275fd1867ad3c5360da35b73742`  
		Last Modified: Tue, 18 Mar 2025 17:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:054d1a0f0d9a7354f4ebcd12afbbe2a9020155beaa0ec46770c789ccbf1c7a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e93df1fe28f45f774c9bf9ae35f4ca1912f62366ff899cafd275a526941419`

```dockerfile
```

-	Layers:
	-	`sha256:bac4c3a563812a6f84462124d368a71f165d3ee1ef9df06d3da71b7cca36e7d9`  
		Last Modified: Tue, 18 Mar 2025 17:44:55 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:2af701b2acf52ac01aabe3f7b24129785436531e6994b6d19a75101c844b2aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69324552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f31a9e113936d6381be6fa03f180d10952d7db5923ef4da1db2e5c4d6ffb1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b09fa191c121508f9a9d87798bb34995414e0d3faa5f809d1e62e19860660a8`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.4 MB (20434194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6403c00baefb96711f430c72def01b60a418362d712aa7a1e306ca7a6d847f`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 20.1 MB (20082303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39f0022c40821c098b1929dc1e74fe8c0b353024e3c7ca30b209a99841fa13`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90aea4ea3008d94818b62be572f32785691a3f3cb0458f919f54c5a130bb898`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8b7518e8da521a85b7dbd871f1e1f860ce73d9863a671cf7ccc1737870143`  
		Last Modified: Tue, 18 Mar 2025 17:44:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5e3d207e61cde6b1bc54354f37f0fbad8172bfc2584f0f5b511d0c598048f59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d14fb837116a45283ffadd7317ab0232cd066d977df7dc75bbd371ef47aed6`

```dockerfile
```

-	Layers:
	-	`sha256:0f25bf12b560e48dc887224d3f73240586d2726286656f557d257939d0aacae9`  
		Last Modified: Tue, 18 Mar 2025 17:44:34 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:04807cef21610146931e7f832e432dd6be839755c5c24f82fa9874c484cbbb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68335053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb05e9491231e4be13e7ab718281fbafe06de01645b4397b60281bdcd298495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
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
	-	`sha256:f1080dc1ff56824d3ad13b9275f6a95c0abe01e8607ad4edccd1992454435480`  
		Last Modified: Wed, 19 Mar 2025 04:32:32 GMT  
		Size: 17.5 MB (17453632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66f2fd753e6ed68df1fc6f7be57f2118f38a30d7e503b6f82aa3933778b796d`  
		Last Modified: Wed, 19 Mar 2025 04:32:32 GMT  
		Size: 20.4 MB (20414145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab45acc9674ad87ae2d92c8247281226d7ade24e5f9a8da000aa0baa8b48343`  
		Last Modified: Wed, 19 Mar 2025 04:32:33 GMT  
		Size: 20.1 MB (20066339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5420da33d776f0ff4624b323fb3a0b479092e26f5bcb9aad1841470f8ff315d`  
		Last Modified: Wed, 19 Mar 2025 04:32:32 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f245c6b6fa68cd42f432cd4dd196c81d7e3890ac45b5d164cce0c21dcc4d29`  
		Last Modified: Wed, 19 Mar 2025 04:32:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d447a11f6eee43033e5c99ef8347a3cefd7f10a7e2348ebf7f43d4c70bae3b`  
		Last Modified: Wed, 19 Mar 2025 04:32:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a2e137e5fa2b8ab9ced562506f581d57de1b5238bbe995f4a990970daf158ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25553b8d13e1d0593421184934cb634d52e312c29d285e5958a99ef3c25c4bdc`

```dockerfile
```

-	Layers:
	-	`sha256:0785759120a3578c878bfaff7ea7d6a403204aa4a67ee51c0e94070970fa9af5`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9c69cedb70e576809b1c4bb33946ad8d85529f61c03e4b8f4641ef2e2c12c13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70126294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71220c9f3c0d88be6dd15374a7cde12582c3decef4a2ad6ac4ee45b346fd333f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.3
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-amd64'; 			sha256='47f456339ca8926efcb7266f700a3bbb8a472585d977e7e2f6f22242ea6531c6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v6'; 			sha256='79ec391c50d1ebb3f38e842dcb8b27423f07b4554dd64052a08e82387a965fcc'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm-v7'; 			sha256='b5ecd26229143997cb597ba1c705def85d85dccdbfdbbbbef44bd84c9a0c0a54'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-arm64'; 			sha256='90157681a0a033b285e80d3350741452d7647994fb371c9ee3a423f2ca4f22cc'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-ppc64le'; 			sha256='d27713f8f297db6e808787a15843a3af0b345a53ff23dac53b775ad8277d408e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-riscv64'; 			sha256='bf34fcc2d2d78ae5aab34f515d952918451e849f06739dffcc6f9d87b1bfb1a7'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.3/buildx-v0.21.3.linux-s390x'; 			sha256='73a6738f54542115ceeb92ecef751703f9d868607280ab1715380d9751e35ccb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Mon, 17 Mar 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Mar 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Mar 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 23:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab078fb8e0936c19967fb29bd3d05d61ebee79042ae86372272ab15db3888f`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 8.1 MB (8076579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a691aac23055f287d1a1d8ac0213059467a98167e65ab418beb14db59519a12`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd9f42ee1e553f23d5e353e3c57eb63e837193d94fc2dedf12a1a4bf393d08`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcbadbd125fca403235efa4b6145914c0c83132dd10dc1f49b0cb57a1e9a24`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 20.0 MB (20047022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471ac8872a7153ba16acbe3d15032d400e639da065961f9dc95746e8195b7af3`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c4a5ee6facaf9ec7eabaf3f5fd747ab8ce399d9de99194a4b90eb127e8f1f`  
		Last Modified: Tue, 18 Mar 2025 23:59:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8626a45c25ab8c417b0af3400ab2cdd97c612ed49317f7c86e11dd42341a7a0`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0743648b6c3803db6a13374054a9de32a5947fda7e40aa129f766508b478627c`  
		Last Modified: Tue, 18 Mar 2025 23:59:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a846f337948335ee9c66b55db9f4242f141b62ed0ac940a7308b6234a44672f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a466e3dd4f8d4aacc72abf776fe2dfb6d6eb6906cb0c1dd8bcca331951704947`

```dockerfile
```

-	Layers:
	-	`sha256:337cad1d65245942e78863cb17cababc17db3c09293347e6e4ce59e58b6d2e1c`  
		Last Modified: Tue, 18 Mar 2025 23:59:16 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:22eb9db6081c0bc3c05137a5e8f26720e1b09aaafd3f18b923b494bcd6283a3a
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

### `docker:29-cli` - linux; amd64

```console
$ docker pull docker@sha256:93afea9ac780f8706540408cba1e801ba285071476b0c2bff424a0ca0037869c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65959799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54560465c89852384428d8b003c70278f2a11fdee74fde28173fea1077416da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:43:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:43:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:43:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:43:53 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:43:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:43:54 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:43:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:43:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:43:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:43:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:43:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959d822c11f4cffde22f6a8ca77070ab678788ee8a60e50bf52240fab7600d55`  
		Last Modified: Tue, 19 May 2026 18:44:02 GMT  
		Size: 8.3 MB (8311621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf748eeffe46320957e43a6d041504e02f6d54efaa90b05ea0a5e76259a3bc9`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29db3e4d2cf2bffd95a0b8c095c0dfc7f4b6ee9717169afb9c613ae0714f22a5`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 19.5 MB (19549501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418895c8a0097a67712f5b2385b094ed4ed5af1359b9b43cb86c07da48ca11c9`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 23.0 MB (22988580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4382b5de8ae74e74d495d9d94f0127cf051728dc00cab26dfa163bba8cdbcf13`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 11.2 MB (11243752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53914aaed626c98320ff52b5bbe81eb804e9a82d445d07a5908e16e86ac5a5c`  
		Last Modified: Tue, 19 May 2026 18:44:03 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac0928dd7f6aa6c83aa987350f200df21db15618f2ba47912f35be2b16b3b9`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c069fc81d4d790f039a7a8160f23dffa6c11a22ee385a0db0fe75ae235dfe1`  
		Last Modified: Tue, 19 May 2026 18:44:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e6e636232d7064d32da9c46ef93c11a565c43d61068daa1785a2d63bb664c190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973ee0a24a2536030656c4b9be0b463122f73df6150f6b0949b3d3601798afd1`

```dockerfile
```

-	Layers:
	-	`sha256:dbed7195f208034adcef893e2efc57ce071c5d914a8a9624d5a8a7fbb1a9f99e`  
		Last Modified: Tue, 19 May 2026 18:44:01 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:663439730373cf7597a3f83ae50ab11f8a171b59b1e9ce95a730be4c0b42eb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62234030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0de2aee792b8ce4ffb303432b131ae0026fdd58af954221ecf5bcb4f293705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 18:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 May 2026 18:46:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_VERSION=29.5.1
# Tue, 19 May 2026 18:46:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 May 2026 18:46:29 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Tue, 19 May 2026 18:46:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 May 2026 18:46:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Tue, 19 May 2026 18:46:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 May 2026 18:46:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 18:46:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 May 2026 18:46:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 May 2026 18:46:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 18:46:34 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e510993d358b2182e33432b09c723cb2de90442627624e753d33ff6f58e37cf`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 8.2 MB (8211856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6422e386e61fe4ba4eb1abca9f67aef1bba270f947f3797505168eddc865ef`  
		Last Modified: Tue, 19 May 2026 18:46:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c6104ecd7c2122cba9eadf591b901752e839d28c94e9786023634ab16c4e86`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 18.2 MB (18183185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9278a90d0e78f94da7f59f70fe4811830047483868d42c4e25a85b91a3359765`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 21.6 MB (21614147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f94e1195a7d62fc4046fa609e325b2001195cf49352924129c45728445d565`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 10.7 MB (10650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8126c2985de246f1344d8c4340e5934b14cdf06f269351c0bfeac534be4c3a`  
		Last Modified: Tue, 19 May 2026 18:46:41 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c028f2e167a9ccd442fe69b89b5f1ca9e19f4589d7160d5af4d3b451ba862`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa9769c6262cc549e78864817d114f4780b6b611ff08c097bcb018ab9040fd0`  
		Last Modified: Tue, 19 May 2026 18:46:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:866404ab9edde4226ee79d91959d86956cc3fe71a933e10c9c282f3bb9fe1e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f84764e1609e718085281484003ba89b5bd9d8cbb6984808cae3079115e48a`

```dockerfile
```

-	Layers:
	-	`sha256:60a6451bb1e2eecccb01163a32454bf66adbc39c153e56f1b682485c3f73fbc4`  
		Last Modified: Tue, 19 May 2026 18:46:40 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:9ec11722eadaf4ecb19592ea19d512fc17ef941738677435dc52f1f70e3b4da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61215589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376a20891ab4edb0bcada5d8b3ba3f89f105c6351ce5368f2cafee22c9c2e764`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:11:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:11:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:04 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb53acd779ed72fcbca92822c9c8dca72fc19b59b4367fc8edbe5c8edd184829`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 7.5 MB (7520515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3717dbbea465f22997cb871db7b421cb78bfc5d2353e0fbb9c24a4d7f4eead8b`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2765ebda46cc899cbdd1066e7e900d81e9e6227536c38218d156a6c6ffc93324`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 18.2 MB (18172266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8e62c2751306352d388df5f6ed3f91e4f160f2da7a249168dc387777896b44`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 21.6 MB (21600397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74677ed12033b201cddf684740d6f5f9540e22ab253c874ab4d21644f5b592`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 10.6 MB (10637133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d76fc015f6b878f4335aa2e01b8ef18fcc9e9b2cb962b48d46350deb994e02d`  
		Last Modified: Fri, 15 May 2026 22:12:17 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad7ca5f5e6e176e7d1835e181fe35affc2155c45a6a1148aa7f18ea76d9d05e`  
		Last Modified: Fri, 15 May 2026 22:12:18 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdab469dc84864d9800ae053f9d87586d2515da2b650cf6f13f5ee84e15b2276`  
		Last Modified: Fri, 15 May 2026 22:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3733f58f759836ce9f96949b34cf083d5873acad577a5181e080afb4bf3249f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f8c9cf97e3e4d9ec70c8edcea1d71eca3c988ea012b28acc4d35eea629ae37`

```dockerfile
```

-	Layers:
	-	`sha256:7ce1554139b841ff42f6ca82b422a07755ca34b9f40a43a8f69db42b7b360f47`  
		Last Modified: Fri, 15 May 2026 22:12:16 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e211ecf9a3c37d57418eef652252ba0ca62fc942cdfa0d8dec160bc3086bd9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61632856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4f6ad10554b836d3f6dad4bf015212f96fc505f746c44c549df3e29d3fd2a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 22:12:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 15 May 2026 22:12:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 May 2026 22:12:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_VERSION=29.5.0
# Fri, 15 May 2026 22:12:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 May 2026 22:12:17 GMT
ENV DOCKER_BUILDX_VERSION=0.34.0
# Fri, 15 May 2026 22:12:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-amd64'; 			sha256='0144479d5a1cd710be3464ae898628cfa68033e16b225aef52f81930c45ac9b5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v6'; 			sha256='1f34337385921c5da43d63452282726b062aa887fda975f96dd3d6e869648bc6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm-v7'; 			sha256='3560b5b6fd3485f4d0bd160e7edf56cc1f08f0cb5852c9af28bf3fab9973c7c2'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-arm64'; 			sha256='565605fe0bb393ed5d11771e5b52fc7ef05c701868861fa85609747c9d74a440'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-ppc64le'; 			sha256='c5ef8012f48a518e1c235ad408d26cd424d7b5fa87eaf78cb2ff4b9048730120'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-riscv64'; 			sha256='80b27d5f3a346591a5045b81217ee5be578ed151ef8cbd883a892c0ec0ac33f1'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.0/buildx-v0.34.0.linux-s390x'; 			sha256='04f5bd0d389f682c7e9287a3b3a1777b0848f8e10d58cbf9d4d12c9002bbb378'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 May 2026 22:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 15 May 2026 22:12:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 May 2026 22:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 May 2026 22:12:19 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 May 2026 22:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 22:12:19 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51147f6d8210f56d90e095c69db7468c6a7f4c96b15954bec62a38d029c230`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 8.4 MB (8368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca485120792b1bdb82820fd08df20937c87c36c02b044d113785a278f04c9c5e`  
		Last Modified: Fri, 15 May 2026 22:12:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be2953b1820f6b03454f4cc64611d855fbccf3feb3c9d49c80e129eddcad5`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 18.0 MB (18003835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8387c97690c1e6db50aa3de5c90f1742500af7c360287ddfe4acd0578e0eb`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 20.8 MB (20815340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3087ee8252be9dcbda43072f57a958f8f37983b3932bdca55c49fc7420da93f`  
		Last Modified: Fri, 15 May 2026 22:12:26 GMT  
		Size: 10.2 MB (10243274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027710042ccab2488d5291cd625bb62305844954e320f530f618c56b53ef928c`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557313fec61d76b6a60306c806eb278032cfc80335daa86db37ad9979e81756`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074eaed06bf00c4914e361b510e55cd12bb8b0305b732d777ef95e01914b4f4`  
		Last Modified: Fri, 15 May 2026 22:12:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:06da91c70ff029cd54c906f93a84997c38caa126b495b2f94c29d83561aa534a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c299b9b46a49c14a1255ad31a3c17438482a28e9408b1dcd36db58d87d66247`

```dockerfile
```

-	Layers:
	-	`sha256:912e2047614870aa935e1c45fd05fb52050a876007557a6795c50c8237ff6549`  
		Last Modified: Fri, 15 May 2026 22:12:24 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

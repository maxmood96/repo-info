## `docker:26-cli`

```console
$ docker pull docker@sha256:a57c8422ce20c07cbda4de330b1edfce77438c4166a0b8a7804641c0d804c04d
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

### `docker:26-cli` - linux; amd64

```console
$ docker pull docker@sha256:21d912433d713310cbd122a332a22944859088658012414eedfb57ee23ccceec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60520147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a166850b75ee5082e2fc8a4d12f7b59d4cb9505d705d1722562b45e481968f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:09:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 22 May 2024 19:09:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_VERSION=26.1.3
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 May 2024 19:09:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 May 2024 19:09:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 May 2024 19:09:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:09:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cb2a59ced673275c4d194fc0bf5a88d16561a08dc3bf1e300878396a062eb`  
		Last Modified: Wed, 22 May 2024 22:54:40 GMT  
		Size: 2.0 MB (2010472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb247a8f83e747078be96970bd4a0b1550bc53508f29ec882ee2c629ee5c9e95`  
		Last Modified: Wed, 22 May 2024 22:54:39 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32499521033d872bb3ecaec64746bb66e8865da4220597373b6ee8e135138d2`  
		Last Modified: Wed, 22 May 2024 22:54:39 GMT  
		Size: 18.0 MB (18031645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38fd5a68d3448d81e597d18b7ba48addada8c54857f7d350f4f10068200b415`  
		Last Modified: Wed, 22 May 2024 22:54:40 GMT  
		Size: 18.1 MB (18089095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421921fd35be50f14f772e703fd96c5f47727915d87b24d22eeafa897f76d2e7`  
		Last Modified: Wed, 22 May 2024 22:54:40 GMT  
		Size: 18.8 MB (18764679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcd32e1b4bb951b68185e09df7da620b58563f8b93ba02db839bb703d0bd0d6`  
		Last Modified: Wed, 22 May 2024 22:54:40 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6456e0b3931787e86695d10d8725381d2c98ffbda04d774c3a11fd1dfc3bebae`  
		Last Modified: Wed, 22 May 2024 22:54:41 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d97db5952e9161d03e0800789a7ff38f8e585a9c939c108e0c2c925d651b7ad`  
		Last Modified: Wed, 22 May 2024 22:54:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2ce3d885bcc89e85de0016ca1f7dc03c062db0e4e4ff961c2bb962390abd0a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a457024de7675f947739e80a68fc07a7dc01f147f2da1f5567df177d38005bec`

```dockerfile
```

-	Layers:
	-	`sha256:6c66f63094ff5f7813cf5839bf2f3676563685a2a07f2fa66875953c4628c9a8`  
		Last Modified: Wed, 22 May 2024 22:54:39 GMT  
		Size: 37.8 KB (37827 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:3986ee89b2c6c0cf73d079f9cf0895dfb79297533d7a7bf588872f8382bf94c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56329547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d8a93aa003e44f7679a2f5760c5c39757d2cda321f03a9dd7f051cb86b4f90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:09:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 22 May 2024 19:09:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_VERSION=26.1.3
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 May 2024 19:09:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 May 2024 19:09:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 May 2024 19:09:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:09:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2863b6e4728b0513981e38cb0cc25f74d957d69a3f91a81349913f7a35b4df40`  
		Last Modified: Wed, 22 May 2024 23:10:11 GMT  
		Size: 2.0 MB (1993318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352afe3e78919dd96f99a9990219479e1a427b80e2ce44e78392532814857308`  
		Last Modified: Wed, 22 May 2024 23:10:11 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121f9c0cfe3ca50953ccdb5f96b2ce6fe5b7a0643617a8e2513bfed0ec31ca6a`  
		Last Modified: Wed, 22 May 2024 23:10:12 GMT  
		Size: 16.3 MB (16326345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f6b7c1afbd6531fd8d1fb75871557638429f4ddf5a8bbb3cdeef5be66d6bca`  
		Last Modified: Wed, 22 May 2024 23:10:13 GMT  
		Size: 16.9 MB (16916100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9c1d3488e143123ec43fcada3dc17df3331f70ebe72bef803e15c2abb9245f`  
		Last Modified: Wed, 22 May 2024 23:10:14 GMT  
		Size: 17.7 MB (17726567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd7af48d9fb34f7e70ff5aee8effa5aa49a1fbbd3a3b7aac976cf82d8fad24a`  
		Last Modified: Wed, 22 May 2024 23:10:13 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117fe24024b14b1d6ab5070fdb9e9973d2af787928f91bd83c07f14be7096eb8`  
		Last Modified: Wed, 22 May 2024 23:10:14 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a501b3274f71f151c98aed5894fb0f09a898077462bf1c263177455dc2ee35d2`  
		Last Modified: Wed, 22 May 2024 23:10:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:859870d96b3765b81f92529379d1762b066777eaf916278797a041298a15a82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26c518f2d617094a850ad8b4b59993e324e87e15f187cfef3c8ec5d9c1b514c`

```dockerfile
```

-	Layers:
	-	`sha256:aa187a8ebac5906887c4242d48d93df6a3ec0b6742dcfa9e31bbec4ef893d0a4`  
		Last Modified: Wed, 22 May 2024 23:10:11 GMT  
		Size: 37.8 KB (37818 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:a07ba58af38d45eeaf819d03c7cb23dc26de8baaa838db02d6ec1dcdbf7316de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55874186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8984978970b623b4c0c631cde1e9ce6a711f46924dd484cbbf9ab26fb48d2bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:09:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 22 May 2024 19:09:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_VERSION=26.1.3
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 May 2024 19:09:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 May 2024 19:09:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 May 2024 19:09:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:09:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5c6f7a405660615a06b7d5d966e10fcf15352fc52f8276f2f985a2fdbc131b`  
		Last Modified: Thu, 23 May 2024 00:40:04 GMT  
		Size: 1.8 MB (1841223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86e7b10d2ec33c904ae8e224344ce970078ff58a41aa11591f96e48eb0c4223`  
		Last Modified: Thu, 23 May 2024 00:40:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5356bc95ad6f482a22537e21d66bd6e24ff51d866fbd2ad842d7c00d707ce9`  
		Last Modified: Thu, 23 May 2024 00:40:05 GMT  
		Size: 16.3 MB (16317800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4cfd0dff942402111740420d898ea6c95f618ad775cda47b3d967d81391b3e`  
		Last Modified: Thu, 23 May 2024 00:40:06 GMT  
		Size: 16.9 MB (16908311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6cafbce69372876d6c8c1a7f9b43f0ac876d3f7526dd07b042a5f8ac077058`  
		Last Modified: Thu, 23 May 2024 00:40:06 GMT  
		Size: 17.7 MB (17710658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a042f387cf0201d03fd9597f03a47fad3590b9c1f9ba60bb64d23a3835c9d11`  
		Last Modified: Thu, 23 May 2024 00:40:06 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a674158d44010688eaf490da507723c9593de44f9439657795ebbe96ebfaf2`  
		Last Modified: Thu, 23 May 2024 00:40:07 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f1a027ee4eb52d40380a555802fc09008f2fff9462b9c3a45b1f83bd300eb`  
		Last Modified: Thu, 23 May 2024 00:40:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9bc5dc39641b13c871f0a7145820cc0d0fb1a3ff7073515dba22b5f007966420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b0a199d9b29d60436e3593b0756fa06c16e1ae554347af6df17ba6da624fb2`

```dockerfile
```

-	Layers:
	-	`sha256:10e0e97178c43c8b0b5ad956c11ffa7a7705d7b2c5642a0973e3b03121c9aca7`  
		Last Modified: Thu, 23 May 2024 00:40:04 GMT  
		Size: 37.8 KB (37818 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6c6ba385c8d6d6f21c5276791b9bd1cc8fb4238a3c75b77be8c770e20f4b81d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56669093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad83571fe4b5f4e6d46ed4a39c5f37a4ef8774b7c8d0caac777d15bad73da722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:09:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 22 May 2024 19:09:49 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_VERSION=26.1.3
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 22 May 2024 19:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 22 May 2024 19:09:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 22 May 2024 19:09:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 22 May 2024 19:09:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 22 May 2024 19:09:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:09:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeff538fc611c5175105f9f005c3552426210b835f1716c1b5e1521c54176b7`  
		Last Modified: Thu, 23 May 2024 06:13:27 GMT  
		Size: 2.0 MB (2006606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b49800f10e13b1bd816fa74ace8882c4c7340e84c68b55a44add2715286e4d`  
		Last Modified: Thu, 23 May 2024 06:13:26 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bceab9a87f0f744c442f0fd063f1a00e0351a48d6c4476028febb80586c82`  
		Last Modified: Thu, 23 May 2024 06:13:33 GMT  
		Size: 17.0 MB (16988430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061f435c49b2fa9f18104b78ef3de0960c5e4c93a6a60a60f0425ca393358b49`  
		Last Modified: Thu, 23 May 2024 06:13:27 GMT  
		Size: 16.5 MB (16450822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19b16c332f9523cf5299647fe3decef4a10241a395420fdcf7a62c91eccfd27`  
		Last Modified: Thu, 23 May 2024 06:13:28 GMT  
		Size: 17.1 MB (17134298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eb2e65793799cd32f571ae16f4f26a892bc383c1a452d8c383b178926dad6d`  
		Last Modified: Thu, 23 May 2024 06:13:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6846f7d028260698208b6ad0eaea09f5aae1e04c937ea835936fcc0fd22c3164`  
		Last Modified: Thu, 23 May 2024 06:13:28 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673d1bb4a6e79d9eb543938b510283ddc0313aac961761d8e20b4a2a68e80ea1`  
		Last Modified: Thu, 23 May 2024 06:13:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-cli` - unknown; unknown

```console
$ docker pull docker@sha256:49e41d3ea59f8d5374c2b310ef785a3e3fd74a02bfd048484e95ebef81b26a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24623ab418be32da917e26abea52b9a80152a736a38ce0ffdb5e13aafc6dddd`

```dockerfile
```

-	Layers:
	-	`sha256:704aacec552d3528cec6f05583d2bbab366b9e3c694e67fd0dc11a2e46d343f9`  
		Last Modified: Thu, 23 May 2024 06:13:26 GMT  
		Size: 37.7 KB (37674 bytes)  
		MIME: application/vnd.in-toto+json

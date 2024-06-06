## `docker:cli`

```console
$ docker pull docker@sha256:5fa382ce1c0cecef3c83c3bab64d38ef6b23d3460573f943fc798db5a6006f6d
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
$ docker pull docker@sha256:8139703b330f698840f846820f526b343cfefd8ac3b3ce21ac9a31399db65c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60554574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1af8914e0a57df38fd99ec07dd3d28892e0fd1aaba3b03a9532bc5907001e0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6078ef297057e0f7c5b340bcbd171a1fdcdb6ebe9a9db3db32f7c7f7053b451e`  
		Last Modified: Wed, 05 Jun 2024 19:53:47 GMT  
		Size: 2.0 MB (2010485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec122f0d962fd662a31cb500909545708e551517a1c71780e752e40a956a870`  
		Last Modified: Wed, 05 Jun 2024 19:53:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca60424613dce47aa4cd74cd5ef17acab13b4c499411d4baa81fd6b7f189e7b`  
		Last Modified: Wed, 05 Jun 2024 19:53:47 GMT  
		Size: 18.1 MB (18054139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c566a1e5ff24d785269fb6dd158887a795d94ea9eb635971f5a9c0d898d2375b`  
		Last Modified: Wed, 05 Jun 2024 19:53:47 GMT  
		Size: 18.1 MB (18089103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92217334f819e4bdd753396764ac6a7863c047ff3e0e57aca7994f9f2ea30dce`  
		Last Modified: Wed, 05 Jun 2024 19:53:48 GMT  
		Size: 18.8 MB (18776581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3464b44de8798fd61bfffc12a4e3aa29aced4d9dd0ebb8c91ba035120bcab9d`  
		Last Modified: Wed, 05 Jun 2024 19:53:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bddfcb55e5d58a502a3a78689fcdca0877e94c273fc21b6f6a2433dea6276e7`  
		Last Modified: Wed, 05 Jun 2024 19:53:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16d2b1a991d014ad82edb016606e3efaecb9ba86b96bfb19fd5de6d4ae83a05`  
		Last Modified: Wed, 05 Jun 2024 19:53:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:cf5a5c62eb56bc544087dbf3c1061cc3754ab7b08575274fd73035b587020ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370f0f87c718efd2c0191885f07e381368e1021654c00baf6f436ac6e47bd12e`

```dockerfile
```

-	Layers:
	-	`sha256:14864f10e8dc06d7b716d21e29a2cd3c397f98f7132218c7d614c4d2a109ed03`  
		Last Modified: Wed, 05 Jun 2024 19:53:46 GMT  
		Size: 37.7 KB (37711 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b4c8bf25d7126341d4e5f729a0fce5d3462c7e1861c49520fa842c34ccb73d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56344901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3753cdb6478a90a3ac939bde4e78230fd2697b12dbb2087890c54f13c0373d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06403ab95d3d601d04f073f82627c9db7565c5ff0f4b4fdd691714861953bc2a`  
		Last Modified: Wed, 05 Jun 2024 19:53:42 GMT  
		Size: 2.0 MB (1993315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8421477ba9f164a03ba7f4d32c7071fb0e840c04221c9f411599008e3d71d2f5`  
		Last Modified: Wed, 05 Jun 2024 19:53:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61cbdfa95f0fdca7da47d75f88dca7838ff437a02dc52bc93f1a542f4c716aa`  
		Last Modified: Wed, 05 Jun 2024 19:53:43 GMT  
		Size: 16.3 MB (16329502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb751942039be62475b91bc8ec9d02af686a4405fb36dc891f0c601cd9984b00`  
		Last Modified: Wed, 05 Jun 2024 19:53:43 GMT  
		Size: 16.9 MB (16916106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c382e859d55a3ac73ac82ff6abe87545a0d8ebe8dbb30495dca2d42cb66cc1a1`  
		Last Modified: Wed, 05 Jun 2024 19:53:44 GMT  
		Size: 17.7 MB (17738752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8d79244f1b5c48742514ad17c7fe71cf217edeab9140a15fff50b7b5800ded`  
		Last Modified: Wed, 05 Jun 2024 19:53:44 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bf2cbd818e60a907ca08387f99d34790bc69507224a0dcf211d0986d161418`  
		Last Modified: Wed, 05 Jun 2024 19:53:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d125905215ba5ec9166ccc9c3e5605d0b1b1eaa8d4bf1ee4b14f0ddc022a0657`  
		Last Modified: Wed, 05 Jun 2024 19:53:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a42d9d4fc77921c75353ba56ea0c42993e7a89973783bed9db1c69d91ad19643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9365a7769d6d9f2af6d8574d34714d4c00fb608ea6b812d6e8efacdbb3021a40`

```dockerfile
```

-	Layers:
	-	`sha256:e704863254f08ea000d21f0e628f51ed564bf48ea25f1fd47a1c55a33ca773a3`  
		Last Modified: Wed, 05 Jun 2024 19:53:42 GMT  
		Size: 37.9 KB (37867 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:0aee9829d308393bb18400d17348467ec025979cc0b33b184abe0521cfa5b5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55886359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444128034e9c9040f5a8e98f7c4c32dabf9600c605315ab081fdf9de0b037189`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a8e77ea95dde50e081ad38e5d1ee96710e1135104592d94bfe9b7196dfc3d6`  
		Last Modified: Wed, 05 Jun 2024 19:53:35 GMT  
		Size: 1.8 MB (1841224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcde31c960324e5db2de3957096240837d1c7317714fd30c2ed21bfdb1936e1a`  
		Last Modified: Wed, 05 Jun 2024 19:53:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6e44d361e3671e3e10c0705cfc2d254da99fe08fdf3aa68fee83aaff266e30`  
		Last Modified: Wed, 05 Jun 2024 19:53:35 GMT  
		Size: 16.3 MB (16319673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97f04fe6de754ce3c994e9c4d746489805bb6400ca871ca204e8411ca93d275`  
		Last Modified: Wed, 05 Jun 2024 19:53:35 GMT  
		Size: 16.9 MB (16908323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2514f35f9e14b9e2ca8876d258691899a64945de8ea8ce3f81d8dd9a36bed23d`  
		Last Modified: Wed, 05 Jun 2024 19:53:36 GMT  
		Size: 17.7 MB (17720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820db871b9578c4eaf6439341d97df29b05acec52e3942bac450f51076c9be28`  
		Last Modified: Wed, 05 Jun 2024 19:53:36 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c1fee398eca22f4d22e9d6557fcf2ad1d5db00b768f7703dd991630f1604a5`  
		Last Modified: Wed, 05 Jun 2024 19:53:37 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1090bad840b6a6e2f5b94ed2d4d8ce6b0a74956432841caf3d61303e2da624b5`  
		Last Modified: Wed, 05 Jun 2024 19:53:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:d79d4f286e6919c2ac62054b2973ea97dcbb7f841a972511175852eb95b53623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d92eee3250adcff151f964bc864ecb678212046cc5839180bd160ff16041b58`

```dockerfile
```

-	Layers:
	-	`sha256:176782b0ac8470c2fd924775115404d32e03bd55107ec24bfde8152edb5fd014`  
		Last Modified: Wed, 05 Jun 2024 19:53:34 GMT  
		Size: 37.9 KB (37867 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8bd7ea9e7a4a14baa452b56176eb4f9406c9fe34989b40e7f235fe09c51c9eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56702791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fe0fc18698b3b8a6a1ab60f83384d17cfe2e8af5926e23df70924c5cbc6af1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d756e38ca34a843f4cbd95ec36aec8a5395c768ee0b27ff0a08740c6bea4ac`  
		Last Modified: Wed, 05 Jun 2024 19:55:30 GMT  
		Size: 2.0 MB (2006617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e41820f0b10d7f2e27295a5b776c1896dc67cdd473789e76808a2b544fa4d6`  
		Last Modified: Wed, 05 Jun 2024 19:55:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2262cdbee266c87a0a27299467946362a2439bec202bdb3bf5ea63e1d1b4e037`  
		Last Modified: Wed, 05 Jun 2024 19:55:31 GMT  
		Size: 17.0 MB (17011535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24054fcebdc5d5e13596fc2e5111138fdfd012fbd3dfa5694eb777c6fa43ed2c`  
		Last Modified: Wed, 05 Jun 2024 19:55:31 GMT  
		Size: 16.5 MB (16450839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb62ed300d80264c145cd8b09dfbcf20ddd3b9c62b052ec11389c88a17616ea`  
		Last Modified: Wed, 05 Jun 2024 19:55:32 GMT  
		Size: 17.1 MB (17144851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be5f580932489a97a4b43a55882c67d45c5c64b5678351d2028d87dcd55a99`  
		Last Modified: Wed, 05 Jun 2024 19:55:31 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3788af95e0f46d61eca561d4e558894f6df1643259fab7c1563d4f40a96249`  
		Last Modified: Wed, 05 Jun 2024 19:55:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9bb6683660a31ba553acc409f01ec3b325ada03a18352552f81d293e39a41b`  
		Last Modified: Wed, 05 Jun 2024 19:55:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:28c70b0d8eb464daaf415f3ad95f54627f20c8e090d6a3944370b19de71490de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24107dde2fc62b5a6d71ccb5dd984be0dbf3a7df27debb722a54b9ab24a3415`

```dockerfile
```

-	Layers:
	-	`sha256:c5405207956d781bd1550a6e45c1e47a81307e372d423b948d0797bde2517c3c`  
		Last Modified: Wed, 05 Jun 2024 19:55:30 GMT  
		Size: 38.0 KB (38023 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:cli`

```console
$ docker pull docker@sha256:ce5ca0c57db0e5a43bf59a7cf62c2309b53f63dc86e18521798744054c000024
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
$ docker pull docker@sha256:a5b59cb5d3566306a49b0d5327a5f587495dba666f02465a9bd17f336b717f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67573462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eead92024b60db078c11c4de32c42ecc9692bcc500301f52f922f7a0b5b9334c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.4
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-x86_64'; 			sha256='2eb8de746c0bc724bb5da4de52fc9660c2e866afc9a639ffdb1adfef2649cc0c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv6'; 			sha256='ad707af427c3d3574c9e7dbc77915dcd06779a58e2c3b3783f7781166213454e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv7'; 			sha256='bd473fb4fcdb6ff9d1616d7ff3294387a574298083de91a36eed2741341f3c97'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-aarch64'; 			sha256='d95d239bec166137a1ede1d441cb808da800dacc6041c966be35066aa96c6ee7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-ppc64le'; 			sha256='72d4359904b6821b04b77f7dac609b994847838d1d38e5840362d64dc35d9bff'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-riscv64'; 			sha256='34f859fd5b5d3f081a88004ad9a165b01f5b549abb76e0b99a3281bc963ebbde'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-s390x'; 			sha256='d4f333a3abb6f4904e75e56196a3e6671797ef2f5e09cfbe71263f2dad466ea0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 16 Sep 2024 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Sep 2024 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0966a0f631285640f25edd7bba35753850ee7393b097de621f6b37e7ac11a4`  
		Last Modified: Mon, 16 Sep 2024 18:57:16 GMT  
		Size: 7.9 MB (7872601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26149871b493de74f6a37424eeb87e9e3e7c613491280a34b65f32da554c42e9`  
		Last Modified: Mon, 16 Sep 2024 18:57:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaeaaae10d5fef524c17e571bdfb9795c5467ab9c7e0ea9d782e9f001b0ab891`  
		Last Modified: Mon, 16 Sep 2024 18:57:16 GMT  
		Size: 18.6 MB (18601176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd93dda3ae202c3b16bdca3149afda5b74c76b40c2a25378239edc44c5f176f`  
		Last Modified: Mon, 16 Sep 2024 18:57:16 GMT  
		Size: 18.4 MB (18437722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdf299cbed4059618163808f1e0e0aaccd74e639c88ff8e923db474351945fa`  
		Last Modified: Mon, 16 Sep 2024 18:57:17 GMT  
		Size: 19.0 MB (19036007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184f1bddc792fe42fbf95d2fd9cef7e723f57b297230ddaff0172234d836831b`  
		Last Modified: Mon, 16 Sep 2024 18:57:17 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a344dcbd20d40e3d44fc7b14c0ac44fae3d71e95aa66e3d9bb754077bcca27`  
		Last Modified: Mon, 16 Sep 2024 18:57:17 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be846a8dff29772082ec14d333ad61991d8839c2af8d2164adeb2c5282ac0ce`  
		Last Modified: Mon, 16 Sep 2024 18:57:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:40487790b6f81d68918d39b932892debe6640fb8558998441de867ae8a3a823c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb2defe84891b3986f8195872e5d6f829274ea5f25f2d6a3fcaf2c8027fba00`

```dockerfile
```

-	Layers:
	-	`sha256:0dcb789456bc6cdfc540f5c05a8ed47e5ace91ebf0944b689366f2c48d26669b`  
		Last Modified: Mon, 16 Sep 2024 18:57:16 GMT  
		Size: 37.9 KB (37914 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:8f072c28a193d17c687b4858e7b2b60d5b70a84ff83d867eb8b80ab071a390f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62850077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5add3cf63918536d576e90dd84f0449fc3200a18f8ee30cb239bee956071fd07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.4
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-x86_64'; 			sha256='2eb8de746c0bc724bb5da4de52fc9660c2e866afc9a639ffdb1adfef2649cc0c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv6'; 			sha256='ad707af427c3d3574c9e7dbc77915dcd06779a58e2c3b3783f7781166213454e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv7'; 			sha256='bd473fb4fcdb6ff9d1616d7ff3294387a574298083de91a36eed2741341f3c97'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-aarch64'; 			sha256='d95d239bec166137a1ede1d441cb808da800dacc6041c966be35066aa96c6ee7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-ppc64le'; 			sha256='72d4359904b6821b04b77f7dac609b994847838d1d38e5840362d64dc35d9bff'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-riscv64'; 			sha256='34f859fd5b5d3f081a88004ad9a165b01f5b549abb76e0b99a3281bc963ebbde'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-s390x'; 			sha256='d4f333a3abb6f4904e75e56196a3e6671797ef2f5e09cfbe71263f2dad466ea0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 16 Sep 2024 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Sep 2024 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ccba012a8887fe20dd0d97354a55a0b8a43eb44692a096f1f6ba70ee50791b`  
		Last Modified: Mon, 09 Sep 2024 23:01:13 GMT  
		Size: 16.6 MB (16646018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefed47b60f47d2893fd6b2c20014cefa29c62ed324fefb4ab197def4e44b983`  
		Last Modified: Fri, 13 Sep 2024 18:56:51 GMT  
		Size: 17.1 MB (17145053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a0b13b079e2f3be21f85147817d1053c060975dc90466b09ea5a718312bf1`  
		Last Modified: Mon, 16 Sep 2024 18:57:20 GMT  
		Size: 17.9 MB (17882582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e30cec072c86205cc31ef24c71f3eb22a5fa542d27ab4744424af6da684d49`  
		Last Modified: Mon, 16 Sep 2024 18:57:20 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1758c31b0c62566f0e9a5698e94fbfaad06872b01d54f392f5c88588d57c0d`  
		Last Modified: Mon, 16 Sep 2024 18:57:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aa813f62ca8dbed64340f7e0b4eef0ee07447b6cb169136267c7226ee6ca2b`  
		Last Modified: Mon, 16 Sep 2024 18:57:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:236acc24d4b25ab554402d323799409b488172cd67d6101ec61f7ca5f3bc2ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37e313c955cfeff16987296ad8d353e2c7d2cdb6ca84cd036224af08b1f9f53`

```dockerfile
```

-	Layers:
	-	`sha256:ed0c194ec72e5a4724433ec472b44ebf272eadf5aaf85327eaa0869a0cd4cc1e`  
		Last Modified: Mon, 16 Sep 2024 18:57:19 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:18aeb8bdb6328df32a4b55108c95b34ed33748d8ec827abc5f2ea0b60e29d958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61880083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df554b4e51df066227c382f323387cc9880ed294be846c03e1219f452465a89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.4
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-x86_64'; 			sha256='2eb8de746c0bc724bb5da4de52fc9660c2e866afc9a639ffdb1adfef2649cc0c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv6'; 			sha256='ad707af427c3d3574c9e7dbc77915dcd06779a58e2c3b3783f7781166213454e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv7'; 			sha256='bd473fb4fcdb6ff9d1616d7ff3294387a574298083de91a36eed2741341f3c97'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-aarch64'; 			sha256='d95d239bec166137a1ede1d441cb808da800dacc6041c966be35066aa96c6ee7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-ppc64le'; 			sha256='72d4359904b6821b04b77f7dac609b994847838d1d38e5840362d64dc35d9bff'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-riscv64'; 			sha256='34f859fd5b5d3f081a88004ad9a165b01f5b549abb76e0b99a3281bc963ebbde'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-s390x'; 			sha256='d4f333a3abb6f4904e75e56196a3e6671797ef2f5e09cfbe71263f2dad466ea0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 16 Sep 2024 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Sep 2024 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca4111f91093de4178551363e4e5bb63c0285ef95fc3965527d7675d5b7be38`  
		Last Modified: Tue, 10 Sep 2024 00:48:37 GMT  
		Size: 16.6 MB (16633809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd394d391bedece8ee407ba342a5fe5c8bdbd24595743e9e33cad5fc27722d2`  
		Last Modified: Fri, 13 Sep 2024 18:56:40 GMT  
		Size: 17.1 MB (17135219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd2560b3f9c8876dc6252c3be05e2162898ae095e8ff8eeac9ff2e64909fac8`  
		Last Modified: Mon, 16 Sep 2024 18:57:32 GMT  
		Size: 17.9 MB (17869529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fed447528c1e926cebf15acdca2f603c6765579a2b6f20a3c5cb5dae0a56d9`  
		Last Modified: Mon, 16 Sep 2024 18:57:31 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ca32caaa383dbfb9743741989eb5fe541f1762bf48b380575d1d08496b0fcb`  
		Last Modified: Mon, 16 Sep 2024 18:57:31 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676bd3063078f78d473225414a8dbfbbb5d95c8392d689113ba3b5f9d6f05e5b`  
		Last Modified: Mon, 16 Sep 2024 18:57:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:de24d718a41fd2bec866b65b1b0024e6ca211ea41f8a57845349158c28f0e4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c260ecf137c45c0f41ca186db83f7a05a97d149cb153101258b516db34e9a12`

```dockerfile
```

-	Layers:
	-	`sha256:b9113d7ca43f5bdb0ad29c74988ed9af47e209a532b201f31c95a71c60aa4a57`  
		Last Modified: Mon, 16 Sep 2024 18:57:31 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:321619caa9b7fc8ba64b7de5d38e1bb2e20dbac7d4641ce589c74a55a116c89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63843449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7b52452b321ab98b50a1d12b35d5c5114e59478db8314065c27c69717f8c78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.4
# Mon, 16 Sep 2024 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-x86_64'; 			sha256='2eb8de746c0bc724bb5da4de52fc9660c2e866afc9a639ffdb1adfef2649cc0c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv6'; 			sha256='ad707af427c3d3574c9e7dbc77915dcd06779a58e2c3b3783f7781166213454e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv7'; 			sha256='bd473fb4fcdb6ff9d1616d7ff3294387a574298083de91a36eed2741341f3c97'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-aarch64'; 			sha256='d95d239bec166137a1ede1d441cb808da800dacc6041c966be35066aa96c6ee7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-ppc64le'; 			sha256='72d4359904b6821b04b77f7dac609b994847838d1d38e5840362d64dc35d9bff'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-riscv64'; 			sha256='34f859fd5b5d3f081a88004ad9a165b01f5b549abb76e0b99a3281bc963ebbde'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-s390x'; 			sha256='d4f333a3abb6f4904e75e56196a3e6671797ef2f5e09cfbe71263f2dad466ea0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 16 Sep 2024 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 16 Sep 2024 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Sep 2024 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d9fd5f156909c93f8bb558b3ad30308b845a01e16f4acde498ab920754f13a`  
		Last Modified: Fri, 13 Sep 2024 18:56:36 GMT  
		Size: 16.8 MB (16800785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40540d48c5c7e8f17d80bbcb893e550e8f11944431d68fb5a2f9f6777ed23b8`  
		Last Modified: Mon, 16 Sep 2024 18:57:12 GMT  
		Size: 17.4 MB (17414634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bcf936815f4c055cc1848a3b65c259bd6cf10f5e214baeed9ec73b54d28d25`  
		Last Modified: Mon, 16 Sep 2024 18:57:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff30aae6900ca7f69c8a3f8c80f2547b1d717e513fc60287245f9d7db46332c4`  
		Last Modified: Mon, 16 Sep 2024 18:57:11 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e2c247538881d517585c0a64cd8787893f366c84bab63c29d812472e810b5d`  
		Last Modified: Mon, 16 Sep 2024 18:57:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:8817c5d82768a4a7d802ad2f8ec47001b78a5dfb14af2ecafcfdb81ea682f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198033e92d615626f208683d8047ebaea33b0fba19331d4519a276bee7f4070d`

```dockerfile
```

-	Layers:
	-	`sha256:8fd0afd1b9e589b3d633afcd530dfc2c6a597eaaf909661302a146ab5582aaa9`  
		Last Modified: Mon, 16 Sep 2024 18:57:10 GMT  
		Size: 38.2 KB (38226 bytes)  
		MIME: application/vnd.in-toto+json

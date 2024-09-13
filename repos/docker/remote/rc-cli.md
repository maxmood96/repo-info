## `docker:rc-cli`

```console
$ docker pull docker@sha256:870618ae70e32e9046436dc07e10a6336ae23ba18ea11bec26c9028ca0f5a1da
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

### `docker:rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:509a647dd96c4bd5a66d49809eb5a44e7e3538d917dcc219870e11cb12daf407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67545949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273bfce0f5d19c54f8d32fbc659fbc07dd44a6bd4fea51e16624977429a27b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-x86_64'; 			sha256='241b75fe0f8194a48d01f99d683aa1100579b21caa60d2d78c9c824855c57937'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv6'; 			sha256='4abff57472ce971e84ccd6d09287da02515e99e1a2208e867c5d03123a1c406d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv7'; 			sha256='37fabd59e170943e12b4945a1a85c853e7db4759091f16036787fa02f6e2ec0a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-aarch64'; 			sha256='10ded2b3b02b15957b1650b99d1e5ff216d882c5203a563d0aa7a87580a0d8ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-ppc64le'; 			sha256='f8c63bcc8e8dca6703893c6fe909a10aef288bc347ee37922afc0099abf87946'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-riscv64'; 			sha256='9e51a8531b0db7f96b1ef8c9c27f104b4847c867af72056d3f7625b065cf9861'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-s390x'; 			sha256='3929a9d8a6a7a2521de7c2b148337f04dd360e30a2114a8200b123b398e97c35'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Sep 2024 16:59:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7708aa01b6f7e3eecfc6edf56ad1d100a0c1beca4ebb0d276611a9dace95c2a8`  
		Last Modified: Fri, 13 Sep 2024 18:56:29 GMT  
		Size: 7.9 MB (7880479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21e982418042b5628a4137c8363a7890e6b19a829c280bff9f6445a6dccaec2`  
		Last Modified: Fri, 13 Sep 2024 18:56:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c271021c2e3783e1cf076ef0e232c2689f4dc918a3d86975bed19a6425de2d5`  
		Last Modified: Fri, 13 Sep 2024 18:56:30 GMT  
		Size: 18.6 MB (18562804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c125e5b892d38c6e8cf747196b938c03b6fdfa691b9b435f6d33e7f8ceaf7245`  
		Last Modified: Fri, 13 Sep 2024 18:56:30 GMT  
		Size: 18.4 MB (18437712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a38ceb825ab4f2a3f0a03a17bc4eeecb5c9c5ee32738f9437e9ab51c04dc621`  
		Last Modified: Fri, 13 Sep 2024 18:56:30 GMT  
		Size: 19.0 MB (19038997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6a13aa581ced12f4cd200149e601c8e1ad874c62985d584e088f8609eab516`  
		Last Modified: Fri, 13 Sep 2024 18:56:30 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33268b31a641bc3b7a715e8fc468ad4064a4baf3296d729948d13a1b58fa374c`  
		Last Modified: Fri, 13 Sep 2024 18:56:31 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d234c71e8226d2c42f5942f297e2e4a37041f178b305e71ab0fe97e9e8825d`  
		Last Modified: Fri, 13 Sep 2024 18:56:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d26c2e241dd1df266739a3150ae99f981d9b9c8409044ebbbbdfabb746432a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc21a0bb3cc94fbf6ff5203d9d32db73928559499b83a2f185653a779e0c0e32`

```dockerfile
```

-	Layers:
	-	`sha256:31509177648367d27d96155d149e6587278c47f5bdcb6259b9c1e1a9fb36de92`  
		Last Modified: Fri, 13 Sep 2024 18:56:29 GMT  
		Size: 37.7 KB (37709 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:7cec5677cf1d421a2d4fc87191c4a3bccabf427a4a251cda88ab1c3deaf76722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62813830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd80755ccbb4336370e64f36f923b599efdf6dedc7b713a08f4fe336d698627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-x86_64'; 			sha256='241b75fe0f8194a48d01f99d683aa1100579b21caa60d2d78c9c824855c57937'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv6'; 			sha256='4abff57472ce971e84ccd6d09287da02515e99e1a2208e867c5d03123a1c406d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv7'; 			sha256='37fabd59e170943e12b4945a1a85c853e7db4759091f16036787fa02f6e2ec0a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-aarch64'; 			sha256='10ded2b3b02b15957b1650b99d1e5ff216d882c5203a563d0aa7a87580a0d8ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-ppc64le'; 			sha256='f8c63bcc8e8dca6703893c6fe909a10aef288bc347ee37922afc0099abf87946'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-riscv64'; 			sha256='9e51a8531b0db7f96b1ef8c9c27f104b4847c867af72056d3f7625b065cf9861'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-s390x'; 			sha256='3929a9d8a6a7a2521de7c2b148337f04dd360e30a2114a8200b123b398e97c35'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Sep 2024 16:59:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
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
	-	`sha256:37549dd8e6a6d0cdc996cc5449b22373bef199464d62afc97165e91bd4ce7194`  
		Last Modified: Fri, 13 Sep 2024 18:56:23 GMT  
		Size: 16.6 MB (16601245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecc51522c1dd8bec9e2a4dd04d57834bffc385d2118a77d5817edd2a634dbc5`  
		Last Modified: Fri, 13 Sep 2024 18:56:23 GMT  
		Size: 17.1 MB (17145035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ab83b8632853dba0f7781aa1a44cb98f0f489efa4263a2330a85cf22300e1`  
		Last Modified: Fri, 13 Sep 2024 18:56:24 GMT  
		Size: 17.9 MB (17891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2117e236c5946cfa586b1ecd5e102bb3f09fcc8f8445bd088c88358062ba35d8`  
		Last Modified: Fri, 13 Sep 2024 18:56:23 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1b721fac24b09109792893508589bafaebcf025f7a40daa95de370f4865afe`  
		Last Modified: Fri, 13 Sep 2024 18:56:23 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13a7951c6466716f0d29fcef3108d95384aca7f180fe82552429884e550b6e`  
		Last Modified: Fri, 13 Sep 2024 18:56:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1737bc949c83474554cd5c453751bfc11bff7b4c65fd6941536e723f53b2a6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea6108b8193b9f5fdcdce2c06f09bcb9a03a124c3f78bc6452f01866aff1297`

```dockerfile
```

-	Layers:
	-	`sha256:53e2955bf89b6e8b04b9b20d241b7757abccdfc331298c9078afe1a58b2ba617`  
		Last Modified: Fri, 13 Sep 2024 18:56:22 GMT  
		Size: 37.9 KB (37858 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:d636e7aef66325ea9dcdd45ca062bfc0e07b430a057fcb58f9308bafe0a66984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61840896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cf15bff6dc22d4b35a848cdaf40cae798f3bb1008bdd19dd0b1ceea6080a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-x86_64'; 			sha256='241b75fe0f8194a48d01f99d683aa1100579b21caa60d2d78c9c824855c57937'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv6'; 			sha256='4abff57472ce971e84ccd6d09287da02515e99e1a2208e867c5d03123a1c406d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-armv7'; 			sha256='37fabd59e170943e12b4945a1a85c853e7db4759091f16036787fa02f6e2ec0a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-aarch64'; 			sha256='10ded2b3b02b15957b1650b99d1e5ff216d882c5203a563d0aa7a87580a0d8ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-ppc64le'; 			sha256='f8c63bcc8e8dca6703893c6fe909a10aef288bc347ee37922afc0099abf87946'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-riscv64'; 			sha256='9e51a8531b0db7f96b1ef8c9c27f104b4847c867af72056d3f7625b065cf9861'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-linux-s390x'; 			sha256='3929a9d8a6a7a2521de7c2b148337f04dd360e30a2114a8200b123b398e97c35'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Sep 2024 16:59:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
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
	-	`sha256:242d3ee078c98df2b09361b18c3ef358e4394cd924061652a17793b08ddaae6a`  
		Last Modified: Fri, 13 Sep 2024 18:56:13 GMT  
		Size: 16.6 MB (16590994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db63cdca03f9525b3158778ada4971fca8f6fe02a5fcfc1b97ce3f0b93662f09`  
		Last Modified: Fri, 13 Sep 2024 18:56:12 GMT  
		Size: 17.1 MB (17135230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9957d68eaa170ddad5d88dc3bf27d79bb147b0e49af4b9f617c803a0267f9ea1`  
		Last Modified: Fri, 13 Sep 2024 18:56:12 GMT  
		Size: 17.9 MB (17873154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9011740efcd365fa8ba0eb717ba563b19b7d57ce48b4df4575e5de12b14b28c7`  
		Last Modified: Fri, 13 Sep 2024 18:56:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcb76c009fdefd70c50ad43acdbe22a5de2509387e16e8a35899b8c0189f7d9`  
		Last Modified: Fri, 13 Sep 2024 18:56:12 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35f2717de70a6e55035d1ed7ee8a471d30f97f7fb852ede7136cbc53bc47ff1`  
		Last Modified: Fri, 13 Sep 2024 18:56:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b73529fd3e40c2c461fbdb798b1e279063937ab804627b0611b283d7f7d5eaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d05db7c63d3fd91861dd08093d96eb449cbc822a706e973550d2e99c06a5be`

```dockerfile
```

-	Layers:
	-	`sha256:2a6f8c32d0e217d7bbef3ad9f38090a61bf814ebdc102301acdd11d183e16d43`  
		Last Modified: Fri, 13 Sep 2024 18:56:11 GMT  
		Size: 37.9 KB (37858 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a7395aa6fab4c1a24a3a192e9ee84f842a5eaa49b560097db8db29d754ad77ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63295507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de6eae0ce59d5abca4886b66f9daa4c16e192f19ddabebb9bceaa4f2d0be73b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_VERSION=27.2.0-rc.1
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 17 Aug 2024 05:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19dc33df4c8f435b82bd76228e820d17db82bafa51365d6d7ca39f18b0ac35`  
		Last Modified: Mon, 19 Aug 2024 18:59:40 GMT  
		Size: 8.0 MB (7981766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc98e249bb1c68fcd6c7af4cd94d4dc840949342f303f3453b89e47b10baac`  
		Last Modified: Mon, 19 Aug 2024 18:59:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b064ad1c39cab9bbd12ce8a44da8ca317ae42aafc3a703eb68481279fac32d9`  
		Last Modified: Mon, 19 Aug 2024 18:59:40 GMT  
		Size: 17.3 MB (17264856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36074db9005cb79314791a9d04733048d5cb0703a7ac13b89c26d810045b89d`  
		Last Modified: Mon, 19 Aug 2024 18:59:40 GMT  
		Size: 16.8 MB (16772961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb8b806a016e2bd5e83e137c7787981575ad2ce863d92ce07cee3fc38544c78`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764856852ab1b254b572502db9ed0d8fd601e8e615ae83ba73c5a1e5b592c9ab`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d43f3808e72acbc083572802b4b53a88aa4088c8e2d99825cef40e03c050fd`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12ab67b46ae8edc30d74e102545f60cf7042a2542f02c2b8e7f0a313592f473`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e10f2c6fd467d145de4d4a14fa8ca75a1ee80fe11c0d42eb6e323b5f743df97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fd9030e8a86dd7741b31e53d376214fbd782a1e59b457e75334c2d9aab2c46`

```dockerfile
```

-	Layers:
	-	`sha256:17b7467f3e146fec54cae7f008e9cf996f4c6289eb67a6ed6f3507501ea67e9f`  
		Last Modified: Mon, 19 Aug 2024 18:59:39 GMT  
		Size: 38.0 KB (38010 bytes)  
		MIME: application/vnd.in-toto+json

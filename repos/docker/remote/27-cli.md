## `docker:27-cli`

```console
$ docker pull docker@sha256:c4fad57b6d65c729d2f49717f161ecf57cca76f2d9e449b5adbfe46fb6ed5d5f
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

### `docker:27-cli` - linux; amd64

```console
$ docker pull docker@sha256:7b748c454a63897098b920984ceb577d41b7862310eef5a5925d8eaefa85a0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67573189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8beb79be8ff10d4ff54dd95a0dd5ad5ef418544263bc0caa743be6f56d10da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 11:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 17 Sep 2024 11:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 17 Sep 2024 11:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 17 Sep 2024 11:04:23 GMT
ENV DOCKER_VERSION=27.2.1
# Tue, 17 Sep 2024 11:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 17 Sep 2024 11:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 17 Sep 2024 11:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 17 Sep 2024 11:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Tue, 17 Sep 2024 11:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-x86_64'; 			sha256='589f98f1395936170815282d77dbcb9935210536c769778aedd09c4ff5eec33b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv6'; 			sha256='3484cca874ef8eac4a81a020acbf8380dd9fa6176a1162a2591a42dd26d3d182'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv7'; 			sha256='03848bfe15f37fb078d6ad6f63183de985c837791e472b4e15e5768ab29ca84b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-aarch64'; 			sha256='1301f1e1d94e9f03f39448c1bff5b14238770438f5c698e09ffaa7fad9969901'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-ppc64le'; 			sha256='756103706b378948e989d8aa7e4694a9d8691aabd73019064b57ad4315f6388a'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-riscv64'; 			sha256='6dca0ca98fdcbfbbf26318bf74bb7faf8f221201370f059c83dc554fe08fce23'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-s390x'; 			sha256='6a43ae85495ceaa1b41f8958c1677ce0e25991f96b3bc47107f4af0e4db8927d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 17 Sep 2024 11:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 17 Sep 2024 11:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 11:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 17 Sep 2024 11:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 17 Sep 2024 11:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Sep 2024 11:04:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aefe493c2a4cd2e05feb94b216485333a3d3bba4ccca999ed33d54bea773724`  
		Last Modified: Tue, 17 Sep 2024 22:58:18 GMT  
		Size: 7.9 MB (7872491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f20aed1c0c2bf5dc76f977b195b56c400abcdb9a0007526e12d6362b1f0a49`  
		Last Modified: Tue, 17 Sep 2024 22:58:18 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc9768510de7f1f811a3f110d65fbe905d4580ed9031f99da3eca0991699f1c`  
		Last Modified: Tue, 17 Sep 2024 22:58:18 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d511c2ec4788aa79c04cc3e5aadd876b1c818348358b84b5d6dc13464a6df1`  
		Last Modified: Tue, 17 Sep 2024 22:58:18 GMT  
		Size: 18.4 MB (18437732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d866e42ce49d685afce9b56bc53b3df49ad4c8c9181e0618c00c447c86a6d10`  
		Last Modified: Tue, 17 Sep 2024 22:58:19 GMT  
		Size: 19.0 MB (19035831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f9e1403c39fcb84e71b901e18ba9eefd7c7d24cd96aa0ddd6fbdecf4ecf5c2`  
		Last Modified: Tue, 17 Sep 2024 22:58:19 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fb32a965e63526ae6c840d9b225a95df79b803e5df15665f5f288e11f27871`  
		Last Modified: Tue, 17 Sep 2024 22:58:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb4a4a11a2d339795e030511f4ecd2fcfcdd1c1e8af0f9c6109f43d17a398bc`  
		Last Modified: Tue, 17 Sep 2024 22:58:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6b35d4034e2f5e85556c56c1efd3da3670f1adcda91501713a4627d822f05aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b64a8194652e8a15756690d2ddab6ee5841bb50b79965155787e1859de0afa`

```dockerfile
```

-	Layers:
	-	`sha256:777b1f2a19bfa64c74e333ef89255274eba3f769cc6e2643f0258f735ce5e45a`  
		Last Modified: Tue, 17 Sep 2024 22:58:18 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b37f27c773213521f3b9f50b1bea66893bff8cfdeb6b32ef4c0e848a030a187e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62807970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba098cb71ad32dd006eb0a19187914173eb33de03b198b5fde798eed92a6bc58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
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
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8d75f23a7f71e324101f62e4910ebcd382df1e5b1de7c681a6e4cb6cdb51239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d022f57c2745434cdb5a16d53bf882cfff444c2dfa89bae5a7ed046edeff0c`

```dockerfile
```

-	Layers:
	-	`sha256:230a88f840c3aac47eed4236aa13bb6a08174da6a6206d828702c6e3e539e66b`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:92cd3b7461e08430c9c8b0ed5d4901e0488e284933a85054fda8f8f8023c7f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61841889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c204650295cc9e25dec97762b7a1e329f9096943adb717615dd050b04da93e17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
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
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d05c59320fc8170b965528a28318d76cc3f86132d619ad1abef819b8874a14eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c78e41f7a9e5cff872b1477eb6418d9b44458efb85786cae50dc1b0c591c6eb`

```dockerfile
```

-	Layers:
	-	`sha256:1c05414271ca6215055155152eac69a122f18be18f74b0bb6ca2501c28e886e5`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86b728ef94ed08000296013516632982f9045b3a267320f45f788a1d87837222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63797168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ebacfdc77c1349a11d7396eb11de6e948d8520bb119e3b6d013965e73739e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:64b5880805081e227f6d4a927b96888d67d4a31c3f9b4b8b266dff874ed5476e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9bcf782079c0ad78e0609c8b6af69b3ed5cef3331845bbf72ad615cb3eb46f`

```dockerfile
```

-	Layers:
	-	`sha256:06b348c580d845a356c7f2c8bb62a6c60ea047e84244306dd8cf0189fe150536`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 38.2 KB (38225 bytes)  
		MIME: application/vnd.in-toto+json

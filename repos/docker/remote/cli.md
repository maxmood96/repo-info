## `docker:cli`

```console
$ docker pull docker@sha256:235a25499afa28f3c359b4a90d4245fc74d21f2f368cfb7bbc48aca1e189609d
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

### `docker:cli` - unknown; unknown

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

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:080c2362b79f5d44b3c8634c19b962fc77815ff286085a791599afcaeb052516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62850468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97438d750e356e8a8891f86804de965f15e8e24104e96e971e0c19fda226bf97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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
	-	`sha256:8fbf3613d5eee080054db9b24b3b03baac2f5e6e91781676dc1b1ea4b21a2b02`  
		Last Modified: Tue, 17 Sep 2024 22:59:40 GMT  
		Size: 17.9 MB (17882976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e0f7fd850197fa5321ce8852a4691854c7133d95b6d38985f698345318a20d`  
		Last Modified: Tue, 17 Sep 2024 22:59:39 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9831c095c63fac28cc42901051a93afbdddbd953f0f2842467191f35d6f0cf`  
		Last Modified: Tue, 17 Sep 2024 22:59:39 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194f4a81b2f6e4ac5a8468f3d5cb11a13ef36c0cc532dab076d4f4a21d167c51`  
		Last Modified: Tue, 17 Sep 2024 22:59:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:b0b9676795aed738525009c9ef8336695bc42bd4d50085ea45f1b9a3ff28ed65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424832997f33a6207c036e5396b2f17d43f805ba48b694bf23fd47f8430161cc`

```dockerfile
```

-	Layers:
	-	`sha256:fe4e7781c11ffb4604fb5a227491540a9fa13d33a6e7ff031d12b127e92ba557`  
		Last Modified: Tue, 17 Sep 2024 22:59:39 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:92489caff321842a6a0b736560a1af7a2339fab73f426da6d18bb86b16bf08a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61880608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b74c27a57c062f45c1ccd497ffd2242f6275af815e76ccb52290b722734e3f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
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
	-	`sha256:6cfbb6ee913a54fc7aa99bcd10899b3cb10048d163d29b976ffa15b600eb0bb2`  
		Last Modified: Tue, 17 Sep 2024 22:59:32 GMT  
		Size: 17.9 MB (17870056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4344a96ad10461ab1001e378986cd61235404780b30cfac6a536777130accb44`  
		Last Modified: Tue, 17 Sep 2024 22:59:31 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfca5afccf5689a9b7f7bed04e2d2ada28348111aba4d0bd896632b570ef0aa6`  
		Last Modified: Tue, 17 Sep 2024 22:59:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec723e3245e7f6915c65b87a5d86dda5217bcb0be50feaf86a31e5edaee8fef9`  
		Last Modified: Tue, 17 Sep 2024 22:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4f02453074da1dfdc7c5fd0198ab114229a957a2c5981c9b47c159e289289fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0e225ef82307b31c2c0f10178a80aee22a94d4f8cd11c233131ea4a566c111`

```dockerfile
```

-	Layers:
	-	`sha256:715a1675d3a7dd6b7691e0ecd50929e84df68b0a3f61b85527eb68275613eb5e`  
		Last Modified: Tue, 17 Sep 2024 22:59:31 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b9a7fe8a57ae759c0c164292b04e769d857bc47c3183da0228c052d6a37d6741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63842616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da7547a63942104670aa8843320848e4efeafad6bf2b255f64aebc208344432`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90c77b2dd2fbc19109b7e5173bd83f913522d220b61397c929fbf4b20d0139a`  
		Last Modified: Tue, 17 Sep 2024 22:59:04 GMT  
		Size: 8.0 MB (7981910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fcb907d3b4916cccfc979f994c41efc1a1c74c2c83902e2e97216ca9ee39a`  
		Last Modified: Tue, 17 Sep 2024 22:59:03 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03f564e79a0eeb4378c215a832bfa4833f11010c01fa268227be2954d365de`  
		Last Modified: Tue, 17 Sep 2024 22:59:32 GMT  
		Size: 17.6 MB (17556290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1ea95445ed4d3fd36efa4fd277d9f485e35cfcc36dabab3ae525118479ae56`  
		Last Modified: Tue, 17 Sep 2024 22:59:32 GMT  
		Size: 16.8 MB (16800775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1d1b0cddd3ee53eb30cce47265d2260efcb40b713041d0b9df55d5d5d86613`  
		Last Modified: Tue, 17 Sep 2024 22:59:32 GMT  
		Size: 17.4 MB (17413842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9144b5c5900114e8de0fcca509d639bf955696d9c6f9dbadf6d48ad65dee22`  
		Last Modified: Tue, 17 Sep 2024 22:59:31 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce15d7db8d634bbc89f5223f77d2ee8f913a20b2194d7bfe70ec0f86d78ff1a`  
		Last Modified: Tue, 17 Sep 2024 22:59:32 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cbed250d61fa1b7098661ca291748befb35368c6e06290169afa48e2adbe8b`  
		Last Modified: Tue, 17 Sep 2024 22:59:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:b4a7a3b765d8498774c7a66cdb05d4f44da57f89b2eeba147bd923d974701934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa296be34fa5ac59f3ea4dcd6028817f5b0886fe17546f5ba82871b633fa4f2`

```dockerfile
```

-	Layers:
	-	`sha256:2aadc9748b7fb8715f4f8d4a1e73894bb07ae7bc66530dd90cc4249d24c848c3`  
		Last Modified: Tue, 17 Sep 2024 22:59:31 GMT  
		Size: 38.2 KB (38227 bytes)  
		MIME: application/vnd.in-toto+json

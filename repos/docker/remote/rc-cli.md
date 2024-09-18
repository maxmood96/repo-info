## `docker:rc-cli`

```console
$ docker pull docker@sha256:1dba9f440ba7b91ef68b2ef5b3107bac55b5f1e086774891058eae166a1c6269
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
$ docker pull docker@sha256:47f3f2a019aa5dbab2d1922dedef3e73e87944ddeedeae7880f12b2f209b4341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67534909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4f33ff411f6b15b0473f16e41b7a4b4d71c3e3ea380e22c2755f8f52eecf8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 11:05:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-x86_64'; 			sha256='589f98f1395936170815282d77dbcb9935210536c769778aedd09c4ff5eec33b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv6'; 			sha256='3484cca874ef8eac4a81a020acbf8380dd9fa6176a1162a2591a42dd26d3d182'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv7'; 			sha256='03848bfe15f37fb078d6ad6f63183de985c837791e472b4e15e5768ab29ca84b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-aarch64'; 			sha256='1301f1e1d94e9f03f39448c1bff5b14238770438f5c698e09ffaa7fad9969901'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-ppc64le'; 			sha256='756103706b378948e989d8aa7e4694a9d8691aabd73019064b57ad4315f6388a'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-riscv64'; 			sha256='6dca0ca98fdcbfbbf26318bf74bb7faf8f221201370f059c83dc554fe08fce23'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-s390x'; 			sha256='6a43ae85495ceaa1b41f8958c1677ce0e25991f96b3bc47107f4af0e4db8927d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 17 Sep 2024 11:05:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Sep 2024 11:05:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a9a4043057cd831fa8d4bd19ada174e1d9931be2d09c6293f4bc0c0def1d0`  
		Last Modified: Tue, 17 Sep 2024 22:58:24 GMT  
		Size: 7.9 MB (7872602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09cec39a59857be871d28c3244c84b5495367d43391d20f3631cda3af248e7`  
		Last Modified: Tue, 17 Sep 2024 22:58:23 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4379cf75127356e95e364c696338928b209624d6e2bd9da0b841256e440ea1fb`  
		Last Modified: Tue, 17 Sep 2024 22:58:24 GMT  
		Size: 18.6 MB (18562808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a337023da1ab84f55d473a30c415372f7879717ad91c3c199301f26b8b24ded4`  
		Last Modified: Tue, 17 Sep 2024 22:58:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0ba583cf6af200de2d27691a75f1b7f60edd585142813ce01fb8232dc8c2fa`  
		Last Modified: Tue, 17 Sep 2024 22:58:25 GMT  
		Size: 19.0 MB (19035822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea8048705b3f0a9e17bcd1c995d9b5176b2bc42f708b77762b35817dac49212`  
		Last Modified: Tue, 17 Sep 2024 22:58:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8de27f42311b4f12a9a51f3632c60ade33b80cdc17806f7995f3110b0c346a`  
		Last Modified: Tue, 17 Sep 2024 22:58:25 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f69bae79d73c3fb37255bbe3cde3e0086190373649f7dc9a34df701025dda8f`  
		Last Modified: Tue, 17 Sep 2024 22:58:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:45e2746b5f995b8f00dad7e0bd34deed9e3329d2171fde73ee36f8cd5f86cda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7e6d4e767419e4771331e1b12eb48ae0295047b7dedbb8d60f653e345ee398`

```dockerfile
```

-	Layers:
	-	`sha256:3d3235a741896489d093b3e2e04e77e698d85b4c2a8536edfa3afd0c947bc9a2`  
		Last Modified: Tue, 17 Sep 2024 22:58:23 GMT  
		Size: 37.7 KB (37710 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:671dd81a78552f4e75d91ac5a53484f8c6dd5d9858caf4814fc6c04a8437f3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62805666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02e5a55318906e80f1511b2de1209597d59bf5983d7774b11548302905213b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 11:05:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-x86_64'; 			sha256='589f98f1395936170815282d77dbcb9935210536c769778aedd09c4ff5eec33b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv6'; 			sha256='3484cca874ef8eac4a81a020acbf8380dd9fa6176a1162a2591a42dd26d3d182'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv7'; 			sha256='03848bfe15f37fb078d6ad6f63183de985c837791e472b4e15e5768ab29ca84b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-aarch64'; 			sha256='1301f1e1d94e9f03f39448c1bff5b14238770438f5c698e09ffaa7fad9969901'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-ppc64le'; 			sha256='756103706b378948e989d8aa7e4694a9d8691aabd73019064b57ad4315f6388a'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-riscv64'; 			sha256='6dca0ca98fdcbfbbf26318bf74bb7faf8f221201370f059c83dc554fe08fce23'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-s390x'; 			sha256='6a43ae85495ceaa1b41f8958c1677ce0e25991f96b3bc47107f4af0e4db8927d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 17 Sep 2024 11:05:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Sep 2024 11:05:55 GMT
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
	-	`sha256:cfee6bd9a89cf12af993b9208567d64d346227980977cee41b3846efbbf9c7b4`  
		Last Modified: Tue, 17 Sep 2024 22:59:18 GMT  
		Size: 17.9 MB (17882965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7f5c6b6827edd9b83ffc5d16b3ef8d1a13fb95cfff527748986b9d6f48e89`  
		Last Modified: Tue, 17 Sep 2024 22:59:17 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49963f21eb6cf5ccfc376a260a74354d1b67aed9eafc88449fbbd56d7dc6c6a5`  
		Last Modified: Tue, 17 Sep 2024 22:59:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5842bc8a9717d4f70b167bcfb6c86ecc93103e26c85a8af603963978bb1c8209`  
		Last Modified: Tue, 17 Sep 2024 22:59:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9f8e061e6d60cbe1e4e42cd71271702b8797614fc54be5efa0f7b15bfec9c5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28999d3b557889993ff35f20d001be63b590565120a65f35cd7100153e39718`

```dockerfile
```

-	Layers:
	-	`sha256:b3fb13984bec8eeb9081a738af7391fc9499bae063a89f317bba3a6610a2b1cb`  
		Last Modified: Tue, 17 Sep 2024 22:59:17 GMT  
		Size: 37.9 KB (37857 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:18147dd68d2b2fcdb158e07851c6e64c4ce83ab6a2caef321262aaa1af3be99f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61837816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acaf029e2578f1115e46c89528afe38d11fd94e2cfadb87a83fc8eb5c724633`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 11:05:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-x86_64'; 			sha256='589f98f1395936170815282d77dbcb9935210536c769778aedd09c4ff5eec33b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv6'; 			sha256='3484cca874ef8eac4a81a020acbf8380dd9fa6176a1162a2591a42dd26d3d182'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv7'; 			sha256='03848bfe15f37fb078d6ad6f63183de985c837791e472b4e15e5768ab29ca84b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-aarch64'; 			sha256='1301f1e1d94e9f03f39448c1bff5b14238770438f5c698e09ffaa7fad9969901'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-ppc64le'; 			sha256='756103706b378948e989d8aa7e4694a9d8691aabd73019064b57ad4315f6388a'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-riscv64'; 			sha256='6dca0ca98fdcbfbbf26318bf74bb7faf8f221201370f059c83dc554fe08fce23'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-s390x'; 			sha256='6a43ae85495ceaa1b41f8958c1677ce0e25991f96b3bc47107f4af0e4db8927d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 17 Sep 2024 11:05:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Sep 2024 11:05:55 GMT
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
	-	`sha256:91d7f3c2892dba0be760f8ad3f025c6349fa24026d86d1fbd4bbf1836000b160`  
		Last Modified: Tue, 17 Sep 2024 22:59:10 GMT  
		Size: 17.9 MB (17870070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa2efe9778f03b506b3a7670f3f7a7be968795fcc3bb0a435a1635cecacb713`  
		Last Modified: Tue, 17 Sep 2024 22:59:09 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d06f0e54ec2715144e564987b855a7da1cbe39fada182cec5cca1cec87fbf4`  
		Last Modified: Tue, 17 Sep 2024 22:59:09 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974f85df93f93a17de883775b65688e870ff3ff15a9114659b6a526c15d7b955`  
		Last Modified: Tue, 17 Sep 2024 22:59:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d076b11ba3a702e041c7108ff58ec2a327261a986edb9b66c8b7a0c17b5c67a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71f955ded726b7d9253438c69bf967f30036b91703b525b65fff724a91a99b8`

```dockerfile
```

-	Layers:
	-	`sha256:d2e21911790cd4d61db39dee635bbb695e393ed8425e6c728a4c3dd63da22abb`  
		Last Modified: Tue, 17 Sep 2024 22:59:09 GMT  
		Size: 37.9 KB (37858 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:670ef8100383337ab57e33f8b2f26c1ecc315f318f25ffc65c95c1d953953cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63802242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0b3d03cd77934afe70c35101134fe8df716b6bd4d721685310f6af4daa3855`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 11:05:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Tue, 17 Sep 2024 11:05:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-x86_64'; 			sha256='589f98f1395936170815282d77dbcb9935210536c769778aedd09c4ff5eec33b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv6'; 			sha256='3484cca874ef8eac4a81a020acbf8380dd9fa6176a1162a2591a42dd26d3d182'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-armv7'; 			sha256='03848bfe15f37fb078d6ad6f63183de985c837791e472b4e15e5768ab29ca84b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-aarch64'; 			sha256='1301f1e1d94e9f03f39448c1bff5b14238770438f5c698e09ffaa7fad9969901'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-ppc64le'; 			sha256='756103706b378948e989d8aa7e4694a9d8691aabd73019064b57ad4315f6388a'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-riscv64'; 			sha256='6dca0ca98fdcbfbbf26318bf74bb7faf8f221201370f059c83dc554fe08fce23'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-linux-s390x'; 			sha256='6a43ae85495ceaa1b41f8958c1677ce0e25991f96b3bc47107f4af0e4db8927d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 17 Sep 2024 11:05:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 17 Sep 2024 11:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Sep 2024 11:05:55 GMT
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
	-	`sha256:68050de4c3c5ce0df3f47a970cd043cb32459b7941b24adabbf13a092029155a`  
		Last Modified: Tue, 17 Sep 2024 22:59:04 GMT  
		Size: 17.5 MB (17515919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ae9d4021b4e1ce7fac21d3c27e20e859ec812bd8efdc36e04b6d4ec243545f`  
		Last Modified: Tue, 17 Sep 2024 22:59:04 GMT  
		Size: 16.8 MB (16800778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186a5abd6f117d4c14ebcaf3a896f510d40c057879eb87b2f1b6ce0f276a81a3`  
		Last Modified: Tue, 17 Sep 2024 22:59:05 GMT  
		Size: 17.4 MB (17413836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc5378f1d58dc07a9b6fef86858db1b98556ce4fee55eb7c9bb6843eb3aea7`  
		Last Modified: Tue, 17 Sep 2024 22:59:05 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0586909b8b50aaf12a7e50707147de78515433fac2085b843ccee244ec0b5978`  
		Last Modified: Tue, 17 Sep 2024 22:59:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca70de52cb3f32b56b20d0ee51b41d159021c79e3e2a30a21d23603afaccf14`  
		Last Modified: Tue, 17 Sep 2024 22:59:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5e55d31455c214e25dc85f5102445a969ba1a35a7279296298c72f8603b5e40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff3c263c445797938d6c5b4f60ec633b1e2f2dd37e0c92c71bdebb58f850923`

```dockerfile
```

-	Layers:
	-	`sha256:09594cfc9a36df343b0d45544247135f8050fb85b304b7c06fa24ffca85f3c49`  
		Last Modified: Tue, 17 Sep 2024 22:59:03 GMT  
		Size: 38.0 KB (38010 bytes)  
		MIME: application/vnd.in-toto+json

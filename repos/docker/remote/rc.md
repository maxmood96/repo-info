## `docker:rc`

```console
$ docker pull docker@sha256:8ff7e2767d4cd6bb46ec1c2ad69709b8b2e1470df16acfc3ea5e826925974d7b
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

### `docker:rc` - linux; amd64

```console
$ docker pull docker@sha256:efd53f98acc9b0d18d0dca8528ce0bf92d19816f0ce939c3ad6419faa8c332f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132095708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc85c3fa11c6dc8098a087252a6c7224ddb39524c37c14773cdd624f2769061d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

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
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
VOLUME [/var/lib/docker]
# Fri, 13 Sep 2024 16:59:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 13 Sep 2024 16:59:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
CMD []
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
	-	`sha256:aaf0cb4fa03f3ac4d9674d4312312f612b086983069c981c6b6c2b3ffc36c214`  
		Last Modified: Fri, 13 Sep 2024 19:49:18 GMT  
		Size: 6.7 MB (6657929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279c641c239b0f532e63f8d642856de8239859bb36ac0dfb90cc28d6fadc8907`  
		Last Modified: Fri, 13 Sep 2024 19:49:18 GMT  
		Size: 89.2 KB (89209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8c42fa88383b26f8fdd662974b6b552283cfdc17260c422d4169e692d9b197`  
		Last Modified: Fri, 13 Sep 2024 19:49:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cd6da411f2025fcb0b9575bf91fa6e24999a619d2fb73ae6c649e9bfc15e7f`  
		Last Modified: Fri, 13 Sep 2024 19:49:20 GMT  
		Size: 57.8 MB (57796830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6d8293aad5678208fbdbf1423c4b4909218a28400e3c464fa46e15c45e7ecc`  
		Last Modified: Fri, 13 Sep 2024 19:49:19 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a07ab7807ab6508ed0f0a56feb479b165828d6694c17dab0298ebea483c485`  
		Last Modified: Fri, 13 Sep 2024 19:49:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:372d44ddf9093f65587ba2a87a5c08fa287ecc08ab997b21bc8c92ce7f7e5773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (34041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a39c1f1035693ceb12d101842faa869bc898026157ac7f6a2347d5a63080415`

```dockerfile
```

-	Layers:
	-	`sha256:a88d24cdcac1a8b23ebb02fc86f36bf3e969be802e12a2d2ff8a144b8a81d475`  
		Last Modified: Fri, 13 Sep 2024 19:49:17 GMT  
		Size: 34.0 KB (34041 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm variant v6

```console
$ docker pull docker@sha256:4cf2abbd54e857a6351110ce41019175e297b710e396bc555f370a213cfd5dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123403621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64d06ead4aaf0602b37f3f5f3f824e7fe2178f887949765481fb4ceda379375`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

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
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
VOLUME [/var/lib/docker]
# Fri, 13 Sep 2024 16:59:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 13 Sep 2024 16:59:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
CMD []
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
	-	`sha256:efffdcd359048ad768ec15048c8bd1182c12063d3fc80c9d04b253b1318ccc8a`  
		Last Modified: Fri, 13 Sep 2024 19:49:13 GMT  
		Size: 7.0 MB (6984261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b530771a5b3241763e2dcdfed34b3d32ff2664a42c10b89e2e3a5d5cf2affdd`  
		Last Modified: Fri, 13 Sep 2024 19:49:13 GMT  
		Size: 88.4 KB (88395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea05cd0de206e3d1c12a07f0ad2c86f2fbdd6d4e864f29b065aba245482d1ab`  
		Last Modified: Fri, 13 Sep 2024 19:49:13 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6b20e58c8db85e773d3698be7ae010482cca2e8136d8a4cafe42becc767112`  
		Last Modified: Fri, 13 Sep 2024 19:49:15 GMT  
		Size: 53.5 MB (53511334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76c763e4d235f7856b1b316e727361454d802126b66d5bfa9ef70bcfa990fcf`  
		Last Modified: Fri, 13 Sep 2024 19:49:14 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6784e9d616a33eccc9212443a68c33276a628c2f8844c98e4b7ddb98b920454`  
		Last Modified: Fri, 13 Sep 2024 19:49:14 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:5f2f6129c9c61c3cf051db5ab6eae8137715e312ee59a34a2fbff957c0abc1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c14e7865d9ed528ea733f8d9f5b8c2c36ca6976d3390b77a354ab0b9a93eae4`

```dockerfile
```

-	Layers:
	-	`sha256:4806b4e0440b87c3edd35ab6f36b294993caf1c860eda27f9551bf2a20533dd3`  
		Last Modified: Fri, 13 Sep 2024 19:49:12 GMT  
		Size: 34.2 KB (34243 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm variant v7

```console
$ docker pull docker@sha256:09c710c1c09af4b33d51f1ec7a94c701f0675800b9d0a8467d5c104f7f4e5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121750632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bd2e994947c3769d5c3abb7c273ca0642b8473e2f36ef69981b4b1a0ce4c7b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

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
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
VOLUME [/var/lib/docker]
# Fri, 13 Sep 2024 16:59:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 13 Sep 2024 16:59:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
CMD []
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
	-	`sha256:3d16854e642792dc7476555f7ea220f931f06bed1174bfa9539a6f283d2bb805`  
		Last Modified: Fri, 13 Sep 2024 19:49:13 GMT  
		Size: 6.3 MB (6308109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b364e09468df64830e497d3bdb4e12c4d997fe9e5db5b28446ce2037a941fd0`  
		Last Modified: Fri, 13 Sep 2024 19:49:12 GMT  
		Size: 84.5 KB (84482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a993b1635934610eff0b243ff637f9645860f3d5d2737d34a9b9608942cd30`  
		Last Modified: Fri, 13 Sep 2024 19:49:12 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152bac037edd6ebc296d0ff4a3be3d31bbeadc5e1508134230a8ac59b8f91c2d`  
		Last Modified: Fri, 13 Sep 2024 19:49:14 GMT  
		Size: 53.5 MB (53511346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc819d16155ce71321e755421fa8ed8dbfee88be66ed5cf803cf0899ae41faa`  
		Last Modified: Fri, 13 Sep 2024 19:49:13 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b0f3e1299dc1d11908661db64a963a2892de625dd0f7640477783bbc44bd4`  
		Last Modified: Fri, 13 Sep 2024 19:49:13 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:1cad11af758618069880b8d6f41e0b3ef3657e4eb6bab3def5e7c76deb26f0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794a7eef45ae791187d542eb1d696b8d8abc461c3c60bf33b74d0f7e74473992`

```dockerfile
```

-	Layers:
	-	`sha256:275223863b9e5cd5e557d83225fbbe1b1e146f33a86ba2417acb4b34eb5dab44`  
		Last Modified: Fri, 13 Sep 2024 19:49:12 GMT  
		Size: 34.2 KB (34243 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7723213ae2829f2f478f3a574626536b113feae6cc973f9b3167194640ced2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124362913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83935be5befda3c2d0eee20c55f9f816e055bb2002c8ecafa45573844d077e1a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
VOLUME [/var/lib/docker]
# Fri, 13 Sep 2024 16:59:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 13 Sep 2024 16:59:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
CMD []
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
	-	`sha256:df7ab6a65b5548b28c6ea479b5fa1d0e59628b777830db0afcafd60fb3ea2a24`  
		Last Modified: Fri, 13 Sep 2024 18:56:10 GMT  
		Size: 17.5 MB (17515930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e4860376f01b29ad074f91764ce3a106a4766d66e3c0a722484baa53bd66bb`  
		Last Modified: Fri, 13 Sep 2024 18:56:10 GMT  
		Size: 16.8 MB (16800754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f4e9db94d78707f83eb396a6c1c000e15e675c1b328f9d6e06aa760e8861f6`  
		Last Modified: Fri, 13 Sep 2024 18:56:10 GMT  
		Size: 17.4 MB (17409488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1c5216b408f612b6b7149d0044d644dde8b835925363f6c200c36efe85307a`  
		Last Modified: Fri, 13 Sep 2024 18:56:09 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f679287902c966cc05d2e5e08f6980b44875dfedd8fd630483eb3aa410764f`  
		Last Modified: Fri, 13 Sep 2024 18:56:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35f2717de70a6e55035d1ed7ee8a471d30f97f7fb852ede7136cbc53bc47ff1`  
		Last Modified: Fri, 13 Sep 2024 18:56:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23fd98f27d70d97e6d2df1a701197c5dd50a72e4e597a425ba8d169a14fc12f`  
		Last Modified: Fri, 13 Sep 2024 19:49:03 GMT  
		Size: 7.0 MB (7034854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdedfef6487c5179277a1c1e0b1b3c54ae07767e228040cb5c5a811fe7c1fdf2`  
		Last Modified: Fri, 13 Sep 2024 19:49:03 GMT  
		Size: 98.7 KB (98654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634e05990c20695c6c48892dc6cf469dd6626c70c85ed8bd3e105f96c783c99c`  
		Last Modified: Fri, 13 Sep 2024 19:49:03 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23bb319f014001c9c5caeb1f2a2b2006e909e48d39b8b1e96dfdd43a4901341`  
		Last Modified: Fri, 13 Sep 2024 19:49:05 GMT  
		Size: 53.4 MB (53425704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee4c4cf30d85531b89bf617ac64761f57078a00f2b91f55b58be281d072be90`  
		Last Modified: Fri, 13 Sep 2024 19:49:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f51263034402592d852aa8323e3ac28d7aee471146813a1ee9b2c420169478`  
		Last Modified: Fri, 13 Sep 2024 19:49:04 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:43f8c595666e934349314ec8efb6af9dfeb80036e2fbc8377eded6173e8026e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe60ecb9a6f8374d9133031a7da8f76a6302da7b2cd87c33250292cfec3deb56`

```dockerfile
```

-	Layers:
	-	`sha256:46968210e894a46253a6be78978361aa87b42e0c92712119fc5a516c5aeee585`  
		Last Modified: Fri, 13 Sep 2024 19:49:02 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-rc-dind-rootless`

```console
$ docker pull docker@sha256:a138b2d6e7eceef14700731104e31374fa62663b0bcc6f9198007da0395e7682
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:5c1bfa8027800c7e807c061bdbb84dfaad45269de50b9ab17c56cf7f412edcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154381296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be68659af4f7268f61dcf0f3364c9a58762902d5c405cbf1f315b9dc645bda91`
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
# Fri, 13 Sep 2024 16:59:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 13 Sep 2024 16:59:50 GMT
USER rootless
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
	-	`sha256:05d197cefefe24dd3b1807601fc0e9b6a88bf5bd7b3bee8dc2da85e1a6bd500c`  
		Last Modified: Fri, 13 Sep 2024 20:55:55 GMT  
		Size: 981.0 KB (980979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8d901687e2808b520f40052f5d7d321e4a48655fdb21ecf57a60539861d176`  
		Last Modified: Fri, 13 Sep 2024 20:55:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c8e028bc055645bcf24387db68377b7daebf95ba931a9779c8837fc0f55c92`  
		Last Modified: Fri, 13 Sep 2024 20:55:55 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066e9df02b7083cb0f4ff965d35ac3cf0f6745ba1175f37ab157942dc529239c`  
		Last Modified: Fri, 13 Sep 2024 20:55:56 GMT  
		Size: 21.3 MB (21303253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0be4034d35a7ff00b6130f911f1d47aff74e626cf8db42e33d346c976a3c66`  
		Last Modified: Fri, 13 Sep 2024 20:55:56 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:881c8f96fa77745d56e7f859566b90a3c985fc219b4df41e1324ae6d0759daff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81bcd3f8f2e8cfe9cdf1b0dc9a0b0eadc9003f275bc1aec96bcaf3d10b44123`

```dockerfile
```

-	Layers:
	-	`sha256:3a744faaa0d91d90c227db143d45995ce38c952c64de13d91941b010543e650a`  
		Last Modified: Fri, 13 Sep 2024 20:55:55 GMT  
		Size: 30.3 KB (30332 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:70e2e453f35e98780bca193221f61edd7bdaeb49449b57a014b2c82a59c8b2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148542824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77b5b6ca1ab14a0b3b93df753e80e55e91887ccba8cdc804d9d4afc8383ac79`
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
# Fri, 13 Sep 2024 16:59:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 13 Sep 2024 16:59:50 GMT
USER rootless
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
	-	`sha256:5b31505e521f0828b1793c7fb9ed1c7b82011a79d51b9b1f5d5b5933b1ad6d64`  
		Last Modified: Fri, 13 Sep 2024 20:55:39 GMT  
		Size: 1.0 MB (1023120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413c85bfce890fef8930232016a47761758bd10323d2329894211d2bf6116390`  
		Last Modified: Fri, 13 Sep 2024 20:55:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7b6a01e5243cf48964d681fc8f2e151a1bafba40c6970a1edc40db10541b9b`  
		Last Modified: Fri, 13 Sep 2024 20:55:39 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de417e511ef0d9fd12beee32ca144f287917f472277230c3e7ecbeb5e6ca3465`  
		Last Modified: Fri, 13 Sep 2024 20:55:40 GMT  
		Size: 23.2 MB (23155435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43a4f9f5632aa52b2fdaa2ce71e1d9dc8916cd37aabd5e9a6b8d532b63b1410`  
		Last Modified: Fri, 13 Sep 2024 20:55:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:71b2b64025f67219ad9f3ee78e2c2a919c244efde6020e1f57c9328dc4acea55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3f557a8d6fdf0c2211fa6e5be5e505dbe26e3d714fd739ca1a944314f90e7c`

```dockerfile
```

-	Layers:
	-	`sha256:00ac3f049fbf350edb64241cdbf29b0e2736810cdc186d79ed8388f88d40aa4c`  
		Last Modified: Fri, 13 Sep 2024 20:55:38 GMT  
		Size: 30.7 KB (30746 bytes)  
		MIME: application/vnd.in-toto+json

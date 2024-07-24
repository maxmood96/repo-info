## `docker:dind-rootless`

```console
$ docker pull docker@sha256:c43662abbd8abf32085b73cddcb928f87179ab2dd88739d15fbffd652262bddf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:f94d0d3da3cf5e9fdb95235f772365ac0f2f131f7c3cfb09d962f46784a293a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152285329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9550868b3a8bcaca52c6d18ca59e7c2d3f4924ed7af1a7bc5f4e7a6afa225a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 22:56:51 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
ENV DOCKER_VERSION=27.1.1
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 23 Jul 2024 22:56:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 22:56:51 GMT
CMD ["sh"]
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
VOLUME [/var/lib/docker]
# Tue, 23 Jul 2024 22:56:51 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 23 Jul 2024 22:56:51 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 23 Jul 2024 22:56:51 GMT
CMD []
# Tue, 23 Jul 2024 22:56:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 23 Jul 2024 22:56:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56741e8c5dde644686cd3f2a11a32f8724f953216d0d9837363d627b42cc4308`  
		Last Modified: Wed, 24 Jul 2024 01:08:34 GMT  
		Size: 7.9 MB (7869177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27f6c8943b904338a8ae558701839cba64c21dde29b1ded9b4c62a4c427ead7`  
		Last Modified: Wed, 24 Jul 2024 01:08:34 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3757c82e9d264069e508c3fe589e26a690fb71d1b8b2195931dfc069c5b5e324`  
		Last Modified: Wed, 24 Jul 2024 01:08:35 GMT  
		Size: 18.1 MB (18086581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3309cba0d44219a1e777c13796821e83ccce3866e49a485566770ea966bd06c0`  
		Last Modified: Wed, 24 Jul 2024 01:08:35 GMT  
		Size: 18.4 MB (18404716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4d5e7121b245fcdc48e975496f2153fc6c0cfe24dbb98e37ad8f14d0db50ea`  
		Last Modified: Wed, 24 Jul 2024 01:08:35 GMT  
		Size: 18.8 MB (18818931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445e1ed6e1dc5541cddc13f40ba5df4f6a815dde2e5f7bb62dc8c69811f0f392`  
		Last Modified: Wed, 24 Jul 2024 01:08:35 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a491a417f451d50e24310897a831bc7ce3230a78bd1b49e3989c189bcd3051c5`  
		Last Modified: Wed, 24 Jul 2024 01:08:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be10967b7a2ee1dea8494886486f8bd6469fedfef76ff529c77c7cae0121a916`  
		Last Modified: Wed, 24 Jul 2024 01:08:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893bfa801bba6eeb7b1e890a92c31fbfc971e1f58ab91e8f44a003418288af98`  
		Last Modified: Wed, 24 Jul 2024 02:03:42 GMT  
		Size: 6.7 MB (6655117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de773661e3252f4516a6ac1331dd0eb5dc6d9f0067ef148970eb27b80473eb00`  
		Last Modified: Wed, 24 Jul 2024 02:03:42 GMT  
		Size: 89.2 KB (89208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b333cdcea40f543577948f04e283121bc19b4572a67db0d3e349e4595a5ebadb`  
		Last Modified: Wed, 24 Jul 2024 02:03:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffca936be8aa7dee12ed2dfbf78a3423bb8489ca68314964a1532392619d6de4`  
		Last Modified: Wed, 24 Jul 2024 02:03:42 GMT  
		Size: 56.8 MB (56768709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c5636c4d4359b7040a44bfc1eeed3773ebe0b28a7c290429bfaea6d7db4b7b`  
		Last Modified: Wed, 24 Jul 2024 02:03:42 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d475211fe339464f72c4c7d2326ac10db6e638e6236a5cd0c8858854be9e693d`  
		Last Modified: Wed, 24 Jul 2024 02:03:43 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363ca6d5f29caa687127498ed369c72da2fefc89f01f87a3adee26f18b3fc0d5`  
		Last Modified: Wed, 24 Jul 2024 03:04:06 GMT  
		Size: 981.0 KB (980991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7213539d2b706c8cb2e9dc6369fce7d69944e9a71d372efb5d3df3156ce86a7`  
		Last Modified: Wed, 24 Jul 2024 03:04:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0c3e7f5c2d455ddf55d6c01945e8ae6f6c403cb8f7cabddc46b2b0970d7d84`  
		Last Modified: Wed, 24 Jul 2024 03:04:06 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143ee407fc3adfac20302d269c6b6176f5dbd0f190413760bdb8ddf0750d7146`  
		Last Modified: Wed, 24 Jul 2024 03:04:07 GMT  
		Size: 21.0 MB (20979717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e40fd9df58fdf1122184958d36d15c1501b259a28c47b4113d97685aed0eab4`  
		Last Modified: Wed, 24 Jul 2024 03:04:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:47fd13a2e5266c5599790fb92eddfce3e74d93232e65fa449b96e14574033b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19daac2b9e8eb49a187d3389978c673512772af54c973c0956ff6a48fd30f60`

```dockerfile
```

-	Layers:
	-	`sha256:e69115eec31093982eb7d63dee5f692ccef197d16e220e60af4894bdb0079b81`  
		Last Modified: Wed, 24 Jul 2024 03:04:06 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0a6161e3445687def03e8960236252cac54feb7d889d63f7857bfecddb2d3b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146447737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f97220a8935815502c8559821840905d663df49691f1bcbf16b57188c123a5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 22:56:51 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
ENV DOCKER_VERSION=27.1.1
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 23 Jul 2024 22:56:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 22:56:51 GMT
CMD ["sh"]
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
VOLUME [/var/lib/docker]
# Tue, 23 Jul 2024 22:56:51 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 23 Jul 2024 22:56:51 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 23 Jul 2024 22:56:51 GMT
CMD []
# Tue, 23 Jul 2024 22:56:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 23 Jul 2024 22:56:51 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 23 Jul 2024 22:56:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92a79a211e9d2795fd6862e20d285be2e32204ecf133a96c45fc447719c6ffd`  
		Last Modified: Wed, 24 Jul 2024 11:44:26 GMT  
		Size: 8.0 MB (7974652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82180daf56b45cbe34e984171eb389836179453c540ac437fb696fda30111af6`  
		Last Modified: Wed, 24 Jul 2024 11:44:26 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a37a1633e989cf86c03403851118e2684f8a3fc8ac8974b9b60f835b0b79fcd`  
		Last Modified: Wed, 24 Jul 2024 11:44:27 GMT  
		Size: 17.0 MB (17046583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0061de37dc2980d78c57cf24cf8518c3519c1f8f7829eed9fea1ea0df799f47a`  
		Last Modified: Wed, 24 Jul 2024 11:44:27 GMT  
		Size: 16.8 MB (16772744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ebd0d8ed77f2173e4f27fc152e0c2976930a27e263a47e21d696912c311b1b`  
		Last Modified: Wed, 24 Jul 2024 11:44:27 GMT  
		Size: 17.2 MB (17182710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22732944ffc85cf6cd231ef7ff2b518d5e154cc35b9d0526a39722342a9d0fa6`  
		Last Modified: Wed, 24 Jul 2024 11:44:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abe30c621c6c86a650a87aa6d4be3fd7334504e35877921eb6965571809ef1a`  
		Last Modified: Wed, 24 Jul 2024 11:44:28 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a761bfd34c5fdea613828fb98a664da35e085dc686b074ccbc47abb1c7def8`  
		Last Modified: Wed, 24 Jul 2024 11:44:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d5ddf2553d4b14a97027063d617df9ea3246518589f26be4ea9923c817e8f8`  
		Last Modified: Wed, 24 Jul 2024 16:34:09 GMT  
		Size: 7.0 MB (7034003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e756474f77815332da8a2a986ca8e9e26d3d69f9502dbadf2f947da0fd0d2`  
		Last Modified: Wed, 24 Jul 2024 16:34:08 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a246f52b37e861d7c100249cb85744bf2f916466e932bff0acc25402c5a92bf7`  
		Last Modified: Wed, 24 Jul 2024 16:34:08 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d02ed91431aaf7c1716133ba74d80b090544544d4ae80be33f9c6d8badfeb8`  
		Last Modified: Wed, 24 Jul 2024 16:34:10 GMT  
		Size: 52.4 MB (52383336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205bf0fd7438f6f71e86ea071c99139ab288e5bcf412909da61ec77e38284585`  
		Last Modified: Wed, 24 Jul 2024 16:34:09 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acda8f054f83dccf4f1d00b66fd2ca076c2b44c7f91024c9c05b925ceefb7fc4`  
		Last Modified: Wed, 24 Jul 2024 16:34:09 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e2e8eb2eea977e0eb8dc838c477f66a034b2471565a9c12b83e24836fbc95`  
		Last Modified: Wed, 24 Jul 2024 18:16:13 GMT  
		Size: 1.0 MB (1023106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895c97e956e208c77e6f0b216c95e466c224207835aaba4a680748b9577b7b1a`  
		Last Modified: Wed, 24 Jul 2024 18:16:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039d3b2b1600c125206292e97b30c9ffd77adf139b299172ffac13d0f929e4f1`  
		Last Modified: Wed, 24 Jul 2024 18:16:12 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655f0dfc2393167717eb3bd9e580896cd5e2dcb993a9747c59c78c779087e57f`  
		Last Modified: Wed, 24 Jul 2024 18:16:13 GMT  
		Size: 22.8 MB (22835716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617356db6053f8797d154e58816eaa263d994dea99d04d853601a690c889c739`  
		Last Modified: Wed, 24 Jul 2024 18:16:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:117b8da0ec6ee1f92d530f9a4d42025d6a3f8159e00ff95939341a8a7ff99262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a3d68e60e3f45b8d72dd1133f31c2ebd6c28b670dbfbf70077e2b6ee2bfb23`

```dockerfile
```

-	Layers:
	-	`sha256:0025b28d9480d63be72ec83103acc80a2c894314d1a2c0f601ccc7b18add1c0e`  
		Last Modified: Wed, 24 Jul 2024 18:16:12 GMT  
		Size: 31.0 KB (31005 bytes)  
		MIME: application/vnd.in-toto+json

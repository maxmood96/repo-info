## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:7083f1315db561746e4f3ae83482c0113fcf005c691557bf83edcce2b0bee8d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:be6f7ae14fb3e390b1e944cd2b3b162f2ac4df6cb2314c971ae1eaaea70e7102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165581314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7dc96a0ca41408e7a73d2c439dfebee1714e862e088ba196bed2926456c27f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:55:27 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 31 Oct 2025 23:55:27 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 31 Oct 2025 23:55:27 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 31 Oct 2025 23:55:29 GMT
ENV DOCKER_VERSION=29.0.0-rc.2
# Fri, 31 Oct 2025 23:55:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 31 Oct 2025 23:55:29 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Fri, 31 Oct 2025 23:55:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 31 Oct 2025 23:55:30 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 31 Oct 2025 23:55:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 31 Oct 2025 23:55:31 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 31 Oct 2025 23:55:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 23:55:31 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 31 Oct 2025 23:55:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 31 Oct 2025 23:55:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 23:55:32 GMT
CMD ["sh"]
# Sat, 01 Nov 2025 00:10:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 01 Nov 2025 00:10:42 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 01 Nov 2025 00:10:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 01 Nov 2025 00:10:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 01 Nov 2025 00:10:44 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Sat, 01 Nov 2025 00:10:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 01 Nov 2025 00:10:44 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 01 Nov 2025 00:10:44 GMT
VOLUME [/var/lib/docker]
# Sat, 01 Nov 2025 00:10:44 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 01 Nov 2025 00:10:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 01 Nov 2025 00:10:44 GMT
CMD []
# Sat, 01 Nov 2025 01:10:20 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 01 Nov 2025 01:10:20 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 01 Nov 2025 01:10:20 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 01 Nov 2025 01:10:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-29.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-29.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 01 Nov 2025 01:10:21 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 01 Nov 2025 01:10:21 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 01 Nov 2025 01:10:21 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bd06dfc6cd22322de7d4fca516b20c2b75730c5bc85c35e92c3f2056dbfe9a`  
		Last Modified: Fri, 31 Oct 2025 23:55:53 GMT  
		Size: 8.2 MB (8232146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37009c416213bafe8d6e7c68aa4bc36688e1d7b2974ecd8118fa29dab8c9b0e0`  
		Last Modified: Fri, 31 Oct 2025 23:55:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf24787ade0bced5f7ca8d71e250cb12e67485bc5b8bf812cd213a55bc94f3b`  
		Last Modified: Fri, 31 Oct 2025 23:55:53 GMT  
		Size: 19.8 MB (19805491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3ab349f2296fc0a4ddd69178ec259908ee314379e3d62f368570ed018941de`  
		Last Modified: Fri, 31 Oct 2025 23:55:54 GMT  
		Size: 22.2 MB (22158455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c61c9bea5f68b2a2aa832197cb1bb810d6b36cb4735895ceb746d0e189c14d`  
		Last Modified: Fri, 31 Oct 2025 23:55:54 GMT  
		Size: 21.7 MB (21744287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18182459dae86dae7811839e6eadf296ad064ba58da1d6b8b58e44dcb9172aa`  
		Last Modified: Fri, 31 Oct 2025 23:55:52 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56609bdd1938e140d813a1256e544109491dd98457b2d49d90aa82aa81a361a9`  
		Last Modified: Fri, 31 Oct 2025 23:55:52 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb480d5808d4f087ab02cd111c1f2e64a0c626d48ba125213f0d8beac50bda7a`  
		Last Modified: Fri, 31 Oct 2025 23:55:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f151f4d9622877286111d2a954c2ca5bca92df98c5d12f2d7c92c97c36410c`  
		Last Modified: Sat, 01 Nov 2025 00:11:24 GMT  
		Size: 6.9 MB (6905151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a544beed1fafde505e54e5064229b1ad3935460d389463487d25039d38a4042e`  
		Last Modified: Sat, 01 Nov 2025 00:11:24 GMT  
		Size: 90.4 KB (90389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfdce5f072ff5377a29184255be47e28490ca5c2e58e691b19d3a6363867447`  
		Last Modified: Sat, 01 Nov 2025 00:11:24 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d355d5119d2c5b0cf078c9a79a0a1580e6446ecf0b4c08ca2a3401c3ed602e`  
		Last Modified: Sat, 01 Nov 2025 00:11:33 GMT  
		Size: 62.1 MB (62064856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1942e80d1799d684de1603bae07a09f7185f28e0a81fdb1508da61a86df30d9`  
		Last Modified: Sat, 01 Nov 2025 00:11:24 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec9909192e58115090551d38790f5587205a0c349f98ecbedfb2ed7cc1d924`  
		Last Modified: Sat, 01 Nov 2025 00:11:23 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e603f42ab53f89a2db36837376186a18939c5afd730b079b5d0e9a0b0fc89ee1`  
		Last Modified: Sat, 01 Nov 2025 01:10:43 GMT  
		Size: 3.4 MB (3398372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfba3657d4250a87139c4d9dcbc73fa443e2a27a6b7a6fb3e28c13864fda9ca`  
		Last Modified: Sat, 01 Nov 2025 01:10:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa33c6e911515da7290ffe77dd9b6b3daf05326ef024595238074c9883fd8e91`  
		Last Modified: Sat, 01 Nov 2025 01:10:42 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e30f06c38526b5c6650af4ea6b88e3d14822d7a3e17c9ce3dd382d31b24ba0c`  
		Last Modified: Sat, 01 Nov 2025 01:10:46 GMT  
		Size: 17.4 MB (17370216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba684d24a8426ad3d3c812b20813e2e0c6b5d5ff21a47496a1e2492dda7f9e2`  
		Last Modified: Sat, 01 Nov 2025 01:10:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:aceb237b4290da75a6e92ec63ee92538aee022b0329671465ebfec537ea4194b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2003d2b3623f972bec513aedadf1e6acb722d6a73d8c38229dcdd1d9b793b3`

```dockerfile
```

-	Layers:
	-	`sha256:c198518f5bcc01e1258cf7b2c0b2eb272fc95b23419b26c9cc8fc8f00456f45b`  
		Last Modified: Sat, 01 Nov 2025 02:10:15 GMT  
		Size: 30.3 KB (30346 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:28dedd7ebc4219824f4fed5efca9992223ecaa563c24d247b09a57379ae73bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155510871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e512a44c519aabcc1a297923be4df06baac21de6e1a184f169f223f986f5981`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:54:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 31 Oct 2025 23:54:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 31 Oct 2025 23:54:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 31 Oct 2025 23:54:34 GMT
ENV DOCKER_VERSION=29.0.0-rc.2
# Fri, 31 Oct 2025 23:54:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 31 Oct 2025 23:54:34 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Fri, 31 Oct 2025 23:54:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 31 Oct 2025 23:54:35 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 31 Oct 2025 23:54:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 31 Oct 2025 23:54:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 31 Oct 2025 23:54:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 23:54:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 31 Oct 2025 23:54:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 31 Oct 2025 23:54:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Oct 2025 23:54:36 GMT
CMD ["sh"]
# Fri, 31 Oct 2025 23:56:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 31 Oct 2025 23:56:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 31 Oct 2025 23:56:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 31 Oct 2025 23:56:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 31 Oct 2025 23:56:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 31 Oct 2025 23:56:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 31 Oct 2025 23:56:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Oct 2025 23:56:24 GMT
VOLUME [/var/lib/docker]
# Fri, 31 Oct 2025 23:56:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 31 Oct 2025 23:56:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 31 Oct 2025 23:56:24 GMT
CMD []
# Sat, 01 Nov 2025 00:09:48 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 01 Nov 2025 00:09:48 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 01 Nov 2025 00:09:48 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 01 Nov 2025 00:09:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-29.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-29.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 01 Nov 2025 00:09:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 01 Nov 2025 00:09:49 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 01 Nov 2025 00:09:49 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fff282eeb7407767e807c8e2c701b008eca2417074d98c632fd2c1c9e32668`  
		Last Modified: Fri, 31 Oct 2025 23:54:59 GMT  
		Size: 8.3 MB (8257245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7cf680c517246f7558d98e9fe663129cf4431c15bf708a9dfdb88b07fa173d`  
		Last Modified: Fri, 31 Oct 2025 23:54:58 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b79e6356cad8ca6dd9b94a95cdca0a0e0b49203cdaf787f51e330a960f266e`  
		Last Modified: Fri, 31 Oct 2025 23:55:00 GMT  
		Size: 18.3 MB (18306480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0478849bd227cbdc57a0d01ca2dae045cf5b8413ce8c30c88bd607b4b2c32986`  
		Last Modified: Fri, 31 Oct 2025 23:55:00 GMT  
		Size: 20.3 MB (20273412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cad1d7bfcca1d68c15f1c4cc808053e6475ca91b915b60ac79d38a0a5691b6`  
		Last Modified: Fri, 31 Oct 2025 23:54:59 GMT  
		Size: 19.9 MB (19869852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e662988fc7e1e3cb09e505bf4685896ca72343f7b0fc0225d40a523be2279a4`  
		Last Modified: Fri, 31 Oct 2025 23:54:58 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdb4a8a086c4821e6911e6b504ec97a50ddcbc0fcf568f187ec45461d4ac11f`  
		Last Modified: Fri, 31 Oct 2025 23:54:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fd87c830a2473ee69a18b026de66a888c6f81eb3bbe5b23c73b4c2e4b0f59b`  
		Last Modified: Fri, 31 Oct 2025 23:54:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fa77a501b81fe29e4a169253280bd0bf426e237aad5082f65bb91fa7ffc454`  
		Last Modified: Fri, 31 Oct 2025 23:56:42 GMT  
		Size: 7.1 MB (7140833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9bbca9ebef0ac39fef01d6db8aa69b2d30eccbc579ee5a2a6e72b838c906e3`  
		Last Modified: Fri, 31 Oct 2025 23:56:41 GMT  
		Size: 99.5 KB (99504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be95a09ecf16c7620d38a512de8ede5a896bf82ba945f2426526f503ea5ad6a`  
		Last Modified: Fri, 31 Oct 2025 23:56:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06ac8130b296f601472a0962d21ce42f78a56583e8cd9e8f754e83e54e55829`  
		Last Modified: Fri, 31 Oct 2025 23:56:45 GMT  
		Size: 56.3 MB (56319207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ce44bb40b6d434fd80d453b5e0b51beab29173dd22d19bcf8344e7e8fd96c9`  
		Last Modified: Fri, 31 Oct 2025 23:56:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c707f7d32dcddb0115c41a7df9c780d3e7165bda23bc9e3f88797355bf0d39cd`  
		Last Modified: Fri, 31 Oct 2025 23:56:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c06a237840ceed2bccffcd0c5148fcd3923be406666f706a9059c7a659663a`  
		Last Modified: Sat, 01 Nov 2025 00:10:24 GMT  
		Size: 3.4 MB (3389951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1984fe81b12caeab1c1a51ac4d5e3615e17846eca40233b6f39b06409e05a3`  
		Last Modified: Sat, 01 Nov 2025 00:10:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791b3bd4d1b5956ae1eed6bf78ea762c994d22cc75a96564d24af8ea4af6c6d7`  
		Last Modified: Sat, 01 Nov 2025 00:10:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b050f9de950435d90de4d95b2633e162016d2429e6f47d1dd39e44a2cde81f1`  
		Last Modified: Sat, 01 Nov 2025 00:10:23 GMT  
		Size: 17.7 MB (17706826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661d523cc37231eada1cd4a8f64dbab21e7475f6ff996c37bc6a2a3ca6ed95c5`  
		Last Modified: Sat, 01 Nov 2025 00:10:22 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:947c4c179533987752026838fcf860c71a88adb4bc1d671e9505d70ab968641c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ad11f285ed226d9f9e853d0c6da15ce39e37e261657cc9644e7bbe074127f1`

```dockerfile
```

-	Layers:
	-	`sha256:7cf44a10065c15dc5f704516cff9957c0517c17fae9de241ea2c8abc886357f7`  
		Last Modified: Sat, 01 Nov 2025 02:09:40 GMT  
		Size: 30.5 KB (30498 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:dd6572f903f54e70e75865a69473c1ca45118c47b4a34d532eb99190ba56bfc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:7955ac6376573d4ec0236dc957481947c018bda491cda2103215fcf4c3a23142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165476964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97112eeee8518d786df6e408c57da648f3295c7f7a8fa018395f888e3ea80d53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 21:49:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 24 Nov 2025 21:49:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 24 Nov 2025 21:49:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 24 Nov 2025 21:49:55 GMT
ENV DOCKER_VERSION=29.0.3
# Mon, 24 Nov 2025 21:49:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 24 Nov 2025 21:49:55 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Mon, 24 Nov 2025 21:49:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 24 Nov 2025 21:49:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Mon, 24 Nov 2025 21:49:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 24 Nov 2025 21:49:57 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 24 Nov 2025 21:49:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 21:49:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 24 Nov 2025 21:49:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 24 Nov 2025 21:49:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 21:49:57 GMT
CMD ["sh"]
# Mon, 24 Nov 2025 22:10:29 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 24 Nov 2025 22:10:30 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 24 Nov 2025 22:10:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 24 Nov 2025 22:10:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 24 Nov 2025 22:10:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 24 Nov 2025 22:10:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 24 Nov 2025 22:10:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:10:33 GMT
VOLUME [/var/lib/docker]
# Mon, 24 Nov 2025 22:10:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 24 Nov 2025 22:10:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 24 Nov 2025 22:10:33 GMT
CMD []
# Mon, 24 Nov 2025 22:34:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Mon, 24 Nov 2025 22:34:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 24 Nov 2025 22:34:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 24 Nov 2025 22:34:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 24 Nov 2025 22:34:53 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 24 Nov 2025 22:34:53 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 24 Nov 2025 22:34:53 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c58c82c3f01cae926b34b45feaf2248a180d124b8d96370715a63a233c3d96e`  
		Last Modified: Mon, 24 Nov 2025 21:50:15 GMT  
		Size: 8.2 MB (8232194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73af2fe09aa51103409ce995f010e7a99758cdb2947b175114ce981239f47414`  
		Last Modified: Mon, 24 Nov 2025 21:50:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157febd1a8b3ffb2f88cf5f42236d749bf1e1216d99c8f545098d98b9310e237`  
		Last Modified: Mon, 24 Nov 2025 21:50:15 GMT  
		Size: 18.8 MB (18757774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033545eb99da7aa09e415f357db1257c07dc854379c004159a1f63ec4b7c02fb`  
		Last Modified: Mon, 24 Nov 2025 21:50:15 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19f983d31f1f707462165c11f271b1c212d8e96dc842b0448503f09952fd285`  
		Last Modified: Mon, 24 Nov 2025 21:50:15 GMT  
		Size: 21.7 MB (21744283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068788f67c164250744fa2a27e66692ae8e191f5514f32e8be1c27d59ed42561`  
		Last Modified: Mon, 24 Nov 2025 21:50:13 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f972c8ce0fb024875291f8e9693e62ed8916d6b78889756f10170f081c85a5`  
		Last Modified: Mon, 24 Nov 2025 21:50:14 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8309d0d86a665a82e3fc1d9f035cff1a6ccfe6c953063e5519268475853c31e4`  
		Last Modified: Mon, 24 Nov 2025 21:50:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9197053d15518c43b788fd46024ad8bd64a17b1f208b4c48ab9e7fa548fd2f`  
		Last Modified: Mon, 24 Nov 2025 22:10:56 GMT  
		Size: 6.9 MB (6905414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a038d4b396b86622e31f6a1522ae7184b5b50143935c4f2721f22d49deff25e9`  
		Last Modified: Mon, 24 Nov 2025 22:10:56 GMT  
		Size: 90.4 KB (90387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe155d69f1afe39250f7f036fe26fb282dbac1efa0c7e0b2c228c31888e9937`  
		Last Modified: Mon, 24 Nov 2025 22:10:56 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25be230caed8526f00b9fe93cc7faf07784ed7be09db77982dd6b66aa44389a`  
		Last Modified: Mon, 24 Nov 2025 22:11:03 GMT  
		Size: 62.3 MB (62260902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9347d90c0850810ca20741bea147c808baaae31a163e04544ff6c9fd3977cbcd`  
		Last Modified: Mon, 24 Nov 2025 22:10:56 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d688e0e8bb43ad1a1d2e7948280f64a14fcc11ab6cc82bd1ec5d1652de964d`  
		Last Modified: Mon, 24 Nov 2025 22:10:56 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81c6f62dd7066cb1c1404136678de20214bdcb1ca736f197c341fa074d65c26`  
		Last Modified: Mon, 24 Nov 2025 22:35:14 GMT  
		Size: 3.4 MB (3398366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd07630b57b582ef0320410a380bd1079621bfc667aced8b80327a03db72dc2b`  
		Last Modified: Mon, 24 Nov 2025 22:35:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da94c6d5b8a188de66bee0fbac5c0a327c772a3880bb83e246c3ea84182227e8`  
		Last Modified: Mon, 24 Nov 2025 22:35:14 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e426cbb795580af6915a9095962fa325d240069dbc338a040c4209648bfe9d94`  
		Last Modified: Mon, 24 Nov 2025 22:35:25 GMT  
		Size: 17.4 MB (17370226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae3ff191adef5fd2f0d36c95347d0bb46d5339edff3cb37677b5ef0fb9a1fd6`  
		Last Modified: Mon, 24 Nov 2025 22:35:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:45ec192d3fdeaba5142d39791966924f8666f262129a5d55590c85df2a22dd0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dc2ad8bbcd7c76e87902110fc690583b4bea835ef26ce7f76684ddd18485f6`

```dockerfile
```

-	Layers:
	-	`sha256:7debd1a40e1be84cbf76216a270c1f24314d8dca3af673deabce9d7c77f9cc44`  
		Last Modified: Tue, 25 Nov 2025 00:08:02 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:be8919a2e608103a1cd5ac85a024381303084741c56e5f183bea30bca299c229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155077142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb1efbc9f0413bf5ddd60d24403d65a7e86b63fdb07c4078462060051d99ddb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 21:51:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 24 Nov 2025 21:51:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 24 Nov 2025 21:51:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 24 Nov 2025 21:51:20 GMT
ENV DOCKER_VERSION=29.0.3
# Mon, 24 Nov 2025 21:51:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 24 Nov 2025 21:51:20 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Mon, 24 Nov 2025 21:51:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 24 Nov 2025 21:51:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Mon, 24 Nov 2025 21:51:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 24 Nov 2025 21:51:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 24 Nov 2025 21:51:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 21:51:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 24 Nov 2025 21:51:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 24 Nov 2025 21:51:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Nov 2025 21:51:23 GMT
CMD ["sh"]
# Mon, 24 Nov 2025 22:09:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 24 Nov 2025 22:09:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 24 Nov 2025 22:09:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 24 Nov 2025 22:09:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 24 Nov 2025 22:09:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 24 Nov 2025 22:09:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 24 Nov 2025 22:09:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 22:09:55 GMT
VOLUME [/var/lib/docker]
# Mon, 24 Nov 2025 22:09:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 24 Nov 2025 22:09:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 24 Nov 2025 22:09:55 GMT
CMD []
# Mon, 24 Nov 2025 22:35:35 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Mon, 24 Nov 2025 22:35:35 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 24 Nov 2025 22:35:36 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 24 Nov 2025 22:35:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 24 Nov 2025 22:35:37 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 24 Nov 2025 22:35:37 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 24 Nov 2025 22:35:37 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5242364323c82f967750feb98c18ae0bd443b98ba4ae65c1290a1749b3fd3a2`  
		Last Modified: Mon, 24 Nov 2025 21:51:44 GMT  
		Size: 8.3 MB (8257260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599a21982607353c3b363454d4a46e6fe7fd51f2ce11e094ac72bf595a00ba72`  
		Last Modified: Mon, 24 Nov 2025 21:51:42 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7f2dfec92154168250cda24dcca0745835d9f438ca6fa6c4e1e25cffe8eca1`  
		Last Modified: Mon, 24 Nov 2025 21:51:47 GMT  
		Size: 17.3 MB (17326085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874c9a1e4bef5f6683a2b0c5cd5d9e947cbc46abccf5317f3968240c37015d20`  
		Last Modified: Mon, 24 Nov 2025 21:51:46 GMT  
		Size: 20.6 MB (20645069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbda01a59a356bda61a3f9a572c426393bf7a9363100f37f1c890449a7ef014`  
		Last Modified: Mon, 24 Nov 2025 21:51:46 GMT  
		Size: 19.9 MB (19869858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a574da6021bf9c1bd284b0909fcf1908358f3712ad6adbf58d178361037c9d0c`  
		Last Modified: Mon, 24 Nov 2025 21:51:43 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb6fd58a95488062f4eb908d8ab2fe7be1167bc4e736b5d65777071c54bc28f`  
		Last Modified: Mon, 24 Nov 2025 21:51:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53bb390e848a19d3282fbd3c0ec44e7543e1292bbec4a67595b0e0e94b15435`  
		Last Modified: Mon, 24 Nov 2025 21:51:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cddd679a0252d547df7d3b1caa6683eb4a50d96719f3317d4f3f5206746b30b`  
		Last Modified: Mon, 24 Nov 2025 22:10:19 GMT  
		Size: 7.1 MB (7140928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f36bb36c518e8f044892a3c7695d0e1b6cf57f8bf3ec013a631d57b30766e47`  
		Last Modified: Mon, 24 Nov 2025 22:10:17 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef144f8ee119700b1493b5864607d13138371d281c320ad1550ad8ead803295`  
		Last Modified: Mon, 24 Nov 2025 22:10:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b475d8cd09e5ab78b4c8eed92c57379fda2f58e552551aeda27cc363048160`  
		Last Modified: Mon, 24 Nov 2025 22:10:39 GMT  
		Size: 56.5 MB (56493899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d16721b384e86e26eda92365b7b0aee3b18057abb3039c142c24411a11a4f18`  
		Last Modified: Mon, 24 Nov 2025 22:10:17 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9124fb6450beb85b1200deb3c24366c6504771e9209fd2f569d294514d7cb2b7`  
		Last Modified: Mon, 24 Nov 2025 22:10:17 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70798de9b1c578e124da63dbbbba60afe13562748c6cd94b01a25f9277e5cf2`  
		Last Modified: Mon, 24 Nov 2025 22:35:58 GMT  
		Size: 3.4 MB (3389932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8888c456fd0ef0ebe0d580a53fcf44b37126b9c86ddc746250fc2f178e2e6054`  
		Last Modified: Mon, 24 Nov 2025 22:35:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb48423b3aa0c133b85cb9cf431eee4358f68a64b24786a009481b04225f0998`  
		Last Modified: Mon, 24 Nov 2025 22:35:56 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13a0fba2d5a23a4ae750453bbb50938f2a62a2b9c9dba4b813a3712eb26e374`  
		Last Modified: Mon, 24 Nov 2025 22:35:58 GMT  
		Size: 17.7 MB (17707045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91845071f107b349b21519f87509a64c09c276a66a15bdace0e5669afabec035`  
		Last Modified: Mon, 24 Nov 2025 22:35:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3af2f55d31aa29943673a1bd242ad62148127e1d6f5bd4498cfe07c9d7bdaebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434f867e42fca5aa5f42d705699cc49702d30a2689975550dc8ea2aa252c1182`

```dockerfile
```

-	Layers:
	-	`sha256:6ed9a410ca34d41bee42e0c2cc2ec934bcb7cf23e228aa349faa8e10482b702b`  
		Last Modified: Tue, 25 Nov 2025 00:08:07 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:24-dind`

```console
$ docker pull docker@sha256:6a9019f75c7897050a494cd8ff7a5088eddd3debd4f6404687df372569aec28c
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

### `docker:24-dind` - linux; amd64

```console
$ docker pull docker@sha256:89bb9fd01bb61df10983947a28cda174b71a24f8ed9e8ea1aa68a17ae04a21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125493106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50357febbaef97e0945cc30f3c5a599b36479add518b803f0f68cc8505283e8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-x86_64'; 			sha256='59c6b262bedc4a02f46c8400e830e660935684899c770c3f5e804a2b7079fc16'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv6'; 			sha256='97dac0aa10961ea30a79f6fe2c4a13bfe4da562926365a63042fcceb88d9d125'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv7'; 			sha256='d607ed69f5fe92ee1fd831cf764f977174c86192957a4de678c01db671c3dc52'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-aarch64'; 			sha256='6f00ed24a846046b441c0f0a0f8c1e00194f4b0e33f2433fac0d2dd0e486fc80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-ppc64le'; 			sha256='e3afa6956f6cd4fdbaa8fe19781ae07a1bb8fb2f4d54a1aac857090d6fe1710d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-riscv64'; 			sha256='1d080f5bc04b4b97c61ce3f57ff4a7bd11299f486bc287833f162360be201a7d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-s390x'; 			sha256='5f302fb8e7d973b53f1f9dc808d2b1af08f94687cb14b3f26cc7b358854184b5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 Feb 2024 19:50:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db287e1a31efcf9777aad3e2c2c3f291dcbc6699d6f724c84e214dc0c115480d`  
		Last Modified: Mon, 25 Mar 2024 19:12:09 GMT  
		Size: 2.0 MB (2026164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e831544aa5c9d57189049c63ea52987f006bbb75724b9deecb0726779e43b47`  
		Last Modified: Mon, 25 Mar 2024 19:12:09 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb4489284b20da66de816b146752624ad53d3eda0e70a9d76dc7ddf939c983b`  
		Last Modified: Mon, 25 Mar 2024 19:12:10 GMT  
		Size: 16.4 MB (16410668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0468f26daa7d03bebe8f89ebccf4f8f3be57535a189c1b55bd421c992063c046`  
		Last Modified: Mon, 25 Mar 2024 19:12:10 GMT  
		Size: 18.0 MB (17982274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3995726f3782ab957cc5185b026052ad131d846d69d6d4d7bd501541488294`  
		Last Modified: Mon, 25 Mar 2024 19:12:11 GMT  
		Size: 18.7 MB (18669704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec7527505c01a9ff1503f472842cb806973fe24e89ced47e2a6c981bb6d0d23`  
		Last Modified: Mon, 25 Mar 2024 19:12:10 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9503abbf3673059fff872da078d8b27f029454b55109ad29e4a24d2c22bac7`  
		Last Modified: Mon, 25 Mar 2024 19:12:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76772a122dd0128244aa2ff6fecdd261df83eb325cae7b3ee80f2839730032ef`  
		Last Modified: Mon, 25 Mar 2024 19:12:11 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68ad44a1792b111a70bfc3c2fe686a1123935c055487f0eebb588a8dd1c31d2`  
		Last Modified: Mon, 25 Mar 2024 20:11:58 GMT  
		Size: 12.2 MB (12157613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef560c0b3457952325a69c7f758335131ecafd9a5a232256243f79ffae46392a`  
		Last Modified: Mon, 25 Mar 2024 20:11:57 GMT  
		Size: 89.1 KB (89123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e7c21509bd60c57df9610632c83c32ab39e0006c0bd5800ea1e797be588224`  
		Last Modified: Mon, 25 Mar 2024 20:11:57 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3460e0c19a0843ffa69741977c7ba8eab5afa0c7ca530d0942f255f9cd3e0f35`  
		Last Modified: Mon, 25 Mar 2024 20:11:59 GMT  
		Size: 54.7 MB (54740517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6407e2ae259ebc4f46af358b00d45bc4bd4c9be53c2bdcf5a6f9a4e3c6301be`  
		Last Modified: Mon, 25 Mar 2024 20:11:58 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83644f0385bef6b73e7fadc12f143fec46ef31e61d5a91a027283b9478eba1e6`  
		Last Modified: Mon, 25 Mar 2024 20:11:58 GMT  
		Size: 3.2 KB (3248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0d6210863bf04e593e169205519f290b50e5c985b7de5dae211d1771d439bbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.9 KB (869904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdf313dfa9f365db15c845875147a621f2264350015a4f7342011be907833fb`

```dockerfile
```

-	Layers:
	-	`sha256:52912949613d57bdcb85bc16a37e5f7d40fea9d25cc184df5d9a2ea95ee04529`  
		Last Modified: Mon, 25 Mar 2024 20:11:57 GMT  
		Size: 833.3 KB (833337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:094ac69cffb7bb7468837cffcf0d95307efbaa1eaaef9afea90f52928ff7e540`  
		Last Modified: Mon, 25 Mar 2024 20:11:57 GMT  
		Size: 36.6 KB (36567 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:397fb4781af1005b530736feb90ec0e526e221677d6ca5a61f6c090f4648f58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118706185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaf969cafbb8015226b6f03314d1da244729113cfe31b4d38bd8b54275ef2a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-x86_64'; 			sha256='59c6b262bedc4a02f46c8400e830e660935684899c770c3f5e804a2b7079fc16'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv6'; 			sha256='97dac0aa10961ea30a79f6fe2c4a13bfe4da562926365a63042fcceb88d9d125'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv7'; 			sha256='d607ed69f5fe92ee1fd831cf764f977174c86192957a4de678c01db671c3dc52'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-aarch64'; 			sha256='6f00ed24a846046b441c0f0a0f8c1e00194f4b0e33f2433fac0d2dd0e486fc80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-ppc64le'; 			sha256='e3afa6956f6cd4fdbaa8fe19781ae07a1bb8fb2f4d54a1aac857090d6fe1710d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-riscv64'; 			sha256='1d080f5bc04b4b97c61ce3f57ff4a7bd11299f486bc287833f162360be201a7d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-s390x'; 			sha256='5f302fb8e7d973b53f1f9dc808d2b1af08f94687cb14b3f26cc7b358854184b5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 Feb 2024 19:50:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b118eac215e4599e4010c9e5f0a1e8d36da6b557f5f7ff6cac0b485c2f1aeb3`  
		Last Modified: Mon, 25 Mar 2024 19:52:24 GMT  
		Size: 2.1 MB (2116777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487abfe1cd292c85e2f7bff0176655656a8cfb029d981b200971d5a138a7f45`  
		Last Modified: Mon, 25 Mar 2024 19:52:23 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5301b42da6d861647ddfc3b0d09cecbbab954362d40834f05a27263f99770830`  
		Last Modified: Mon, 25 Mar 2024 19:53:42 GMT  
		Size: 15.1 MB (15132927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd96011584977ee239b0fa6a2b1eb252ba89c810abb180a6d1411bcbbb52773`  
		Last Modified: Mon, 25 Mar 2024 19:53:42 GMT  
		Size: 16.8 MB (16818351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d549fbbdfa07152c9c9ca0cbbebb9dafe0a9aedc10450d6770561a42fe8f7cef`  
		Last Modified: Mon, 25 Mar 2024 19:53:42 GMT  
		Size: 17.6 MB (17631446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b39ff9786f0e336f4cdf4a91745aab6db64287bfcd940580c6d05e391739630`  
		Last Modified: Mon, 25 Mar 2024 19:53:41 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4138dd4277360a1e0be6c90d52c44e6daca90937f271cf5e25f38debbf619479`  
		Last Modified: Mon, 25 Mar 2024 19:53:42 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed529f263af8c05c8aaa26bef70433f895bd905afa4fbfd4914a6375913cb38d`  
		Last Modified: Mon, 25 Mar 2024 19:53:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbc3eb88fae6af81f56280dc8bc7b86e69bb18180adec0cf9ec380909c6bf6b`  
		Last Modified: Mon, 25 Mar 2024 21:12:29 GMT  
		Size: 12.4 MB (12439209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60891173beb56b863df4323eb78707457d47db05f1951e1157ef8a008956656`  
		Last Modified: Mon, 25 Mar 2024 21:12:28 GMT  
		Size: 88.4 KB (88359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93cbb8f70edef086dae6519fa5acfd0505f7e44c93db0f97ecdbbd21d0d2749`  
		Last Modified: Mon, 25 Mar 2024 21:12:28 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b2c04c443c42f9bfc4ba552e6b11326e6a4213c1ffd5a4769907809bac4ecb`  
		Last Modified: Mon, 25 Mar 2024 21:12:30 GMT  
		Size: 51.3 MB (51305397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f982f22a447e60744df508fa116cb1aa68d456389b12d1cc4026a3f37ffd6f4`  
		Last Modified: Mon, 25 Mar 2024 21:12:29 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d0d47b48813b52e0d636af1ffc8e01f39c2b967db0e4bee5f0e9b595175b73`  
		Last Modified: Mon, 25 Mar 2024 21:12:29 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:eb5ae3f6a0bd0a944b9ddd2f6389ab83832b5bfcb816b94fae0c2f52fe170bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c61f92ec36fa9888e51fb05364b4441ec0f97287cab6b62613951eefa7731de`

```dockerfile
```

-	Layers:
	-	`sha256:676e9c46ed9a414cd869ac57dec417c3b88e1864b519483a08bd013285dfa856`  
		Last Modified: Mon, 25 Mar 2024 21:12:27 GMT  
		Size: 36.6 KB (36584 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:09446cbb7a739d231206dfc47ee05c05b301a9d5c7580e838996f75d246e1006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116629018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a64061ecf2def2f7aef1355bf543480fe5fdb29bf8a2374d427811cd2a0bbf4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 Feb 2024 19:50:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62203ebc003cf77a4ff92a3c67a89cd14dcf1adf84fb125d2f3329ad08ad9a61`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 1.9 MB (1896160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8418dd6a88f431ade9efd4277500a4c6483d9ac98459ff95a86dbfde7d02e2a`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8cafec6b550d963e5bc382529ada61abf96cd399412c7e2fd100417257b6a5`  
		Last Modified: Sat, 16 Mar 2024 15:29:41 GMT  
		Size: 15.1 MB (15129219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae6802d0c1ec3f2352b6a3a357cea342d8193b226555358473919d18c1c69a7`  
		Last Modified: Sat, 16 Mar 2024 15:29:40 GMT  
		Size: 16.8 MB (16804624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51029c41a9a83ba7e42604a1512b2162230fa00eaaf905a6c6fdb72048877d2c`  
		Last Modified: Mon, 18 Mar 2024 22:50:50 GMT  
		Size: 17.2 MB (17207758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918889663f8d6f0a6d883cdd72d4b35210027eac7d7ad18751e516a016d387f9`  
		Last Modified: Mon, 18 Mar 2024 22:50:49 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c413941ebd6725db6bba79be5784f7e0438dd09d95e4c907bba2909b9fd5d588`  
		Last Modified: Mon, 18 Mar 2024 22:50:49 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d985ba40d165906552c799cf945866e541363fc468a378f45b5a749ef00ffc`  
		Last Modified: Mon, 18 Mar 2024 22:50:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58756814098cc78f8cc7368809a631f85f85c28f5b91ec9e0bfffdc4e27b9a4b`  
		Last Modified: Mon, 18 Mar 2024 23:56:15 GMT  
		Size: 11.3 MB (11274358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544f21d94b35c15069865108ede9659affa7d0fc1f2e27eeefdc66d81e3b4f64`  
		Last Modified: Mon, 18 Mar 2024 23:56:15 GMT  
		Size: 84.3 KB (84272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d89c0548ebcd9a266f621d43eab3db28eafb6f5fce5b708f46511f1fe4fffea`  
		Last Modified: Mon, 18 Mar 2024 23:56:15 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2e670d64fc6e51da4630c1bc0e5522dea0f3f5b2556f027ac471ab06ad085`  
		Last Modified: Mon, 18 Mar 2024 23:56:17 GMT  
		Size: 51.3 MB (51305403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00217ec4689e19854c789d97a8694168f9f0a1184949e86613a9ec5a5dcd969`  
		Last Modified: Mon, 18 Mar 2024 23:56:16 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b11b8d4888e082be4f9d5c0f206bbf5b25a6d77dcf1400b2e8743ec2827595`  
		Last Modified: Mon, 18 Mar 2024 23:56:16 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1a73e7a09a854b5f5459964170e63c8ea2a3ea7b9742b6833cbdb0ab324f5e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.8 KB (887823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0142980809c0d66befcbb3952e08f5ae6e9294772b980512c58df6bafacfce12`

```dockerfile
```

-	Layers:
	-	`sha256:b59524b75113ffffb8daf9662a44897ec7f6832837a465756a3609b489ceab38`  
		Last Modified: Mon, 18 Mar 2024 23:56:14 GMT  
		Size: 851.0 KB (851024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e283c8deb4de3501378a7686103264dece25e5ed0eb7e52461230e7f856259c5`  
		Last Modified: Mon, 18 Mar 2024 23:56:14 GMT  
		Size: 36.8 KB (36799 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9a38d02f72f943e3d0925d333ccd08c5be7506796311019dbb6d6d990e052ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116632052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17e126bdf0965b023a7858eac3f1fd1668a5b49bb202c2cef0dec73faefd320`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.25.0
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64'; 			sha256='53641b8a28419f947bc58c085e0c39b97a209b6e875a25c585e7fab44ff48576'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv6'; 			sha256='a123b79b530a65c7381ca8bb3b29cde7177f4f260984a127d998c9696cae794c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-armv7'; 			sha256='8ea72e93e8da8259d7d5d051f3c65dc14c44a23d5ebc6939394d7d03b147e238'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-aarch64'; 			sha256='b9f303c9f9db75ecf18ea6fc516b3dc54a3e54f3b3d8e7f1a449416522958bc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-ppc64le'; 			sha256='dc067ab61239cef3d2e145d37fcd68c1fc2320c6728d77a9a4ec4fb0e6c6dd64'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-riscv64'; 			sha256='a17f07604fa74c661e62d5e27ae358f8a611f42bb9a4a147cec76b8bb591bea4'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-s390x'; 			sha256='9e613275e5fa46cb864d3f2fccb10e3239b879527d075490b03e381df56c397c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 Feb 2024 19:50:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b275a3377f65492f727dc46aa2b70be6ec8ff96583fcd9a7b699692b5170bc`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 2.0 MB (2019704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c53acdebd8fb391eae546ed72149f049f8ab4d594f12c74c49be04cc3b9708`  
		Last Modified: Sat, 16 Mar 2024 04:06:08 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e243595b6a4a5354eda3c1c4af2133475005f29ef8acc4da4821fc7fff21a2`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 15.5 MB (15459111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1ea7a6c39e124859c5e26c544d7aff02e08d3965595d626d90a9d54bb420cd`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 16.3 MB (16349525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db075556d6c3ec65e7212ebf5868c54a6b2a003f52befa03b0afa0aea93e98c0`  
		Last Modified: Mon, 18 Mar 2024 22:52:02 GMT  
		Size: 16.6 MB (16646403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c700a96bcdc706c72c84a269d64cf06bd721fc2b9a2a2bafb6d124007f7018a9`  
		Last Modified: Mon, 18 Mar 2024 22:52:01 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0372966def7c7241c44600727ffcc456f40f50233ee0e03dc9a6b57d21815372`  
		Last Modified: Mon, 18 Mar 2024 22:52:01 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1049c071c865dcd9c40f4a80d5902fa62c58d956ad1197278eda9b8ddcb0204`  
		Last Modified: Mon, 18 Mar 2024 22:52:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc57cf04b3492fc7ffe50e5e6dd6d2add34ad98b14aedf724addbc62ea6f6e8c`  
		Last Modified: Mon, 18 Mar 2024 23:54:25 GMT  
		Size: 12.6 MB (12626700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b39887c91a4fdcc838ebe34eccf51f26f8ee5c5ba5e306136e0a07adcef0dd`  
		Last Modified: Mon, 18 Mar 2024 23:54:25 GMT  
		Size: 98.4 KB (98388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f92e21283fab8a1681b55b6bc70e8d93f48ee6de8e36a009d4be4a465b712f1`  
		Last Modified: Mon, 18 Mar 2024 23:54:25 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831af8af4683aa4b9c89c1aefba4d75aa4e9086eee716afbde7033a93f5e0327`  
		Last Modified: Mon, 18 Mar 2024 23:54:28 GMT  
		Size: 50.1 MB (50076174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69eb9c9407f2780cf4782b8e6e65af1a1f620ecca5a988fb5e6aed2723aa1133`  
		Last Modified: Mon, 18 Mar 2024 23:54:26 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58de5aa29ef2154b96b26ae30a51d36b224370eb6b211cb8eb0964fb2cf3600`  
		Last Modified: Mon, 18 Mar 2024 23:54:27 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind` - unknown; unknown

```console
$ docker pull docker@sha256:36d6ae6f10578971167359a7d2d8f24ad7fcf4eea6c8ca85b7c39cbe424a23f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **885.6 KB (885558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1eb0b07780c305bf8aa3dd0f410b6fe63fdee97f7421a70fe595944df9303a`

```dockerfile
```

-	Layers:
	-	`sha256:7dabb321917123a34b0d968914cb51c28f784d9d5d3f5eaac20f6ebf42e3a65b`  
		Last Modified: Mon, 18 Mar 2024 23:54:24 GMT  
		Size: 848.9 KB (848913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fcb48f71ad823ca71fd7069112b3c2d75fe215f6a894da27dabec55b7e7b095`  
		Last Modified: Mon, 18 Mar 2024 23:54:24 GMT  
		Size: 36.6 KB (36645 bytes)  
		MIME: application/vnd.in-toto+json

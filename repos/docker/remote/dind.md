## `docker:dind`

```console
$ docker pull docker@sha256:2ceb471176ad51e37145d43ce7cbf0fa5d644a2b185bd537f0ef695fb3a37497
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

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:b0ea6e8d57b28d04a6999591fdd0f10de8717e956f4f4b6128d2a8cf57b27eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148595240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af9dbadb11a1abd6d67389f127d6d0d2515ce390bb66e053d4ed3b3d6f1406`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c811d3a0ce628e18cd2102f41b09a12de94aff3009128adedaf8be05ccb652`  
		Last Modified: Thu, 25 Sep 2025 20:54:08 GMT  
		Size: 8.2 MB (8198691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e68de1e1b66fd3935b7a551b53e81eb4fa56da7ff46bb1cf59fbd3b730fcee`  
		Last Modified: Thu, 25 Sep 2025 20:54:02 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03228d3b2192185d0f7f0d910bfd3f7bd3a0fb353e0db392b1d011e42464cd51`  
		Last Modified: Thu, 25 Sep 2025 20:54:08 GMT  
		Size: 20.4 MB (20431152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b25686cbcc3e5bf0ecccbaebb8bf2649ebb74a57d8e72ecbb2e64b0df0e14`  
		Last Modified: Thu, 25 Sep 2025 20:54:08 GMT  
		Size: 22.1 MB (22129674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2dc334942f8f12c3e94dc66e8c2843da08c9aa4c21b036b7eebe6617798707`  
		Last Modified: Thu, 25 Sep 2025 20:54:10 GMT  
		Size: 21.7 MB (21656776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2699d074597016a69625082efd60eb798e2a7d48789f6742591230b17fbfaff1`  
		Last Modified: Thu, 25 Sep 2025 20:54:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a04dfb9c21fe098e1940b252c222f3f034270f3c8d3be459a3ce82e1d86d8e7`  
		Last Modified: Thu, 25 Sep 2025 20:54:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab6f3d296852ec656da72958fe4faa16d3267a06ce19580f509719968fff37f`  
		Last Modified: Thu, 25 Sep 2025 20:54:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f6850b2fa726b4577725b9f7cd8c0b70895aa16291ada5547c3ab87fd2762a`  
		Last Modified: Thu, 25 Sep 2025 21:09:58 GMT  
		Size: 9.5 MB (9502618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fd63bf11525bfd6d807edd3e5a88624b60089c4b4294b063ed440a9e73e4b2`  
		Last Modified: Thu, 25 Sep 2025 21:09:56 GMT  
		Size: 90.2 KB (90230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6981e4f36c25a35f340bf1ffaccf45d12e439a7d515be1bdefa3e0ba2f4abc1`  
		Last Modified: Thu, 25 Sep 2025 21:09:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d938082934ba4f4efbe47fbc2050ed2f3ba5d5b175d06046fc7473117cd2e495`  
		Last Modified: Thu, 25 Sep 2025 21:10:07 GMT  
		Size: 62.8 MB (62778263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c8481dab820a79bc6d6792f466a76e4bde0d5ab1c15cad6fbd7c374a21cee2`  
		Last Modified: Thu, 25 Sep 2025 21:09:56 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f4cd091cc501c56cb4053d2e0e9fc4c803abffb625ef1bcba0901e9b838eb`  
		Last Modified: Thu, 25 Sep 2025 21:09:57 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:d690cd349b9c9f3f1a300fff6aec70688768bd192ea76e8fa94bb7ffdedd56a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee1b940f73d4997c654eed20033cc3fcc2ae8f33ff38380daa5f65f6e43944b`

```dockerfile
```

-	Layers:
	-	`sha256:ee91e564e7090e136afa2e00b05406aefca08a09eb5e5255a52ca0b89fe402bf`  
		Last Modified: Thu, 25 Sep 2025 23:07:32 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b70253c35ee785053d1785f38984b9955fe3f10b5a92643d6da093db96c36345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139304419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf656b8bde82bef014ef9995b058d3f9805079d31f28396865a6cb4b1fe5ae73`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5611d52d093486823d79c9825140cf241f69f9de874ef957ea596047f55961d`  
		Last Modified: Thu, 25 Sep 2025 20:54:06 GMT  
		Size: 8.1 MB (8107716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8bd3900f8bd6b8a829b6e373613a694744e091fdf86a61c5d3396acdc14957`  
		Last Modified: Thu, 25 Sep 2025 20:53:59 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98060dd9823d51402148efb3f64f360b12ffe2775fa62c260491f5299baed7a`  
		Last Modified: Thu, 25 Sep 2025 20:54:16 GMT  
		Size: 18.4 MB (18421689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d537e93239fe7a21e8622de5dc63ad129111666e7c590a8fae5072fd699944`  
		Last Modified: Thu, 25 Sep 2025 20:54:14 GMT  
		Size: 20.7 MB (20735424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d730e9e1b0b72410d001953ffe1d672636424962fda55e43ecfb89cc428307`  
		Last Modified: Thu, 25 Sep 2025 20:54:14 GMT  
		Size: 20.4 MB (20395103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1b435c00faad2fdd72e16c48ad7e93e72c0d5de90a0889599938cbb6f572c3`  
		Last Modified: Thu, 25 Sep 2025 20:54:12 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a9acb76d900152096f6c73744c3ea1b7ed8573f9ffc5024b5a49bdb52ed92`  
		Last Modified: Thu, 25 Sep 2025 20:54:12 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311e122b96f003b5b1c9d7eeb532448f3f728889670e163b4e65f61167e1f497`  
		Last Modified: Thu, 25 Sep 2025 20:54:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4126c1eb53ef5589d6aa86eaf93aa4565159e9110de475b59e192250f4f7c50`  
		Last Modified: Thu, 25 Sep 2025 21:09:26 GMT  
		Size: 9.5 MB (9461967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec957c06517156bbdac5f6977a378128a2b774c533dac91cc0c91c84d141d510`  
		Last Modified: Thu, 25 Sep 2025 21:09:25 GMT  
		Size: 89.8 KB (89798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501dc5a6b72224a630d317f7011aec33eede1c0075ab2271d6646f15b40e4692`  
		Last Modified: Thu, 25 Sep 2025 21:09:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf0c2ecdcbfe0993eb2a8dec3593f829f7f66ed6ce6391b13a2a51d884670e`  
		Last Modified: Thu, 25 Sep 2025 21:09:30 GMT  
		Size: 58.6 MB (58583667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af79fcbb563ddd65a78180a888d18b3fc07f7014124523d7b0f0d9f8c60d7faf`  
		Last Modified: Thu, 25 Sep 2025 21:09:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31338a3a168625ff97a2cbd55031aa6f9590ec3c8b493f3ec417c3ba18fbf9c2`  
		Last Modified: Thu, 25 Sep 2025 21:09:27 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:589f0f7115f4bd9a87ccd79c33ce380674a9feab5dbd15b00a362067095ccacc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6e8bb3c0be5c782a56fa55ea7a48f1b9f572b4eb28bb34ec053e615123d864`

```dockerfile
```

-	Layers:
	-	`sha256:9be94bc6a2d635882a06c8aa50b3e1b0815cfe4cf423c3ff903d6d17d18d46ff`  
		Last Modified: Thu, 25 Sep 2025 23:07:35 GMT  
		Size: 34.8 KB (34769 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:1e39c02d6702f97843e1b66b007d50cdf6d6ffca08f9b9c69927d776a170dbc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137259792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410ac22c9b2401cee47c21689e11d370742551f3db12b24b615465fcd482485e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7867d3eaa94563cd370772487935ca8a393a405749485e0ddfa5b870be2a818f`  
		Last Modified: Thu, 25 Sep 2025 20:53:58 GMT  
		Size: 7.4 MB (7431227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c696e4e716d1f3e49e7de97fbc9f203e241a1e05e6480a86c8dee794295917f2`  
		Last Modified: Thu, 25 Sep 2025 20:53:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8c41a039de29ff497f692dba3d6c281e99ef510e059aba81041db9cd3b0be0`  
		Last Modified: Thu, 25 Sep 2025 20:54:07 GMT  
		Size: 18.4 MB (18405280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ca29476c609ea9fb0c3c91eb4a205396fd1be1cd5ff6fddf4e6ea3fc48ed23`  
		Last Modified: Thu, 25 Sep 2025 20:54:07 GMT  
		Size: 20.7 MB (20718523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8b8cda7419a690fae7d4212d1d851bef698457e63eb3a06d5adfb2fd84b21f`  
		Last Modified: Thu, 25 Sep 2025 20:54:06 GMT  
		Size: 20.4 MB (20375959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4533be9db78a2c3371974aa4343e22156ed5d05454e662399d9cc2ffd3ceb`  
		Last Modified: Thu, 25 Sep 2025 20:54:05 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1b5fd6f09ef22633c6fab4c6173d493e306144aec28193f76bb19441f0b5ee`  
		Last Modified: Thu, 25 Sep 2025 20:54:05 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da976038c4dfffea622212c64855bed5523c84cc88a22d9d3e9ae25894a91f7d`  
		Last Modified: Thu, 25 Sep 2025 20:54:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee476c1d69447bb0840ee5f28d2bd56a996de3c8ba178bb6f26040b7d7bd818`  
		Last Modified: Thu, 25 Sep 2025 21:08:15 GMT  
		Size: 8.6 MB (8603508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488c8324f45ba777a50a8c662b9e39a842db4d658116ff4d7b8d9d212e9caaf3`  
		Last Modified: Thu, 25 Sep 2025 21:08:14 GMT  
		Size: 86.2 KB (86235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185f0faa3b9924b8381093a1f6e70e82fa60174a3b9a8e514eec4958971f5023`  
		Last Modified: Thu, 25 Sep 2025 21:08:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a7f5b97b3b7c70feb1a1d350280762500ce703645eca9735d0f99375ef2dcf`  
		Last Modified: Thu, 25 Sep 2025 21:08:19 GMT  
		Size: 58.4 MB (58411865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f6c78d6a63a4d5e221cd05744049c0a58603a1bfd09a7bbcd0aa2f3bdfe1bf`  
		Last Modified: Thu, 25 Sep 2025 21:08:15 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceca909eb7117b3045e3224434acfb47fe8b40462155a8b33ebb5c12a4b96b5`  
		Last Modified: Thu, 25 Sep 2025 21:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a0cccbaab49f76cb1517166222a118b60841e687e26eb46a6c49e3d9c471959d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c676a1c042d0db2d239c76fa9426df799c6ed391efb652b84e4bd84867d59c2`

```dockerfile
```

-	Layers:
	-	`sha256:131ff2dc0a54d88eb3135d32c334e1480ee97b85754938338a77c5b71d17abf9`  
		Last Modified: Thu, 25 Sep 2025 23:07:38 GMT  
		Size: 34.8 KB (34768 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9ce547f7e7ff0e04f39dba537c1e351b98ea301d3ac15f9f20c50ef7d4cedf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139457553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7854ebbfd64a0dff14d83e4ce93f818086b510d68478506dea14214b5cb81768`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_VERSION=28.4.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.28.0
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-amd64'; 			sha256='696bc104bac3bb708eff1af3f8bbc09fda0fd88f5757c1f9b404a35117889224'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v6'; 			sha256='a61ebc09a4406b898d0ce73bc3aa7d70c5aef14b6fe46f18027e0f2ca3e9ae5c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm-v7'; 			sha256='b33d1b7ae5ce3cdae4b710bac1fae9fe101cb3862b00c8e2df424f0f2c2db285'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-arm64'; 			sha256='4e850583cc68ffd8d739ddb8a782b83f2ef9d3bf437ae7c44da4fbfde2613a8e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-ppc64le'; 			sha256='a62b15276f1956c34491f967d01cc07fa794a9fd93b7e67e066b07d018af9790'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-riscv64'; 			sha256='0136f808bab5f5e27da77236d45da5c8e62d4da019db057f495b1272a15263cf'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.28.0/buildx-v0.28.0.linux-s390x'; 			sha256='3057b70f926388e3beb88869d6d028d5893abf18a94496128ca440a80ce130ce'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Sep 2025 23:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD ["sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 03 Sep 2025 23:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 23:04:16 GMT
VOLUME [/var/lib/docker]
# Wed, 03 Sep 2025 23:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 03 Sep 2025 23:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 03 Sep 2025 23:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159de46bb8b0ef6398fe2497ebe83a93e3ecf7a2f72014fcdf50dfe4f653e39`  
		Last Modified: Thu, 25 Sep 2025 20:53:59 GMT  
		Size: 8.2 MB (8216529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b346d0d6accdd625288f88291917533d9b785a0d785dca8ad2a6b70eb55bfcc7`  
		Last Modified: Thu, 25 Sep 2025 20:53:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46eb3163d733fb404119dd6a9e0dc7a91c2dec2108fd816e7a8b8a090b136df`  
		Last Modified: Thu, 25 Sep 2025 20:54:03 GMT  
		Size: 19.2 MB (19234798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e871b083aa33f26240a80ac603199d6fff4380ef080169cbd573826778fc04c8`  
		Last Modified: Thu, 25 Sep 2025 20:54:09 GMT  
		Size: 20.2 MB (20248421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b57a444e1571edd22322a0d809a504dfe64abcda273f686ae074398fd2ce1`  
		Last Modified: Thu, 25 Sep 2025 20:54:21 GMT  
		Size: 19.8 MB (19779968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254bc2b5f41a73c5fc570d76524884781e30f0d2c4be93f2daa76cc156210d3`  
		Last Modified: Thu, 25 Sep 2025 20:54:03 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a3313a01db4e983b833e948ef912faf5f002cea3fef70d201f13eddb1bf0bf`  
		Last Modified: Thu, 25 Sep 2025 20:54:00 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e708e337697b95ff39a61eb356dc3b9a70db1dfc49464c3048e77f419bff271d`  
		Last Modified: Thu, 25 Sep 2025 20:54:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4163a6498ab8a16d41749aefe5fb6ab2c3a5ea579c3090243c00d545afc48dfa`  
		Last Modified: Thu, 25 Sep 2025 21:09:19 GMT  
		Size: 10.0 MB (10031909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0c8de5c2b9181ccad363d500683fe90e25cf70377b1a46eed39e810edad37`  
		Last Modified: Thu, 25 Sep 2025 21:09:14 GMT  
		Size: 99.3 KB (99314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93144db7d942760a159ba46afa2bd0e2a6b67bf9630b1978795b35183bcd0c00`  
		Last Modified: Thu, 25 Sep 2025 21:09:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f705109408c66af73f873bd5c73e33f1fbd3a7acb8027ac652e82f8e1c58251f`  
		Last Modified: Thu, 25 Sep 2025 21:09:17 GMT  
		Size: 57.7 MB (57707704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc9fda925f4d7a4f2fb3790c67828edc273679bb68ee2b64bf47cc481cee146`  
		Last Modified: Thu, 25 Sep 2025 21:09:14 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a12b2b56649547aa9a59ac9ca22ae055b3ca9f6da2089bad2c8945c8dab61c`  
		Last Modified: Thu, 25 Sep 2025 21:09:14 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:cf858e4afead80460d0f1a0a5f1ce13727272944bfc72b94ad902e932b049619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175cae70be5b58c21b585575e9f564afc8770309c299aa26ccc88c49755125a8`

```dockerfile
```

-	Layers:
	-	`sha256:41ad4a111eedc64148d31ddb3ebe324909e800fcc3c08e68838f45d437aea364`  
		Last Modified: Thu, 25 Sep 2025 23:07:40 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

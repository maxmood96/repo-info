## `docker:rc`

```console
$ docker pull docker@sha256:eb67d2d68a0168f1fbf198bd43334cf071eb779cd54fda774e8c7d3608b15462
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
$ docker pull docker@sha256:9f74029d0a7e4b210c2f43b64a478462648d308ded08d4931b31e23ce2cee2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130571375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99b29859a6f6fe2d2f9402c3b6d837de8def53245ef97fa73e8237f2464314a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_VERSION=27.2.0-rc.1
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 17 Aug 2024 05:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD ["sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
VOLUME [/var/lib/docker]
# Sat, 17 Aug 2024 05:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b826b4df39e8b6818aebd9eb70c4704bb0c97fc2cb464aa28510da90630351`  
		Last Modified: Mon, 19 Aug 2024 18:59:19 GMT  
		Size: 7.9 MB (7872281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ee97e7ed5f9f5b0e8abbbf4bd025bff9b040451692c8c646b6f6acc5a1270`  
		Last Modified: Mon, 19 Aug 2024 18:59:19 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb812271b283b43e9c4f2f97567fef7a516fb56c9711dfc83c2d1542037c468`  
		Last Modified: Mon, 19 Aug 2024 18:59:20 GMT  
		Size: 18.3 MB (18318205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b789603700e5b3db4e3d0433d1a05227e1bc914313dace943393a7ec2388f45`  
		Last Modified: Mon, 19 Aug 2024 18:59:20 GMT  
		Size: 18.4 MB (18404803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3295e68d9ed551c77c847e1464219797b4f10b538bd1d3ddb7845d83adf451`  
		Last Modified: Mon, 19 Aug 2024 18:59:20 GMT  
		Size: 18.8 MB (18825286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9917b18cd48d8e82e1f25127437de1b1c380fffd40cce7476361dfbdc7a73202`  
		Last Modified: Mon, 19 Aug 2024 18:59:20 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6acf233fd00d766253e3e1a75561098dd84c85485a3014718c78820e1c0db6b`  
		Last Modified: Mon, 19 Aug 2024 18:59:21 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7925fadc402ad01d5de8aaaf5e54e7255a07c6bd6a36565c4bec0eaf098f49`  
		Last Modified: Mon, 19 Aug 2024 18:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc7a4c3f0a132618da8945101f28aa00c983f1e220eaef8ce1955db8c6c17f6`  
		Last Modified: Mon, 19 Aug 2024 19:51:41 GMT  
		Size: 6.7 MB (6657655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff410ea08e469d13a338681bc58a857a91f1df4cb8b0d7a5eaf49f42b58b1189`  
		Last Modified: Mon, 19 Aug 2024 19:51:41 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926eca05e9b5ce42c69d450078fc4be1ddde7a779fb6a2d83ee1eb247f949b98`  
		Last Modified: Mon, 19 Aug 2024 19:51:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e98e1e520c556c31993a508a2803b68e7c5111ab28579e4c8c8d34edd24485`  
		Last Modified: Mon, 19 Aug 2024 19:51:43 GMT  
		Size: 56.8 MB (56773082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e2ee841e4f6cd5db0b3769603426e68bff61eac4b47d7c7786248d5483362d`  
		Last Modified: Mon, 19 Aug 2024 19:51:41 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6278100443577417d1716bbc6f10e32139f52c14dc45725b5173d08ffe76c08`  
		Last Modified: Mon, 19 Aug 2024 19:51:41 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:b75cc64b2975cda9751c235b7b03581e5da32772c60b270ae2ce783e20b26b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (34041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4042781261812ad05d85f86f43bd762f4355fa73a0becb4252b49840f49b63d8`

```dockerfile
```

-	Layers:
	-	`sha256:d7212b557a4b848e742c627cbcf3aaf89bc5072ea0ff00cac71d6e82145dcc7f`  
		Last Modified: Mon, 19 Aug 2024 19:51:41 GMT  
		Size: 34.0 KB (34041 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm variant v6

```console
$ docker pull docker@sha256:c3aced19489ec2caef25013c465e7a1b51909bb4ac5c3c97272a6dd588d14490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122793122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98014d5bd086acf15c0e6228e5f8abf10e644e8842077fc028c5b01981f276f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_VERSION=27.2.0-rc.1
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 17 Aug 2024 05:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD ["sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
VOLUME [/var/lib/docker]
# Sat, 17 Aug 2024 05:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749d51120dd4449c98cad5624e6a58aaf21f6b57355b1537b1262f69c27968e`  
		Last Modified: Tue, 13 Aug 2024 20:03:13 GMT  
		Size: 7.8 MB (7807488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dee64c722233ea05fa0db7774bbb908ccb3860c76b492b90725b4a00faf74a`  
		Last Modified: Tue, 13 Aug 2024 20:03:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cd7328f0b7553023390e36003472a46b8544f5d0208826dbfa8cea0ab75584`  
		Last Modified: Mon, 19 Aug 2024 18:59:16 GMT  
		Size: 16.6 MB (16577294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0780943347b16a7fa280637ea799b2f561ac9fa59121f4a69f346891128efc7`  
		Last Modified: Mon, 19 Aug 2024 18:59:17 GMT  
		Size: 17.1 MB (17114708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2763f449495d35e9274c80420f20fcc7f50b96788297b1d55a43ecaee92b7b9c`  
		Last Modified: Mon, 19 Aug 2024 18:59:16 GMT  
		Size: 17.8 MB (17783301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516d8517fdcc75f25abf282854de05e764bbf1b80bf3676926e4369d8659c54`  
		Last Modified: Mon, 19 Aug 2024 18:59:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f7fd32c162a1c5fa97cffdae6f51761b1f9d6a2aed1601d4a537ea19edf8ac`  
		Last Modified: Mon, 19 Aug 2024 18:59:17 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f8030f3ff465acb9510e41c77bf5362b3643c069229760a246a061b9b7d6e`  
		Last Modified: Mon, 19 Aug 2024 18:59:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6df700f9e8f1c74ccd289877fa11d66289432ab15ea43d132bc6d31fc93aa3`  
		Last Modified: Mon, 19 Aug 2024 19:51:34 GMT  
		Size: 7.0 MB (6984049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669e04c5955f5107acb67e9a495de8e87149cf80ef8b381c58abb5001cf28393`  
		Last Modified: Mon, 19 Aug 2024 19:51:34 GMT  
		Size: 88.4 KB (88404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc5bae075f73c67c8700b9890e8e968f070f88a0eb3a27702dc4407faaf3ba0`  
		Last Modified: Mon, 19 Aug 2024 19:51:34 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc383be7ef7394357c4d7c916cd6c031b68e10275f450ada6a72a777c6f34d88`  
		Last Modified: Mon, 19 Aug 2024 19:51:36 GMT  
		Size: 53.1 MB (53064730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47449ce99d37708ca2e3df8612ef7c5c8063d3be65d448bcfd7da44515556903`  
		Last Modified: Mon, 19 Aug 2024 19:51:35 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1029cdb907364d0fc6f8449cdfd3ba26602a5f718ddca9fafc19152424ae51a4`  
		Last Modified: Mon, 19 Aug 2024 19:51:35 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:6eef392c99ceaf18472848d7a973719c611af9fd365ac031ed9834e2486908ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3826315b0cf4d33b747775004af42a85381a4325a2610213bb93637ef67bc528`

```dockerfile
```

-	Layers:
	-	`sha256:0df4d99879bd57816b159a1337cffb542004fa5b08d6dd3e1ea1e0ddd8b8bc6b`  
		Last Modified: Mon, 19 Aug 2024 19:51:33 GMT  
		Size: 34.2 KB (34243 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm variant v7

```console
$ docker pull docker@sha256:4f541b5c5f10330688334c0fc8ce12026addbf6f06fd3337ed83f8508c9459bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121146463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b91a5ca9f9ec4d80cc99de6a0f5a18c9dbf036f93f6ee621048c3648f0f116a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_VERSION=27.2.0-rc.1
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 17 Aug 2024 05:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD ["sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
VOLUME [/var/lib/docker]
# Sat, 17 Aug 2024 05:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81dc9168b7d20594a7b5afa567e1b9102c0d289d4b9956af1dd0553da38503f`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 7.1 MB (7143486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b63ca62b0868cd9cbb097a6c34d9eb3a8e551918380dd69db51fbe7459654`  
		Last Modified: Wed, 14 Aug 2024 00:34:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f1562af2a6562c91262cc35beb114be291621f13dc5aab499a519ce739f84`  
		Last Modified: Mon, 19 Aug 2024 18:59:49 GMT  
		Size: 16.6 MB (16568408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1148ff59c0aecf8ad11a6649556e4ebbbb0f55214960c2bd979570197da4dda`  
		Last Modified: Mon, 19 Aug 2024 18:59:49 GMT  
		Size: 17.1 MB (17103045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853cc3993355b48834fac2182b851953466651f831a0613278ce24bb5f2e285e`  
		Last Modified: Mon, 19 Aug 2024 18:59:49 GMT  
		Size: 17.8 MB (17771127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5f7fe6a2aab4ec524ba565eda6ddee598b5920ca4c1e08bc09b9453d29e774`  
		Last Modified: Mon, 19 Aug 2024 18:59:48 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1289cc9f1f7c9201b9d3188887aef5c180dc958c1abbb54fa049d8b3cb289b4`  
		Last Modified: Mon, 19 Aug 2024 18:59:49 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fd8153d77b04c4e621f67f425474de2fa5f8fecef37392b77f46346ed9b95a`  
		Last Modified: Mon, 19 Aug 2024 18:59:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8071b757eea556abe6f577a7540f30c76499b1dccbc684d884a235d24cdbcc0`  
		Last Modified: Mon, 19 Aug 2024 19:51:29 GMT  
		Size: 6.3 MB (6308285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a167545a76af538f68d2984d15fe3237fb08359161c37404bb75034f8258f8`  
		Last Modified: Mon, 19 Aug 2024 19:51:28 GMT  
		Size: 84.5 KB (84498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac6a2f10eb1827167f0464b44f5d58740d969efa798b3b049005fe411b4e101`  
		Last Modified: Mon, 19 Aug 2024 19:51:28 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4e8531bcc2c6182140a580cd99a3b279e10a26474478d347f5802abf9058f`  
		Last Modified: Mon, 19 Aug 2024 19:51:30 GMT  
		Size: 53.1 MB (53064689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad1064e869cc80ae2c6f9dec4b3cb35bc80159beee57c470044b240d2a43f66`  
		Last Modified: Mon, 19 Aug 2024 19:51:29 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca74ed3e36eb28ffd28dc1a3d79a327e0c4b8c34c914e8c07e31abccb27df301`  
		Last Modified: Mon, 19 Aug 2024 19:51:29 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:31a85d7124b668105ea3ede4baf72c04c56127f1e15b872336e4740b77221cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aae297cf9dd27483c0ce627e313e9c9bf67b1224d22abf092845775619bc3dc`

```dockerfile
```

-	Layers:
	-	`sha256:680faa64ce63dfc5250694cc2b0e1a967e8cabb0a30ac3dcd7219ed924ba83cf`  
		Last Modified: Mon, 19 Aug 2024 19:51:27 GMT  
		Size: 34.2 KB (34242 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e15529b48ceaede2b91269d07c355e03270822b49eb640da91b8574c3e71f07d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122827773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0e3c30dfacfaf56b8fb97ec5d1abcd2a2d0d98464e507655e9b5c1775295a4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_VERSION=27.2.0-rc.1
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 17 Aug 2024 05:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD ["sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
VOLUME [/var/lib/docker]
# Sat, 17 Aug 2024 05:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD []
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19dc33df4c8f435b82bd76228e820d17db82bafa51365d6d7ca39f18b0ac35`  
		Last Modified: Mon, 19 Aug 2024 18:59:40 GMT  
		Size: 8.0 MB (7981766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc98e249bb1c68fcd6c7af4cd94d4dc840949342f303f3453b89e47b10baac`  
		Last Modified: Mon, 19 Aug 2024 18:59:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b064ad1c39cab9bbd12ce8a44da8ca317ae42aafc3a703eb68481279fac32d9`  
		Last Modified: Mon, 19 Aug 2024 18:59:40 GMT  
		Size: 17.3 MB (17264856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36074db9005cb79314791a9d04733048d5cb0703a7ac13b89c26d810045b89d`  
		Last Modified: Mon, 19 Aug 2024 18:59:40 GMT  
		Size: 16.8 MB (16772961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb8b806a016e2bd5e83e137c7787981575ad2ce863d92ce07cee3fc38544c78`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764856852ab1b254b572502db9ed0d8fd601e8e615ae83ba73c5a1e5b592c9ab`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d43f3808e72acbc083572802b4b53a88aa4088c8e2d99825cef40e03c050fd`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12ab67b46ae8edc30d74e102545f60cf7042a2542f02c2b8e7f0a313592f473`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae5fb6ccf4a163f82c494b7b9caf3dd9ad4b865c7923f99e1b9d969dbfbe31`  
		Last Modified: Mon, 19 Aug 2024 19:51:28 GMT  
		Size: 7.0 MB (7034951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9747f9655f8f5a18e1f04c84474e64bf4af06cf9a3b0940811d176fb15124d`  
		Last Modified: Mon, 19 Aug 2024 19:51:28 GMT  
		Size: 98.7 KB (98658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30194908ca2a1d60bacf29c1b2422f4f74e8a5587571fe332a8d909021338c6f`  
		Last Modified: Mon, 19 Aug 2024 19:51:28 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60aee437e11c55a81b75f98d77183616292c4270cd75685ecd019c60661872cb`  
		Last Modified: Mon, 19 Aug 2024 19:51:30 GMT  
		Size: 52.4 MB (52392865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5637ce5921a2d301d958f3e970b359747e220bd4ff8b77d743b67cf35348c91`  
		Last Modified: Mon, 19 Aug 2024 19:51:29 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32651485ff3e08e71cc5b9afa52a8300e9f416bcb44a26e9559b887f4ff0a985`  
		Last Modified: Mon, 19 Aug 2024 19:51:29 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:b176e0d5eccc436258c1c85856acc69494c36a796fddc49d3fa21859266835e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc90e8e238a58420cb0e416d3c89f1656a37d053ce86489729f8f0571a52c1ec`

```dockerfile
```

-	Layers:
	-	`sha256:1f458647e36ba103b2638e53013e11e8d28f2aef4f9444de561090e6d68b1f80`  
		Last Modified: Mon, 19 Aug 2024 19:51:28 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

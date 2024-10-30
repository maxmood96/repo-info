## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:d7f70287009a765ce9728d09ae0e1ef10ba2451ee7711298a3937da22dd1be5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:97316936aeccbcfae31c3ee8c744d6517a12ee5278ac04728221b7e239291fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156881916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b77c63afb3f34de27d291e46c605e0bd7afcd078b2e94c5d7e987b573ba2e79`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7c1b27cb672d81ee0e4513235c74e879beb8a1f41f90268f660474d36731c`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 981.6 KB (981576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b81f22ddfe7fe47f5e6cc0d8b061586e9bfb03d6a0f9a72919fb92e33cd59ee`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ceb4b6852f66befe9b5f8c95412a41876132a80328dbdabbd31e81824ad0fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef05fd523513dfcd7ea96faec1283dcd08014ade10ca9180907f4dd5337c774b`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 21.3 MB (21303265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc448d15ea248565c3b89094a50084e2f3eded7d9e10e06475223eb1af7a88`  
		Last Modified: Wed, 30 Oct 2024 00:47:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a071ebd27917f7d76a4782c16e2ee0c723cc0317334b4d40159700599dd079b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be0ed03e7637322aed785abe25aea41b8ebd0c9eac3dd6cd2682ea08d2d40a1`

```dockerfile
```

-	Layers:
	-	`sha256:ce55096dbabb40d46c9d04d1608c3f83e5f81604737859d3977b34896e8ae345`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:df2018bf77ef9956bea679d229e86a0869408918e0c30acbc4557dd6f80054f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151462614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523b102871ed5328ab73a83b6c7007ebe05f5c35c50847019b01818de3303040`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f11fb7c9a7e46e95a9874adf87e8bafd06bb374be2c74d9ccb4622770585fb`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 1.0 MB (1023842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2211e328766d831433385aa9924c089cb0c332a4ed3171aacd3a97de972d5053`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f743305622d792bd249ad20ffdcebea86c516bb417c4a66762aaacc3f242638`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73a168fb4569ec560dd604ca7e06e9a599446e1ebab8434667345f29399fbd6`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 23.2 MB (23155431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318a4093bafc2dc1e678e46e5fd0d9b285777696e0d2be28d06cfe1521a5bdc`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:24d9a91db2e3210efb574de176582c85aecc21e44e45d2eaf780eb384d5f94ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f318787d6f843598fedc7cbfd1b4352e791d42d9506c520cc3af7c1cd448e45`

```dockerfile
```

-	Layers:
	-	`sha256:cb7f847a2eece9d610a02c1a0b9b474079c6f67184588b56f7f3dccbb52bf331`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

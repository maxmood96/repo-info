## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:c6ad06a7997c767d8277292f7c7d73a5d32d430513c89e0ff988b98e286042b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3fd75b0a30c363dc98fa630f87a07acb84ff15a5716f9734f9cc33a94918dc0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155735922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee1c8d83f59c65ac8fa960f4793b958aa2a7b2791d5098b45fa96935093a0d4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d185366bdae3ff1be746691465de29a0e0b2f3e04f28b39180d9375234c91e73`  
		Last Modified: Wed, 08 Jan 2025 17:58:05 GMT  
		Size: 8.1 MB (8058731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5707d5cc11f48c4f3654fab4e9bb2d5d3c8cb71106dd2e58fec35df2b147afb4`  
		Last Modified: Wed, 08 Jan 2025 17:58:05 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089f82d81010cbc4aa96ca98767cc6be68fa0c12bdff13b1ce3fbbbf01f30718`  
		Last Modified: Wed, 08 Jan 2025 17:58:06 GMT  
		Size: 18.7 MB (18669943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffe0aee10ea77c7f0546febfae38a67b69cd1b96736c3e3f8033fee03e1cda7`  
		Last Modified: Wed, 08 Jan 2025 17:58:06 GMT  
		Size: 18.8 MB (18798856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fe673a5ecb77d234d78523d7959f55e887124ffa9ec541309b34336d237520`  
		Last Modified: Wed, 08 Jan 2025 17:58:06 GMT  
		Size: 19.3 MB (19295647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9a9d0c2d0f87990929701ed18006a4ae011dffcb2da0e01d66319135edbb60`  
		Last Modified: Wed, 08 Jan 2025 17:58:06 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc4b63b8b868cb525ebf3a8cae998e0f83daa0250882e0933778897af5cf8ec`  
		Last Modified: Wed, 08 Jan 2025 17:58:07 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdaf163319a658d74a3a98948f1da42cb54f7b0928587abb65b927ad17893e2`  
		Last Modified: Wed, 08 Jan 2025 17:58:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756a2c581c468f113a248bc7adbe1e630723a1760c5bb4ab9b13c225e82bb2b`  
		Last Modified: Wed, 08 Jan 2025 18:22:52 GMT  
		Size: 6.7 MB (6733468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec5c56e7fe13330e1f9b541b35fe33ba41e559420861194fae2ebd2f2f2459b`  
		Last Modified: Wed, 08 Jan 2025 18:22:51 GMT  
		Size: 89.4 KB (89423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0555c3256b7f22c04ad73298910414cae8b436881fc7508e0f0c28962a83fe4`  
		Last Modified: Wed, 08 Jan 2025 18:22:51 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fff1b95f59b97251721540feaca82be3748dfdfa344d8bb049ec157e0bdc12f`  
		Last Modified: Wed, 08 Jan 2025 18:22:53 GMT  
		Size: 58.1 MB (58148414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009ef296d7804aa8f4c2dc64be241f52ce15946ae35f98fa2f490a62ebb37f7c`  
		Last Modified: Wed, 08 Jan 2025 18:22:53 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e23c377a3501a615c52cae3b2b860cc8a06e73006a82f10a25b33da0ac1decc`  
		Last Modified: Wed, 08 Jan 2025 18:22:52 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c58ce0e7c776a3fae576e07dde1e8d303597e1f1a2b8dffaa4461ea120477b0`  
		Last Modified: Wed, 08 Jan 2025 19:14:19 GMT  
		Size: 986.6 KB (986566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a81451b8fc6dbd100ca8a9caf379d931b85807bdae5473aad0fc13cd401bffb`  
		Last Modified: Wed, 08 Jan 2025 19:14:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9057671b324358b0fbab312615ab7c9eee791713490dab1ba3e599bc0fa6b37`  
		Last Modified: Wed, 08 Jan 2025 19:14:19 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e439f2c22182c554f43821b6536d76af8d017b3c824ebede63754adce470cdae`  
		Last Modified: Wed, 08 Jan 2025 19:14:20 GMT  
		Size: 21.3 MB (21303863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b086215de7f48cd3da80a82acbe87676fef0da7072e46127f95c8afa21595574`  
		Last Modified: Wed, 08 Jan 2025 19:14:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a08116cfb2bb4820d45dc283f262f6985d4ca9341019cf7445c8fdf0a6a9dfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303d3fe684b36138fa70a8e9dd85405a297415b2e56375919e36699ba4694c12`

```dockerfile
```

-	Layers:
	-	`sha256:92bb06ef4406939bcc4e4d878df9cb9c9ec12799a873c69c71f9093e21acf634`  
		Last Modified: Wed, 08 Jan 2025 19:14:19 GMT  
		Size: 30.6 KB (30617 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8c7e0916c0c6b768453a98086a3092c15a5a189f8a984898765e717037dc496d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149429747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d0d33f0c88170851c53637b875731d33099303864ade44a65ad2551f2bbc1e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-x86_64'; 			sha256='ec81c40f138db0ca3aee71c2fffb0075636bea5a02109c75177f66e1b8f568b9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv6'; 			sha256='a570825379639804e406c07fe73d052e7909e74c976c3a5cc6cad74a871e405d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-armv7'; 			sha256='bd6a7456eb94e3bb7df31be43f84af9882149abe417f5b7a2635108325e7e604'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-aarch64'; 			sha256='7aa6406406be13c075e92cfbf322470318a9ad7a58c93a9fb3a215dc14aed8bd'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-ppc64le'; 			sha256='4e56b1e8f5d5e68ce66d5a156a96597b1d7534a94dd2d846d288797008e044eb'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-riscv64'; 			sha256='686bba58b9c2cad3edc4045dadb36ed2e2d4b0b72ada8eed832b6a9561fdb50d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.1/docker-compose-linux-s390x'; 			sha256='a40fdae1e4a3b90186bc06712b0b19079877bf408f39b3425bf65048e19bd8aa'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
USER rootless
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd118a02a977501603a666f0534bd4e65d18527588ad5cf400f8c10d29b641a2`  
		Last Modified: Wed, 08 Jan 2025 18:21:52 GMT  
		Size: 8.1 MB (8073087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7344f9e39163b0db1d8cc353b60bb1b0f4a1f5bce6103ce319dc4b80767896`  
		Last Modified: Wed, 08 Jan 2025 18:21:51 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b491da4fa6243026056cc314d938e03599e8dff13f8ac4ff1e5ce0c0bb73c2f`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 17.6 MB (17619414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a0e3aeeec1250aebfa402c0a741416452445d234a867eea35c8c68d19e3c55`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 17.1 MB (17106452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266bf3da8cdc43561b0a4d0e777fff32d6ee6ae16c3a43853b2df21faef62d4e`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 17.6 MB (17642742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b6b0d0e0d21087323094118ec8bbd6ef16965f2436eb105dc930706616ac3c`  
		Last Modified: Wed, 08 Jan 2025 18:22:21 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d0cdcc6385756fabdd902e9c6d48c1f6f8b12bc391af806d11f26476c05183`  
		Last Modified: Wed, 08 Jan 2025 18:22:22 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b883d10753dcfa1efd6a93df081b0ad43dda8c499d48cea04b2cdf24b57cd0c`  
		Last Modified: Wed, 08 Jan 2025 18:22:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839c4567b4fadaafe269111971bd070bf927bd05b7c4317ef220070bddaf8a73`  
		Last Modified: Thu, 09 Jan 2025 06:32:37 GMT  
		Size: 7.0 MB (6981985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9f9768093bd8f950696dba4bbd2e22dc0d35029e93fbbd530aca0ea004c8bc`  
		Last Modified: Thu, 09 Jan 2025 06:32:36 GMT  
		Size: 97.8 KB (97781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5990f111e5a2afba886f027209872336087338a35a44c474bc529aed59851e5`  
		Last Modified: Thu, 09 Jan 2025 06:32:36 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad736c785dc361d394d1824339c7d7eae3787f6f59ff9e1a4700893eda9df21`  
		Last Modified: Thu, 09 Jan 2025 06:32:38 GMT  
		Size: 53.7 MB (53737272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23d1e55cdc236695e744261b5fe3c1a2a00371a70c2fcc78039926935becfcd`  
		Last Modified: Thu, 09 Jan 2025 06:32:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f71d493ae8331570a70ddc29f6a433b4e42f37715dce1fdbb55475ec0032f8c`  
		Last Modified: Thu, 09 Jan 2025 06:32:37 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831eab62af659e47c0fbc7d98d8821563fda5fc18b1f19734a2b0b04cc117b1`  
		Last Modified: Thu, 09 Jan 2025 08:49:45 GMT  
		Size: 1.0 MB (1014209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4d7ff7023380e03997147fc801837cb20084b292e98d51b3b113cb5c231ff2`  
		Last Modified: Thu, 09 Jan 2025 08:49:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98629d3683a1248486388db1219173b27839ccedf69e426d8135e664f9ff719`  
		Last Modified: Thu, 09 Jan 2025 08:49:44 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea801a77bc1a8e2ebaf0b27901f6249e8468cc4a18a9561f407a6e6b57e49cf`  
		Last Modified: Thu, 09 Jan 2025 08:49:45 GMT  
		Size: 23.2 MB (23155146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6617fa2b70fc8d033c1e1322db989bcae377fd35ba9aeea14c9a8e7fffdcae3f`  
		Last Modified: Thu, 09 Jan 2025 08:49:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9501b32f192f914fd2da6e1b5815c07c06f60d075f986e9aca9112c896936cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607cea8077735632eeb079da338b7e18d855a76e6a3b61daadc7fd502783ff30`

```dockerfile
```

-	Layers:
	-	`sha256:4810e1205679520781b0349a6281cf7fefad41fb4806e9d2d15167f7191baee6`  
		Last Modified: Thu, 09 Jan 2025 08:49:44 GMT  
		Size: 30.8 KB (30787 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:8fc8c7e252d63e2280415a0520caf2a014c86b5c8fd25c910fe8adc77aeb94ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:abd2dd1debd13881cb395d987a48ef2db49e904f9260e691cdd8fb3f40c8c810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162261128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515c53634a6d629377edd34a1fa5f3f6977b9ff51a6afb4aa84a220a5f27d5c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 30 May 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD []
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 May 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99164a65e1f060513df17430a291c788a5801cc0364c3cf0abaf9dd47e9d891c`  
		Last Modified: Thu, 05 Jun 2025 22:44:25 GMT  
		Size: 8.2 MB (8207469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a930b44823eb85c484514670f94fa0fadf7649aa34a692072e953b86cff998`  
		Last Modified: Thu, 05 Jun 2025 22:44:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fad9bfb8f24abcb392b00c918762036dedf67787dc8a32b43aec570f3557f4`  
		Last Modified: Thu, 05 Jun 2025 22:44:28 GMT  
		Size: 20.1 MB (20083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e993a5c36c8c13b622945142edd4bdf6b5d03775d8e91196856e50e0512650a`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.3 MB (21290182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58cf00359048abfc4f447feefe1373db7fd84dfe136fb751689b640844dd4b`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 21.1 MB (21092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd9fc81ec33be8d5693955225a870888bf988fe35871af701d05810a7718b9`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc70da6730815a90c517d43ed51312bc13932b65a288bbb8952f74df9d763a`  
		Last Modified: Thu, 05 Jun 2025 22:44:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2483cd3bb024143d65a844f930ffb5aa01cb0932a660abcaa0fcd68ddc0810`  
		Last Modified: Thu, 05 Jun 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232671b8d6c574d91a514e1073ddb00bd37e47ba17cfeefc0a4e078e392e4a00`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 6.9 MB (6905563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947c15ddd39c2ad279e9f5b5180a071aa948c04d248e2dcf4cb13585d9b47b8`  
		Last Modified: Thu, 05 Jun 2025 23:10:12 GMT  
		Size: 90.5 KB (90492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e4c6039fec8c4db67902febab1ae735352d758ffb76367f1e3e68a0b04b9d`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369f3cb80e373dbeee03da49ca69ce93f7c63f165704f929f0a040a4de56ed8e`  
		Last Modified: Thu, 05 Jun 2025 23:10:16 GMT  
		Size: 62.2 MB (62206624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a0f373a71bb7b7e7a3be4baa2472d2850c4c9549c66b58e70a59a51b696ee`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbe5b0725a180af25ab3d235ff1a32980b060cb2e263d0362d2baa5b73d858`  
		Last Modified: Thu, 05 Jun 2025 23:10:11 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64aa3fd56b6d8303e9c2e032693fa69765ebe0ca402c8652e2e4be4bd9b8a2f`  
		Last Modified: Fri, 06 Jun 2025 00:13:41 GMT  
		Size: 993.3 KB (993270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ac68c4bd4a09936531af4a567ee2065e73f798766ad456aef07aa86555af1`  
		Last Modified: Fri, 06 Jun 2025 00:13:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e79fe881b6f2ad1dc6bfdf95095a21b2a9400b5098d82da1be17d678d59226`  
		Last Modified: Fri, 06 Jun 2025 00:13:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91260bbdd96570e120d536ac928e3f77c4f858234e17f2ba9abb34a416109116`  
		Last Modified: Fri, 06 Jun 2025 02:08:01 GMT  
		Size: 17.6 MB (17585969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e31b397060352f80943b2c245dfb2b9014d8caaaefa979cba711e233412315`  
		Last Modified: Fri, 06 Jun 2025 00:13:54 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0c4804528defa4555b2fadbd0044e12d0585c45979692580e6f2793f2e1eea66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33f1746b3d799c576bbbfea37de0b6f65df618daea063dddc5c07da8dfdd129`

```dockerfile
```

-	Layers:
	-	`sha256:4faecdc253478ec516ca521def628c3524f48440edfd20522bf779744323317c`  
		Last Modified: Fri, 06 Jun 2025 02:07:42 GMT  
		Size: 30.4 KB (30450 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8f8a0cd4395a6ab286a0630f776e920239e6a01f6de484c2c23292ef76381bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153539458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63acc824e3021e35e0fbed5808986ced5616f6da68905d273709d210e4a8ade6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-amd64'; 			sha256='c41ed17ec05b6ebb50eeb02fb26cce90f16cd260b8d26ce73963428c6b2d6508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v6'; 			sha256='591abb51afe942814a45f4f3d0f1a97fe8c5c212142bded66025ae019136bac8'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm-v7'; 			sha256='69a3afa3d22867ea67b87e5f205574478e7a795599c471b61575bacf455452ae'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-arm64'; 			sha256='ad33819d085a635e3b4400a412bd2b4e943bfbc830366d78f50579bae48f8053'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-ppc64le'; 			sha256='90c02625d1e52abd8e6089854208963651ea727028aaca58b29847dc594c01f8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-riscv64'; 			sha256='3031cf533e015ea77425446e4bc87173f1316447ed3369c2898f73ac353de404'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.linux-s390x'; 			sha256='821ea62254a7be6cab51c5ebefc9ba74b7e2dd902c78d16b268850dc29869ca2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-x86_64'; 			sha256='e6e471b1e7bf0443592d3987dea6073f08db3e48ba0580199109aa7a44257e54'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv6'; 			sha256='f09294bd81119701f051733b45be487d55faa29d20fb9c54412975a6c7fd8696'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-armv7'; 			sha256='b1b592889f15f50ddc77685ed499c69599117e52240b196447cb82821da3f7f8'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-aarch64'; 			sha256='664e8c532ac0dd54d14af4eb3fe4edce86ce27d970ec832a96b55bc2ef1dffdf'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-ppc64le'; 			sha256='83c7cf5afffcc7944e23ba5c1c038aff4f2d760f08681d76b5271b66c9e2af5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-riscv64'; 			sha256='0e6047d2b0f745f0bbb13d707cfb945295bf45e397e67ff756f8551043a1f5bc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.0/docker-compose-linux-s390x'; 			sha256='381b5b77e6a91075e746167ac160062a1adf4d2a1121e433f1ca731ad08e2353'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 30 May 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD []
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 May 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a584a1da307e1ac31b3fd852369ae8a8176a1baa2e783b7e72077d8318364`  
		Last Modified: Thu, 05 Jun 2025 23:07:15 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122792206f35c9e929c0c28c585fd195a84012e2d9bea1522c579660e013f3a5`  
		Last Modified: Thu, 05 Jun 2025 22:50:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5a5c767d7cf27a922e7c99956942414d9e65453df45e3500e05adf80db19d`  
		Last Modified: Thu, 05 Jun 2025 23:07:16 GMT  
		Size: 18.9 MB (18902608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc5aa8a4cd07adf8f84bd323a5d415f9ca2c5c158b74f9382a0b369265fe2`  
		Last Modified: Thu, 05 Jun 2025 23:07:14 GMT  
		Size: 19.5 MB (19469838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba639502cad797b5554e57bbdc209e0c34366d2a40e0b51a2fa20dfce1a5b337`  
		Last Modified: Thu, 05 Jun 2025 23:07:13 GMT  
		Size: 19.3 MB (19344051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0f9c86634c1a6b9059d179ed7e6ead432e9b8bcddfb0e980660053ccaef13`  
		Last Modified: Thu, 05 Jun 2025 22:50:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef143fe66bfdc5598981ca016d8e3884fde63a7858eb245932bb9745217e515a`  
		Last Modified: Thu, 05 Jun 2025 22:50:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e2c1a5fdbb4dad365dd880c4621563cfe56068eb2e2541c0de0b1de1353676`  
		Last Modified: Thu, 05 Jun 2025 22:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81c7606e8dcfe2fd4ea847b572c410188a1a61c1b7b1cda6ba28a64e97f159`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 7.1 MB (7141567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3f3d3d88e3f3363a8a38c1a676767483806a513d0552d4772a08e36257b1c`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abefbbf9a5b4d4cca3ef794fb554ab4acac7277079ebf9e0403cc7bb13360683`  
		Last Modified: Thu, 05 Jun 2025 23:08:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15537da54888f9d1dd7c82127a2affc9eaa21eec06bc9938606f42434884b95d`  
		Last Modified: Thu, 05 Jun 2025 23:08:12 GMT  
		Size: 57.2 MB (57168179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5eff1498a195bfe23aea7da2bcdf6de5f313f4140c8715a32acf14d62d62cd`  
		Last Modified: Thu, 05 Jun 2025 23:08:04 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4cb7df5229fcce96acdc6de42d98aa670436a784a0e59417a1584407b6bb8`  
		Last Modified: Thu, 05 Jun 2025 23:08:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b640b4b96d1a9d3b71ca7172efbfc7644661ed859290a1ef70f6efb5ae8646b6`  
		Last Modified: Thu, 05 Jun 2025 23:10:53 GMT  
		Size: 1.0 MB (1022994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3954fdd9c5b6656129957c10bf87d54fb3f5abd93ddb09065d380cb210a5077`  
		Last Modified: Thu, 05 Jun 2025 23:10:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4258e800a40d5a0144bf5289d6469124b4dcd57aa4a07ebfe0b4d51a68c8176e`  
		Last Modified: Thu, 05 Jun 2025 23:10:54 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603a03c83db0af7bcffad6809d5df5087ed7fc636e484590aa7baf42f257b2f2`  
		Last Modified: Thu, 05 Jun 2025 23:10:56 GMT  
		Size: 18.0 MB (18016150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ced063cb74820e91a874efbb44b00db32b5453e8cf96c0082bfe9265f119ad2`  
		Last Modified: Thu, 05 Jun 2025 23:14:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:84c0fd5fb3a3c2479438611da949f104f724c986c93c76c12541d88382d56a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2929db2e0b226bded3985c6262f564307858288cba598d29b2ed0fa3c11f193`

```dockerfile
```

-	Layers:
	-	`sha256:fb773e2f1f91681ce7adadf4bf3c53895f7c309689fbb9874a70b1ce0fc12347`  
		Last Modified: Fri, 06 Jun 2025 02:07:46 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

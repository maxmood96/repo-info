## `docker:dind-rootless`

```console
$ docker pull docker@sha256:eeb43ad630a5165c910f03041a590147ddb1c2632be3a3c397e9b2c2b4efa7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:b3d53c924e34d7e003f601d8d6222844b9c1b71b7aa0b2ed4655a6b30fe32602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169675916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78479fdc55be9d0c2772a94ab8b66e905f686b58a754da0f12cd11b4ba460167`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.5.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-amd64'; 			sha256='d02d47061bede1b90d34bf6562a5f39e686773e97cf9d00e7114b3c1e269e524'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v6'; 			sha256='7a90b222d33f2b70540ac9fa0d2d7feff02accb83a22c557c78f2ad924807ed5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v7'; 			sha256='4af7949022b2f5228990d7b9faab5cea8ac93edc6faf284d115fa33bbb367778'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm64'; 			sha256='14e50940aef67c4b46f6b03a5ccc3851a30f883e751a61048a4bc80b8832a840'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-ppc64le'; 			sha256='eaaa77de28c79306be25ad992a1fbd537113bc3543ccac2a3e2e1855a752a665'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-riscv64'; 			sha256='16fcd25ec8ca6f15d6264133c3dc93cdce211fb2028b8cb529c0ea7b880c3818'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-s390x'; 			sha256='dec5db787903debb0f83012a416421e4119d7f28837ae7aa6ae5b689750285fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD ["sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD []
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f4121261305cd808f866e5cc468c62c7b691048458ce84c73cebc8744a0f5c`  
		Last Modified: Fri, 03 Oct 2025 15:42:57 GMT  
		Size: 8.2 MB (8206013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacb763c34fa98faf157ad30ac845055c7e17d6bc356a735dd34979b2ca3dcd`  
		Last Modified: Fri, 03 Oct 2025 15:42:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82baaa61b0bd5e833b9bf0dce2a5ba042e651d1dae98dcecd76a54d85245f705`  
		Last Modified: Fri, 03 Oct 2025 15:43:00 GMT  
		Size: 20.4 MB (20429721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c233148e55acfe21ab7559acf33645c62cab15c2786fb755b117d0f761692214`  
		Last Modified: Fri, 03 Oct 2025 15:43:04 GMT  
		Size: 22.2 MB (22158310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a01365128829f855670516e240e079aaa07cca78da2106a03fe8cc88723c3c6`  
		Last Modified: Fri, 03 Oct 2025 15:43:10 GMT  
		Size: 21.7 MB (21656766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d97b7b769f0ef0ffff5fb8721b8852aab640d625cccad858457c7ccdc01909`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c252ca38c80c99c59f88eb9177337a5d1e1be51a71bca74077ce10d0e2db2ff6`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f710bb1cc914e30eac705c8d79e2b6fac559197d538c0a843bfdd992a69bfe1`  
		Last Modified: Fri, 03 Oct 2025 15:42:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bd32a0ea96da36ee694f909a448f72d9ce8f3161366150204ce43f92f3ef25`  
		Last Modified: Fri, 03 Oct 2025 16:55:35 GMT  
		Size: 9.5 MB (9507812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b78db0b14600437995bb4b41a16d542cc1c29e47d131a154fcd0e71e1240e7`  
		Last Modified: Fri, 03 Oct 2025 16:33:46 GMT  
		Size: 90.4 KB (90414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02844b1b965c7106b174fa8fcc81da5932ae550f52b2cdea2f4b1cbc72cf9103`  
		Last Modified: Fri, 03 Oct 2025 16:33:51 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c0d4f3fc3deda7540f99bf89eb4616d8fe2bf6fde04101d3c62817b55b32ed`  
		Last Modified: Fri, 03 Oct 2025 16:55:36 GMT  
		Size: 62.8 MB (62827332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2b4197469badf8d75becb38e327e689d7b466f9a06cbf2e22c1574489684fc`  
		Last Modified: Fri, 03 Oct 2025 16:33:54 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733f9fcc3eeee9d72d8b472b1225e3228f39f1cefe71d8dff9f1a2c710decce`  
		Last Modified: Fri, 03 Oct 2025 16:33:57 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac14d1bbef2a00ee6148a84da6d122959f4469478e896e6b0238d37228c12e58`  
		Last Modified: Fri, 03 Oct 2025 16:56:10 GMT  
		Size: 3.4 MB (3398331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a4cba6aa490126672884ec1cc7fc81c87c39f7a7b752a3a27031de81cc7e66`  
		Last Modified: Fri, 03 Oct 2025 16:56:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3068b13530be21c371198cff4b2617ff2f7bf794a5ff5f9daf01addd778aa4b0`  
		Last Modified: Fri, 03 Oct 2025 16:56:10 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aed80e8577ba3b89d9e8425fc00a705532e626ca3fc051bad538409c0399762`  
		Last Modified: Fri, 03 Oct 2025 16:56:14 GMT  
		Size: 17.6 MB (17592032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069ff56a1905eb0680d22ee4587a1a1ba638f709814aca49b750b3c4bf3531f6`  
		Last Modified: Fri, 03 Oct 2025 16:56:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:93a89793da5adcc19ef3c9827d45c6ecb2767c1a1585dc874a34e2e3565f084f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119379607dbb4d2e6842aa149d585b6259e03e4b136a8b29a877d1fd94e7a05f`

```dockerfile
```

-	Layers:
	-	`sha256:91562a8e6c08e44f1300395f13fbf8c2f9e8521ccc3a5a2685e8553f477b409e`  
		Last Modified: Fri, 03 Oct 2025 17:07:59 GMT  
		Size: 30.6 KB (30636 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:96a3c2358a11eb6c0b8b8697af03c763b040a4289d5cdb41afce7cccfdc6a7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160960944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09fc28f780b87f424eac4f8d8e1a3e2f8b076509e298aa9f1c3af3ce13c6945`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.5.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-amd64'; 			sha256='d02d47061bede1b90d34bf6562a5f39e686773e97cf9d00e7114b3c1e269e524'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v6'; 			sha256='7a90b222d33f2b70540ac9fa0d2d7feff02accb83a22c557c78f2ad924807ed5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm-v7'; 			sha256='4af7949022b2f5228990d7b9faab5cea8ac93edc6faf284d115fa33bbb367778'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-arm64'; 			sha256='14e50940aef67c4b46f6b03a5ccc3851a30f883e751a61048a4bc80b8832a840'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-ppc64le'; 			sha256='eaaa77de28c79306be25ad992a1fbd537113bc3543ccac2a3e2e1855a752a665'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-riscv64'; 			sha256='16fcd25ec8ca6f15d6264133c3dc93cdce211fb2028b8cb529c0ea7b880c3818'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.linux-s390x'; 			sha256='dec5db787903debb0f83012a416421e4119d7f28837ae7aa6ae5b689750285fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-x86_64'; 			sha256='7af95166a730b87e172d4fc9aefea8725d3c6c7327d59149267b452114ddb7d4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv6'; 			sha256='e376f677087bc5d85a19d24765fea400f88de2d18577dab0dd746961fcfe8804'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-armv7'; 			sha256='c0d6fe1d2e1e3e8490804ef092793f3c0368c4458d0fcb86a7df8670a9d8ae78'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-aarch64'; 			sha256='49082844b87f03cdcd5f5bbef1ba8c9c897b7a2dfb80cea18d61ec8ca6117e0c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-ppc64le'; 			sha256='a731c350b577926b11b986d1e54e2332bdef3647c55c90931000ad9e8434d0cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-riscv64'; 			sha256='a7081ade7067a5486a81514d50adec82337e14cdcea5f2127edd6e45905fc0fa'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-linux-s390x'; 			sha256='4e32f5c43ffe7564d9a39f78d502fbdc17904e1b62add9c7939ec3bbd6de1af9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD ["sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 02 Oct 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 02 Oct 2025 23:04:15 GMT
CMD []
# Thu, 02 Oct 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 02 Oct 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 02 Oct 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befee8c2b0ad40f8afec285692dd9de306244ab77849362b32f364598f4dd856`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 8.2 MB (8227655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81db965703fb492a9487f0707728f846ca5016cffbe4cca14a9aaedf3fe47be`  
		Last Modified: Fri, 03 Oct 2025 16:10:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae023da43925318e9d906c7752c90968e4e76401eff1a13c13a02dfad260775`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 19.2 MB (19238158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d084ed095dcaaa56e75d1464d58172ca160961091fd6c2110b81301c1c8d144a`  
		Last Modified: Fri, 03 Oct 2025 16:10:12 GMT  
		Size: 20.3 MB (20274240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5cbf3334db63fb72ebb37340a3158221d6151607e4b01c5be6b44f4c2a1f35`  
		Last Modified: Fri, 03 Oct 2025 16:10:10 GMT  
		Size: 19.8 MB (19779981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a37c322750556c7e8922a42c05e513ce640dbe5059b406843b4285c15f28be`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ee98d68b79d3a825b7c3d7d4492c505cae7e7ee829b8da41259b5372f704be`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06880fc24b1d74868cf537077a0bd0cc09b9cb315d6f2e5ba9ae3fe57405085f`  
		Last Modified: Fri, 03 Oct 2025 16:10:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e663db0fdfaf3e5f40f7c3d7c3d51cfa62bbe43ddfcb4fe99cb8b6c637f6aa`  
		Last Modified: Fri, 03 Oct 2025 16:11:02 GMT  
		Size: 10.0 MB (10032639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5e31e2508033fa71a6e9c996b28c63fb8717b1fb04950cc9bf8ab9c496715c`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 99.6 KB (99551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44d97f98752505c225f3d7bf9a163d9522bb8c15f839dde10ca592bec612151`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db3a1adaf72d283f41dd82a794dd8a21401cf97b9547986d552142a747eb5ae`  
		Last Modified: Fri, 03 Oct 2025 16:11:06 GMT  
		Size: 57.8 MB (57759208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0ea7e65ba6a9a348e2c362f6ee2128c9cbbc4fe766157fac25a52324ef2e0c`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8003cd90da085be86d46c270b3ffed416d670d6fb46dc211845eaad27c21794`  
		Last Modified: Fri, 03 Oct 2025 16:11:00 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210fc14d10dd6889f85a6c0dda51131547e11a4b09c342a41f267e3b05025bb`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 3.4 MB (3389873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650ea26cdb1e4676d6bce162d7e5a937b93e2705cc86380b54dd03d1e8b1abd3`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5728e12ff2b23e1c18b5c20970862362841a7011baa80aef4a45d5a1b108115`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30951d5b864c3c60fe2adf5433ff9e1d915fc52fdd40fae1766a1948ac8ef345`  
		Last Modified: Fri, 03 Oct 2025 17:08:19 GMT  
		Size: 18.0 MB (18019399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056d88955c46abf8014f4e3163803203a97c96513ab2783aee987fd1cc078700`  
		Last Modified: Fri, 03 Oct 2025 17:08:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4025f450b00c6226d6682f17fbdaa8ff0aca575e36b82377be3680a70b1008ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd180d64e35b20ae847a8335cd5554d37b68ed547c4530d96e617dd92f1a9a0`

```dockerfile
```

-	Layers:
	-	`sha256:e94643b935420367d72f27be406ef5a64f8862ab497d1cb7c6291454821ec49c`  
		Last Modified: Fri, 03 Oct 2025 17:08:03 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

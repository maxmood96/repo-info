## `docker:dind`

```console
$ docker pull docker@sha256:c090c93b63bc690570a0cab398904c855a46f08e0b6804e51bb5ad26e3407f9a
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
$ docker pull docker@sha256:65225ff17745723684af9877ae9dddbe41f16246ec27df7844bb5e1f8b448e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148684215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fcc7c017f93c90eb877637eec77bab54feee6b8e16a5b92674fa73cac78739`
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

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:4b130afc50f0712d1601d5dbfd68f88c03253aaa79cf89ee5677e58b91eb4938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ae93cb82bd2326d3e9aa7dbd8a0b1e33a25b33184a53142a82499aff09420b`

```dockerfile
```

-	Layers:
	-	`sha256:257184b172509ed95babb35a55fcacbb032c196e2f5d4d175e4086bf0de2f815`  
		Last Modified: Fri, 03 Oct 2025 17:07:34 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:c4d4815b9a11442fc43201919aa8014847193b2ea525ace85b8d0eb60d765a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139373870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd8a359ce6c26d86fb042cbf450b3c3ff541e12cb9fb7a3b997249ccf091c4d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e741fecb89d2db47b037f78cdb8490877b12c4d1e828f80f3b1293a401b20878`  
		Last Modified: Fri, 03 Oct 2025 15:43:07 GMT  
		Size: 8.1 MB (8113304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346499d5a12a0d1eeb76f29fdae7d39b3ed1691d2970b7b4241a85a0e2e3bef8`  
		Last Modified: Fri, 03 Oct 2025 15:43:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afe8024aad7ad6596057655d9b78201ae0e584574468ac179036133c2567840`  
		Last Modified: Fri, 03 Oct 2025 15:43:09 GMT  
		Size: 18.4 MB (18419890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4bb5235a7e0f14da9eb4e2ea6fb77c0065d5f84a49d54b08906ec0ecdd9f2f`  
		Last Modified: Fri, 03 Oct 2025 15:43:09 GMT  
		Size: 20.8 MB (20759307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef894bb2a7c2d67015665f6d2215a2827e7e83b54c9faacc27a95226e77785e`  
		Last Modified: Fri, 03 Oct 2025 15:43:09 GMT  
		Size: 20.4 MB (20395111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e560df71363b222435e64e5d5cb6b7c662012dcaf8e3aa6e0e6d48b51e402be`  
		Last Modified: Fri, 03 Oct 2025 15:43:07 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f6e2a7bf9e1086d0da4efd3d4ef8b63976d2d5b8b312ff28faedbc78a2326c`  
		Last Modified: Fri, 03 Oct 2025 15:43:07 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7f4fcb9ac33ee3406f8a2e0a0a7f9e8d49f7d284d569d0fd29dd6869ba6800`  
		Last Modified: Fri, 03 Oct 2025 15:43:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2c3aa0041ce9ba572b86ea1fcac3b5d7f4b1677cf9f095f468906db1729596`  
		Last Modified: Fri, 03 Oct 2025 17:07:55 GMT  
		Size: 9.5 MB (9461646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fe314793c08ec1515cd9deda4460b8a5b0db59e8729d8bded69bdec566cd71`  
		Last Modified: Fri, 03 Oct 2025 16:59:42 GMT  
		Size: 90.0 KB (89981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb653e89e23d01c359f38e4450c46e2d9ca61cc191138aa22957c203ed6e22ec`  
		Last Modified: Fri, 03 Oct 2025 16:59:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf8683c1349c2a719607f0bcb1a8d41f5e6a29f4b03f96244fb2cf0f5f4dd66`  
		Last Modified: Fri, 03 Oct 2025 17:08:08 GMT  
		Size: 58.6 MB (58625566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688e92fba7d15ffd6cd6e27300ad649cabb51eff9ccdaec5ef114b9350cc7b4e`  
		Last Modified: Fri, 03 Oct 2025 16:59:48 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1462b184835eae09507a3e3d65e9c9f19fcd9848c71828db1e285b96bfcb79`  
		Last Modified: Fri, 03 Oct 2025 16:59:51 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:c7e45e86f8604600d824baec0e69f4c65462df8aac93b87ad7cf803d86abd9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f804293a66ed736d887ecd088c6ca90edaec061dbac7ab4a980d15f3aa5c5e9`

```dockerfile
```

-	Layers:
	-	`sha256:0530a53564b6d37728db77e17830b3b569f1dacada687a47ab52b54ad1c62b4e`  
		Last Modified: Fri, 03 Oct 2025 17:07:37 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:0a926edb934d0f8b17e76d7f6f17e9d6bd9bbc3ad6518162b53fdb9c3fdd882d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137340580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c652524e809c5d137417df4764b799e2c6a8c4322962058b296c35b34062b1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d657a1bd6673b13a869dd3aef9cb3bf6e77a13d7fbd88af33a7bd58887072018`  
		Last Modified: Fri, 03 Oct 2025 15:42:27 GMT  
		Size: 7.4 MB (7437667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfff8f3e04fb650d0573a6e389dd188a26cba26951c74c1394ec977fe1ef58bf`  
		Last Modified: Fri, 03 Oct 2025 15:42:27 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f2efb09e78c3d501b901d46bd087f1a612e3e10f89869cff4521a5c9c2b6ae`  
		Last Modified: Fri, 03 Oct 2025 15:42:28 GMT  
		Size: 18.4 MB (18402988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48db8f4416a857355de94fb9f102ee288bc32a5b53c5ab11905115a9a5994bea`  
		Last Modified: Fri, 03 Oct 2025 15:42:31 GMT  
		Size: 20.7 MB (20743372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92347015b38c861670eb924808eab074eea9dcf1673973127cca5beb673dfdf`  
		Last Modified: Fri, 03 Oct 2025 15:42:28 GMT  
		Size: 20.4 MB (20375979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ad4c72b2e8eebe227682353ea38c6836bee64dfe34120bb0978a6a1b2c877e`  
		Last Modified: Fri, 03 Oct 2025 15:42:27 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4668ed29abe41847a4deb43b28b6a5ed5e091640d9ec945da223020b6f00ea7`  
		Last Modified: Fri, 03 Oct 2025 15:42:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1598b4284b6ec18f8af59189933ad4ee519d64618bd695ca79acc5d939da33`  
		Last Modified: Fri, 03 Oct 2025 15:42:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ebb21f754214da975a71e1ba28d952b5ae191687ae6c179c78065ce4e541e`  
		Last Modified: Fri, 03 Oct 2025 16:11:19 GMT  
		Size: 8.6 MB (8610523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0877977e09f87101c4bd9c37bd65e153b219f9836b23d556a16a9b0b5fe45d45`  
		Last Modified: Fri, 03 Oct 2025 16:11:19 GMT  
		Size: 86.4 KB (86413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc827d329b124f2b9726dfe6a69cc386dc0eda533d3cd963c4adb66a009c692`  
		Last Modified: Fri, 03 Oct 2025 16:11:19 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de26344b3baf222165d99725f4e6005989ad9aac0d86b9823da47d9a2822a1e`  
		Last Modified: Fri, 03 Oct 2025 16:11:27 GMT  
		Size: 58.5 MB (58456440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b861b628ae6ea276b3ec7b316e997d5af30aa5a020c46aa575255be8141aa963`  
		Last Modified: Fri, 03 Oct 2025 16:11:19 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e625b77a45b983325a2fb85508fbae7fb9528de4aa9c234df3d9ae7997ea62c3`  
		Last Modified: Fri, 03 Oct 2025 16:11:19 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:28ea01538c9e99afc728e7a4ccea25b786fb165d230438dd230909f8b1acf756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47499ecd1917c3c2dc0afb0eb65986977f671e3f857b2efb2fde33166b49952`

```dockerfile
```

-	Layers:
	-	`sha256:7d09db7c2511a8add6fa1782a8ec1264a402e03b8d100de5628bda682ade79e3`  
		Last Modified: Fri, 03 Oct 2025 17:07:40 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9b1e822a590c78b7451b791f292c410c8f69c7640dd08e59254f79895428a3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139550335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19722dfc0d9b013519a534499e2fee11d2089961fed39dfe8c4c33b8b47380f`
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

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:3fa0c490ac7be08d8aabf40573a97ac75cc2b74d7409d6b4613b2fa333e08c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa504619bebfd347448636f4153732c1bf90a84b047296cee36e608377d75e23`

```dockerfile
```

-	Layers:
	-	`sha256:803bf8be38f0ab775046063b7f39b17d8f2196b3399174639076413b58ba84c2`  
		Last Modified: Fri, 03 Oct 2025 17:07:43 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

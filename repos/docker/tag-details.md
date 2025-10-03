<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.5`](#docker285)
-	[`docker:28.5-cli`](#docker285-cli)
-	[`docker:28.5-dind`](#docker285-dind)
-	[`docker:28.5-dind-rootless`](#docker285-dind-rootless)
-	[`docker:28.5-windowsservercore`](#docker285-windowsservercore)
-	[`docker:28.5-windowsservercore-ltsc2022`](#docker285-windowsservercore-ltsc2022)
-	[`docker:28.5-windowsservercore-ltsc2025`](#docker285-windowsservercore-ltsc2025)
-	[`docker:28.5.0`](#docker2850)
-	[`docker:28.5.0-alpine3.22`](#docker2850-alpine322)
-	[`docker:28.5.0-cli`](#docker2850-cli)
-	[`docker:28.5.0-cli-alpine3.22`](#docker2850-cli-alpine322)
-	[`docker:28.5.0-dind`](#docker2850-dind)
-	[`docker:28.5.0-dind-alpine3.22`](#docker2850-dind-alpine322)
-	[`docker:28.5.0-dind-rootless`](#docker2850-dind-rootless)
-	[`docker:28.5.0-windowsservercore`](#docker2850-windowsservercore)
-	[`docker:28.5.0-windowsservercore-ltsc2022`](#docker2850-windowsservercore-ltsc2022)
-	[`docker:28.5.0-windowsservercore-ltsc2025`](#docker2850-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

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

### `docker:28` - linux; amd64

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

### `docker:28` - unknown; unknown

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

### `docker:28` - linux; arm variant v6

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

### `docker:28` - unknown; unknown

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

### `docker:28` - linux; arm variant v7

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

### `docker:28` - unknown; unknown

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

### `docker:28` - linux; arm64 variant v8

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

### `docker:28` - unknown; unknown

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

## `docker:28-cli`

```console
$ docker pull docker@sha256:9346c5506bb395e8d543072b8a42e55b6ac4c1ee2bb49ea1e6dbcdae058d6413
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

### `docker:28-cli` - linux; amd64

```console
$ docker pull docker@sha256:d5eea7f642a97e37c6cfb144bbf1c621a921d6bd6770925ca46083b6022e72ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76252652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5318c07034b1070773327332274ae100cfd2b187005a9b16f0560bcaf24f6374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b0a855e3980a26a067b2d2a0781a2320c0ebb0b95cdd8969e3d1e63c41977d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9a5a518442282d243de3bf9659aab9d1324488d38cf20df6f68901e7a70638`

```dockerfile
```

-	Layers:
	-	`sha256:b23b75fb095cd2bcd99a74b495c36431098c714483d3aee226f206d2f69e78d9`  
		Last Modified: Fri, 03 Oct 2025 17:07:47 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d7381fa06c8275c17d5e128e8ffe09b5da39eb3e8af48dd9b249316673239c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71190674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f458ec5b7496b07e3c6124e1edb26f921eb5e0291749ec9f7fb91d2be49adcf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:288801d6b3cdcdd95811bed6b33669ba7e4a9291f0803185af8cba15f3a43326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c159a7f1feae003fde9b008e8ea0a16bb293f6dc4a2131b493431ba075f28d4`

```dockerfile
```

-	Layers:
	-	`sha256:fb2fa30f269ea814e093ddff016eaecae13a50ff05d306e058913baf73667f5c`  
		Last Modified: Fri, 03 Oct 2025 17:07:50 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:bb7ef8a43ddb42bea13ec4c076ada0fb84a1187d43d5a485d1857244574d25dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70181198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b28aaf2092e123a0a50c48ec059da72a6b792fc5ad10d81c3c61e0f4f57e412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b53b2a0dfffaf54e3c1624ca1acfe05f386da5c9a30462d4f81b2ac6efbad288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e3716ca95c952691eb8a96e068b1721637e70962ee86e71f5249766dc0ce19`

```dockerfile
```

-	Layers:
	-	`sha256:fda163a204484dc73af895db49f72864ac1701fb57029233d7ddc220474c8610`  
		Last Modified: Fri, 03 Oct 2025 17:07:53 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c0724b17cc1213826a3286add14ace28d271de874fa36db2ee89bd4dace4f3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71652939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dffc628b273a3882ea3e3ba84bb32e497b0a22f0c102b4d59362d4fe31fcac6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:522c2cc4ffb9267687aef6f8d72730ea70ceca998330ee32f74c9816c9a1acbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b98ac9778851ce1834f2ea2b1f14805861737c19429ba5d5ad7902bd7ded272`

```dockerfile
```

-	Layers:
	-	`sha256:bb5f4b80b573216b93fcd1b186a648d54c90b671162a8e1cf7cac20bc8679899`  
		Last Modified: Fri, 03 Oct 2025 17:07:56 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

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

### `docker:28-dind` - linux; amd64

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

### `docker:28-dind` - unknown; unknown

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

### `docker:28-dind` - linux; arm variant v6

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

### `docker:28-dind` - unknown; unknown

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

### `docker:28-dind` - linux; arm variant v7

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

### `docker:28-dind` - unknown; unknown

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

### `docker:28-dind` - linux; arm64 variant v8

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

### `docker:28-dind` - unknown; unknown

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

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:eeb43ad630a5165c910f03041a590147ddb1c2632be3a3c397e9b2c2b4efa7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

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

### `docker:28-dind-rootless` - unknown; unknown

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

### `docker:28-dind-rootless` - linux; arm64 variant v8

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

### `docker:28-dind-rootless` - unknown; unknown

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

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:0ef80f9aee78421ad00cb9465c8d1f248f547c926315728845aa35ddc93b63d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:ad136d080029be1c9cf7792be1903931d264f5381e42166d3f3e7f1cfb01ea39
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638399147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a2b67a7be1525f868135b1a1c818f62ea909ae749a6bb5b517794cd4079df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Fri, 03 Oct 2025 15:43:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:38 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:45:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:00 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:45:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:45:02 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:45:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:45:12 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eac7129a35b3f3d93c10663cb922ac94175a7659ab43177cd29b8385d27396`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736095fdc18733277b021a61df3a3e30ce7092927089af31f6692fda83cace32`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 387.0 KB (386985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d353df5347d8893329766ad323f55f264ba05d9a3aac24528687197623c4ce0`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b067755f7397460b020f2cc400bd867b894ced17e4c67e655baa97401f6df86`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cf9b648dddc92e1677712ec6e0bae6d9a44e3648499cd72518c52fb94fb638`  
		Last Modified: Fri, 03 Oct 2025 15:58:03 GMT  
		Size: 20.8 MB (20792951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2af40a7d166840f2088865abe2618fec08f1764ebf29f2c95eaad97a5808c09`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f0b14cc909cb5745c3ddf411f5554cb3266e8a84577d7ca3786d71658b0e1`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420ccf00c9a5ac48828c2db2e12d31e69b900387f51aa2e08fcf0d82d599fd3`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8df219328e6f8e13ea4ce0e6f4e259f30e86c01f2cf4b0e935b34d182f2d99e`  
		Last Modified: Fri, 03 Oct 2025 15:58:16 GMT  
		Size: 23.2 MB (23173234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557962edd46b4b31a288d5f51205186b0bbbe6d695dd9c58cf749f07272beded`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55536c08291034b8fd66f7eb66d704bdd91734ed084ef651a0e6def838bd3ddf`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0bc4bd86cc52355181c183581a4717dbd9fa11425954465150b60ddc54db89`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c62fdb98b4bcde258cbda8487f9c4beacc78ab1e94f47db066289a37859dc0c`  
		Last Modified: Fri, 03 Oct 2025 15:58:01 GMT  
		Size: 22.6 MB (22594497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:beb061eb6549b25fd99d8cabf410d457746a606589a7c2ae5aaf3f93da667b34
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349086539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5cb3226376ec4297559382e05ed2b5b66cccb4f94ae0332cb304ad7ccf0335`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 03 Oct 2025 15:43:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:12 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:44:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:29 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:44:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:44:32 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:44:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:44:51 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa8a1e68a053fb59ee6d7717ce3dd08bb123234150d6c4f204b79c4babf6f96`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31091b97f76c2d01280909a82b19ec67be3458d552c83d1c3412bb1ada372478`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 375.6 KB (375595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe433c7244e17c134d5228a182610dd844018e175f0b7156d52e7a52b8c86db`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c85d8d7af1aafc8bd20e85d1d8a691a264d31a4819e86d6c7312e07aee8304`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0070dbe9d2e0f165d892573932fb485610fd5fc96f45f8094a36f5058b12e5a`  
		Last Modified: Fri, 03 Oct 2025 15:52:17 GMT  
		Size: 20.8 MB (20789973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213aa569cb703a24a789f517fe56a6ae497c99175c3d2cd373c89fa1f1089b4e`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7de2afae7847412112e197ac1c25ec2a40c9581eea75463412a97252857436`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85316e22a17d0d25c44a17c27c81262dfc1d7b2a3ab2928fb437761164e0c9`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f657f72b51307aef095c995e842dc3864c6bab5f77c72502b408e99fde4c0555`  
		Last Modified: Fri, 03 Oct 2025 15:52:35 GMT  
		Size: 23.2 MB (23171772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc17bee33fd2a219b6c8c2e719be2eee0413c0498eabf36c7df35feacde51`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca46b7935b2586b3219f0dcbb26f056695aa4d2780b86eef9c123323d12e442`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40563864091199f7c4bd7971379390f2a0eb68602bd84363d0d619d389081a66`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120ec86946b04b2ce643f75ca4da1136e61282d75f9079ce2dbe6439377e191c`  
		Last Modified: Fri, 03 Oct 2025 15:52:19 GMT  
		Size: 22.6 MB (22592462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0ba9c9b2ed57e14d1f504dee1e427cfba36d706f3fb4aed03f518b850f8f59b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:beb061eb6549b25fd99d8cabf410d457746a606589a7c2ae5aaf3f93da667b34
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349086539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5cb3226376ec4297559382e05ed2b5b66cccb4f94ae0332cb304ad7ccf0335`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 03 Oct 2025 15:43:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:12 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:44:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:29 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:44:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:44:32 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:44:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:44:51 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa8a1e68a053fb59ee6d7717ce3dd08bb123234150d6c4f204b79c4babf6f96`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31091b97f76c2d01280909a82b19ec67be3458d552c83d1c3412bb1ada372478`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 375.6 KB (375595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe433c7244e17c134d5228a182610dd844018e175f0b7156d52e7a52b8c86db`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c85d8d7af1aafc8bd20e85d1d8a691a264d31a4819e86d6c7312e07aee8304`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0070dbe9d2e0f165d892573932fb485610fd5fc96f45f8094a36f5058b12e5a`  
		Last Modified: Fri, 03 Oct 2025 15:52:17 GMT  
		Size: 20.8 MB (20789973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213aa569cb703a24a789f517fe56a6ae497c99175c3d2cd373c89fa1f1089b4e`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7de2afae7847412112e197ac1c25ec2a40c9581eea75463412a97252857436`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85316e22a17d0d25c44a17c27c81262dfc1d7b2a3ab2928fb437761164e0c9`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f657f72b51307aef095c995e842dc3864c6bab5f77c72502b408e99fde4c0555`  
		Last Modified: Fri, 03 Oct 2025 15:52:35 GMT  
		Size: 23.2 MB (23171772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc17bee33fd2a219b6c8c2e719be2eee0413c0498eabf36c7df35feacde51`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca46b7935b2586b3219f0dcbb26f056695aa4d2780b86eef9c123323d12e442`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40563864091199f7c4bd7971379390f2a0eb68602bd84363d0d619d389081a66`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120ec86946b04b2ce643f75ca4da1136e61282d75f9079ce2dbe6439377e191c`  
		Last Modified: Fri, 03 Oct 2025 15:52:19 GMT  
		Size: 22.6 MB (22592462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:805b80eb5838dff72fb60586d27489abce0602489110a4c8936a08781e407c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:ad136d080029be1c9cf7792be1903931d264f5381e42166d3f3e7f1cfb01ea39
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638399147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a2b67a7be1525f868135b1a1c818f62ea909ae749a6bb5b517794cd4079df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Fri, 03 Oct 2025 15:43:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:38 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:45:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:00 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:45:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:45:02 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:45:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:45:12 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eac7129a35b3f3d93c10663cb922ac94175a7659ab43177cd29b8385d27396`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736095fdc18733277b021a61df3a3e30ce7092927089af31f6692fda83cace32`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 387.0 KB (386985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d353df5347d8893329766ad323f55f264ba05d9a3aac24528687197623c4ce0`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b067755f7397460b020f2cc400bd867b894ced17e4c67e655baa97401f6df86`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cf9b648dddc92e1677712ec6e0bae6d9a44e3648499cd72518c52fb94fb638`  
		Last Modified: Fri, 03 Oct 2025 15:58:03 GMT  
		Size: 20.8 MB (20792951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2af40a7d166840f2088865abe2618fec08f1764ebf29f2c95eaad97a5808c09`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f0b14cc909cb5745c3ddf411f5554cb3266e8a84577d7ca3786d71658b0e1`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420ccf00c9a5ac48828c2db2e12d31e69b900387f51aa2e08fcf0d82d599fd3`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8df219328e6f8e13ea4ce0e6f4e259f30e86c01f2cf4b0e935b34d182f2d99e`  
		Last Modified: Fri, 03 Oct 2025 15:58:16 GMT  
		Size: 23.2 MB (23173234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557962edd46b4b31a288d5f51205186b0bbbe6d695dd9c58cf749f07272beded`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55536c08291034b8fd66f7eb66d704bdd91734ed084ef651a0e6def838bd3ddf`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0bc4bd86cc52355181c183581a4717dbd9fa11425954465150b60ddc54db89`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c62fdb98b4bcde258cbda8487f9c4beacc78ab1e94f47db066289a37859dc0c`  
		Last Modified: Fri, 03 Oct 2025 15:58:01 GMT  
		Size: 22.6 MB (22594497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5`

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

### `docker:28.5` - linux; amd64

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

### `docker:28.5` - unknown; unknown

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

### `docker:28.5` - linux; arm variant v6

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

### `docker:28.5` - unknown; unknown

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

### `docker:28.5` - linux; arm variant v7

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

### `docker:28.5` - unknown; unknown

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

### `docker:28.5` - linux; arm64 variant v8

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

### `docker:28.5` - unknown; unknown

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

## `docker:28.5-cli`

```console
$ docker pull docker@sha256:9346c5506bb395e8d543072b8a42e55b6ac4c1ee2bb49ea1e6dbcdae058d6413
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

### `docker:28.5-cli` - linux; amd64

```console
$ docker pull docker@sha256:d5eea7f642a97e37c6cfb144bbf1c621a921d6bd6770925ca46083b6022e72ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76252652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5318c07034b1070773327332274ae100cfd2b187005a9b16f0560bcaf24f6374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b0a855e3980a26a067b2d2a0781a2320c0ebb0b95cdd8969e3d1e63c41977d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9a5a518442282d243de3bf9659aab9d1324488d38cf20df6f68901e7a70638`

```dockerfile
```

-	Layers:
	-	`sha256:b23b75fb095cd2bcd99a74b495c36431098c714483d3aee226f206d2f69e78d9`  
		Last Modified: Fri, 03 Oct 2025 17:07:47 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d7381fa06c8275c17d5e128e8ffe09b5da39eb3e8af48dd9b249316673239c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71190674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f458ec5b7496b07e3c6124e1edb26f921eb5e0291749ec9f7fb91d2be49adcf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:288801d6b3cdcdd95811bed6b33669ba7e4a9291f0803185af8cba15f3a43326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c159a7f1feae003fde9b008e8ea0a16bb293f6dc4a2131b493431ba075f28d4`

```dockerfile
```

-	Layers:
	-	`sha256:fb2fa30f269ea814e093ddff016eaecae13a50ff05d306e058913baf73667f5c`  
		Last Modified: Fri, 03 Oct 2025 17:07:50 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:bb7ef8a43ddb42bea13ec4c076ada0fb84a1187d43d5a485d1857244574d25dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70181198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b28aaf2092e123a0a50c48ec059da72a6b792fc5ad10d81c3c61e0f4f57e412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b53b2a0dfffaf54e3c1624ca1acfe05f386da5c9a30462d4f81b2ac6efbad288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e3716ca95c952691eb8a96e068b1721637e70962ee86e71f5249766dc0ce19`

```dockerfile
```

-	Layers:
	-	`sha256:fda163a204484dc73af895db49f72864ac1701fb57029233d7ddc220474c8610`  
		Last Modified: Fri, 03 Oct 2025 17:07:53 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c0724b17cc1213826a3286add14ace28d271de874fa36db2ee89bd4dace4f3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71652939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dffc628b273a3882ea3e3ba84bb32e497b0a22f0c102b4d59362d4fe31fcac6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.5-cli` - unknown; unknown

```console
$ docker pull docker@sha256:522c2cc4ffb9267687aef6f8d72730ea70ceca998330ee32f74c9816c9a1acbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b98ac9778851ce1834f2ea2b1f14805861737c19429ba5d5ad7902bd7ded272`

```dockerfile
```

-	Layers:
	-	`sha256:bb5f4b80b573216b93fcd1b186a648d54c90b671162a8e1cf7cac20bc8679899`  
		Last Modified: Fri, 03 Oct 2025 17:07:56 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5-dind`

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

### `docker:28.5-dind` - linux; amd64

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

### `docker:28.5-dind` - unknown; unknown

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

### `docker:28.5-dind` - linux; arm variant v6

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

### `docker:28.5-dind` - unknown; unknown

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

### `docker:28.5-dind` - linux; arm variant v7

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

### `docker:28.5-dind` - unknown; unknown

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

### `docker:28.5-dind` - linux; arm64 variant v8

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

### `docker:28.5-dind` - unknown; unknown

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

## `docker:28.5-dind-rootless`

```console
$ docker pull docker@sha256:eeb43ad630a5165c910f03041a590147ddb1c2632be3a3c397e9b2c2b4efa7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.5-dind-rootless` - linux; amd64

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

### `docker:28.5-dind-rootless` - unknown; unknown

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

### `docker:28.5-dind-rootless` - linux; arm64 variant v8

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

### `docker:28.5-dind-rootless` - unknown; unknown

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

## `docker:28.5-windowsservercore`

```console
$ docker pull docker@sha256:0ef80f9aee78421ad00cb9465c8d1f248f547c926315728845aa35ddc93b63d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:28.5-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:ad136d080029be1c9cf7792be1903931d264f5381e42166d3f3e7f1cfb01ea39
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638399147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a2b67a7be1525f868135b1a1c818f62ea909ae749a6bb5b517794cd4079df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Fri, 03 Oct 2025 15:43:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:38 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:45:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:00 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:45:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:45:02 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:45:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:45:12 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eac7129a35b3f3d93c10663cb922ac94175a7659ab43177cd29b8385d27396`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736095fdc18733277b021a61df3a3e30ce7092927089af31f6692fda83cace32`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 387.0 KB (386985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d353df5347d8893329766ad323f55f264ba05d9a3aac24528687197623c4ce0`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b067755f7397460b020f2cc400bd867b894ced17e4c67e655baa97401f6df86`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cf9b648dddc92e1677712ec6e0bae6d9a44e3648499cd72518c52fb94fb638`  
		Last Modified: Fri, 03 Oct 2025 15:58:03 GMT  
		Size: 20.8 MB (20792951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2af40a7d166840f2088865abe2618fec08f1764ebf29f2c95eaad97a5808c09`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f0b14cc909cb5745c3ddf411f5554cb3266e8a84577d7ca3786d71658b0e1`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420ccf00c9a5ac48828c2db2e12d31e69b900387f51aa2e08fcf0d82d599fd3`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8df219328e6f8e13ea4ce0e6f4e259f30e86c01f2cf4b0e935b34d182f2d99e`  
		Last Modified: Fri, 03 Oct 2025 15:58:16 GMT  
		Size: 23.2 MB (23173234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557962edd46b4b31a288d5f51205186b0bbbe6d695dd9c58cf749f07272beded`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55536c08291034b8fd66f7eb66d704bdd91734ed084ef651a0e6def838bd3ddf`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0bc4bd86cc52355181c183581a4717dbd9fa11425954465150b60ddc54db89`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c62fdb98b4bcde258cbda8487f9c4beacc78ab1e94f47db066289a37859dc0c`  
		Last Modified: Fri, 03 Oct 2025 15:58:01 GMT  
		Size: 22.6 MB (22594497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.5-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:beb061eb6549b25fd99d8cabf410d457746a606589a7c2ae5aaf3f93da667b34
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349086539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5cb3226376ec4297559382e05ed2b5b66cccb4f94ae0332cb304ad7ccf0335`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 03 Oct 2025 15:43:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:12 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:44:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:29 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:44:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:44:32 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:44:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:44:51 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa8a1e68a053fb59ee6d7717ce3dd08bb123234150d6c4f204b79c4babf6f96`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31091b97f76c2d01280909a82b19ec67be3458d552c83d1c3412bb1ada372478`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 375.6 KB (375595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe433c7244e17c134d5228a182610dd844018e175f0b7156d52e7a52b8c86db`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c85d8d7af1aafc8bd20e85d1d8a691a264d31a4819e86d6c7312e07aee8304`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0070dbe9d2e0f165d892573932fb485610fd5fc96f45f8094a36f5058b12e5a`  
		Last Modified: Fri, 03 Oct 2025 15:52:17 GMT  
		Size: 20.8 MB (20789973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213aa569cb703a24a789f517fe56a6ae497c99175c3d2cd373c89fa1f1089b4e`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7de2afae7847412112e197ac1c25ec2a40c9581eea75463412a97252857436`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85316e22a17d0d25c44a17c27c81262dfc1d7b2a3ab2928fb437761164e0c9`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f657f72b51307aef095c995e842dc3864c6bab5f77c72502b408e99fde4c0555`  
		Last Modified: Fri, 03 Oct 2025 15:52:35 GMT  
		Size: 23.2 MB (23171772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc17bee33fd2a219b6c8c2e719be2eee0413c0498eabf36c7df35feacde51`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca46b7935b2586b3219f0dcbb26f056695aa4d2780b86eef9c123323d12e442`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40563864091199f7c4bd7971379390f2a0eb68602bd84363d0d619d389081a66`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120ec86946b04b2ce643f75ca4da1136e61282d75f9079ce2dbe6439377e191c`  
		Last Modified: Fri, 03 Oct 2025 15:52:19 GMT  
		Size: 22.6 MB (22592462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0ba9c9b2ed57e14d1f504dee1e427cfba36d706f3fb4aed03f518b850f8f59b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:28.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:beb061eb6549b25fd99d8cabf410d457746a606589a7c2ae5aaf3f93da667b34
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349086539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5cb3226376ec4297559382e05ed2b5b66cccb4f94ae0332cb304ad7ccf0335`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 03 Oct 2025 15:43:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:12 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:44:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:29 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:44:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:44:32 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:44:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:44:51 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa8a1e68a053fb59ee6d7717ce3dd08bb123234150d6c4f204b79c4babf6f96`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31091b97f76c2d01280909a82b19ec67be3458d552c83d1c3412bb1ada372478`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 375.6 KB (375595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe433c7244e17c134d5228a182610dd844018e175f0b7156d52e7a52b8c86db`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c85d8d7af1aafc8bd20e85d1d8a691a264d31a4819e86d6c7312e07aee8304`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0070dbe9d2e0f165d892573932fb485610fd5fc96f45f8094a36f5058b12e5a`  
		Last Modified: Fri, 03 Oct 2025 15:52:17 GMT  
		Size: 20.8 MB (20789973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213aa569cb703a24a789f517fe56a6ae497c99175c3d2cd373c89fa1f1089b4e`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7de2afae7847412112e197ac1c25ec2a40c9581eea75463412a97252857436`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85316e22a17d0d25c44a17c27c81262dfc1d7b2a3ab2928fb437761164e0c9`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f657f72b51307aef095c995e842dc3864c6bab5f77c72502b408e99fde4c0555`  
		Last Modified: Fri, 03 Oct 2025 15:52:35 GMT  
		Size: 23.2 MB (23171772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc17bee33fd2a219b6c8c2e719be2eee0413c0498eabf36c7df35feacde51`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca46b7935b2586b3219f0dcbb26f056695aa4d2780b86eef9c123323d12e442`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40563864091199f7c4bd7971379390f2a0eb68602bd84363d0d619d389081a66`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120ec86946b04b2ce643f75ca4da1136e61282d75f9079ce2dbe6439377e191c`  
		Last Modified: Fri, 03 Oct 2025 15:52:19 GMT  
		Size: 22.6 MB (22592462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:805b80eb5838dff72fb60586d27489abce0602489110a4c8936a08781e407c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:28.5-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:ad136d080029be1c9cf7792be1903931d264f5381e42166d3f3e7f1cfb01ea39
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638399147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a2b67a7be1525f868135b1a1c818f62ea909ae749a6bb5b517794cd4079df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Fri, 03 Oct 2025 15:43:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:38 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:45:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:00 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:45:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:45:02 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:45:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:45:12 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eac7129a35b3f3d93c10663cb922ac94175a7659ab43177cd29b8385d27396`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736095fdc18733277b021a61df3a3e30ce7092927089af31f6692fda83cace32`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 387.0 KB (386985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d353df5347d8893329766ad323f55f264ba05d9a3aac24528687197623c4ce0`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b067755f7397460b020f2cc400bd867b894ced17e4c67e655baa97401f6df86`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cf9b648dddc92e1677712ec6e0bae6d9a44e3648499cd72518c52fb94fb638`  
		Last Modified: Fri, 03 Oct 2025 15:58:03 GMT  
		Size: 20.8 MB (20792951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2af40a7d166840f2088865abe2618fec08f1764ebf29f2c95eaad97a5808c09`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f0b14cc909cb5745c3ddf411f5554cb3266e8a84577d7ca3786d71658b0e1`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420ccf00c9a5ac48828c2db2e12d31e69b900387f51aa2e08fcf0d82d599fd3`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8df219328e6f8e13ea4ce0e6f4e259f30e86c01f2cf4b0e935b34d182f2d99e`  
		Last Modified: Fri, 03 Oct 2025 15:58:16 GMT  
		Size: 23.2 MB (23173234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557962edd46b4b31a288d5f51205186b0bbbe6d695dd9c58cf749f07272beded`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55536c08291034b8fd66f7eb66d704bdd91734ed084ef651a0e6def838bd3ddf`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0bc4bd86cc52355181c183581a4717dbd9fa11425954465150b60ddc54db89`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c62fdb98b4bcde258cbda8487f9c4beacc78ab1e94f47db066289a37859dc0c`  
		Last Modified: Fri, 03 Oct 2025 15:58:01 GMT  
		Size: 22.6 MB (22594497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5.0`

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

### `docker:28.5.0` - linux; amd64

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

### `docker:28.5.0` - unknown; unknown

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

### `docker:28.5.0` - linux; arm variant v6

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

### `docker:28.5.0` - unknown; unknown

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

### `docker:28.5.0` - linux; arm variant v7

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

### `docker:28.5.0` - unknown; unknown

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

### `docker:28.5.0` - linux; arm64 variant v8

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

### `docker:28.5.0` - unknown; unknown

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

## `docker:28.5.0-alpine3.22`

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

### `docker:28.5.0-alpine3.22` - linux; amd64

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

### `docker:28.5.0-alpine3.22` - unknown; unknown

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

### `docker:28.5.0-alpine3.22` - linux; arm variant v6

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

### `docker:28.5.0-alpine3.22` - unknown; unknown

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

### `docker:28.5.0-alpine3.22` - linux; arm variant v7

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

### `docker:28.5.0-alpine3.22` - unknown; unknown

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

### `docker:28.5.0-alpine3.22` - linux; arm64 variant v8

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

### `docker:28.5.0-alpine3.22` - unknown; unknown

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

## `docker:28.5.0-cli`

```console
$ docker pull docker@sha256:9346c5506bb395e8d543072b8a42e55b6ac4c1ee2bb49ea1e6dbcdae058d6413
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

### `docker:28.5.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:d5eea7f642a97e37c6cfb144bbf1c621a921d6bd6770925ca46083b6022e72ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76252652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5318c07034b1070773327332274ae100cfd2b187005a9b16f0560bcaf24f6374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.5.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b0a855e3980a26a067b2d2a0781a2320c0ebb0b95cdd8969e3d1e63c41977d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9a5a518442282d243de3bf9659aab9d1324488d38cf20df6f68901e7a70638`

```dockerfile
```

-	Layers:
	-	`sha256:b23b75fb095cd2bcd99a74b495c36431098c714483d3aee226f206d2f69e78d9`  
		Last Modified: Fri, 03 Oct 2025 17:07:47 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d7381fa06c8275c17d5e128e8ffe09b5da39eb3e8af48dd9b249316673239c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71190674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f458ec5b7496b07e3c6124e1edb26f921eb5e0291749ec9f7fb91d2be49adcf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.5.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:288801d6b3cdcdd95811bed6b33669ba7e4a9291f0803185af8cba15f3a43326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c159a7f1feae003fde9b008e8ea0a16bb293f6dc4a2131b493431ba075f28d4`

```dockerfile
```

-	Layers:
	-	`sha256:fb2fa30f269ea814e093ddff016eaecae13a50ff05d306e058913baf73667f5c`  
		Last Modified: Fri, 03 Oct 2025 17:07:50 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:bb7ef8a43ddb42bea13ec4c076ada0fb84a1187d43d5a485d1857244574d25dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70181198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b28aaf2092e123a0a50c48ec059da72a6b792fc5ad10d81c3c61e0f4f57e412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.5.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b53b2a0dfffaf54e3c1624ca1acfe05f386da5c9a30462d4f81b2ac6efbad288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e3716ca95c952691eb8a96e068b1721637e70962ee86e71f5249766dc0ce19`

```dockerfile
```

-	Layers:
	-	`sha256:fda163a204484dc73af895db49f72864ac1701fb57029233d7ddc220474c8610`  
		Last Modified: Fri, 03 Oct 2025 17:07:53 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c0724b17cc1213826a3286add14ace28d271de874fa36db2ee89bd4dace4f3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71652939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dffc628b273a3882ea3e3ba84bb32e497b0a22f0c102b4d59362d4fe31fcac6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.5.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:522c2cc4ffb9267687aef6f8d72730ea70ceca998330ee32f74c9816c9a1acbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b98ac9778851ce1834f2ea2b1f14805861737c19429ba5d5ad7902bd7ded272`

```dockerfile
```

-	Layers:
	-	`sha256:bb5f4b80b573216b93fcd1b186a648d54c90b671162a8e1cf7cac20bc8679899`  
		Last Modified: Fri, 03 Oct 2025 17:07:56 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.0-cli-alpine3.22`

```console
$ docker pull docker@sha256:9346c5506bb395e8d543072b8a42e55b6ac4c1ee2bb49ea1e6dbcdae058d6413
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

### `docker:28.5.0-cli-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:d5eea7f642a97e37c6cfb144bbf1c621a921d6bd6770925ca46083b6022e72ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76252652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5318c07034b1070773327332274ae100cfd2b187005a9b16f0560bcaf24f6374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.5.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:b0a855e3980a26a067b2d2a0781a2320c0ebb0b95cdd8969e3d1e63c41977d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9a5a518442282d243de3bf9659aab9d1324488d38cf20df6f68901e7a70638`

```dockerfile
```

-	Layers:
	-	`sha256:b23b75fb095cd2bcd99a74b495c36431098c714483d3aee226f206d2f69e78d9`  
		Last Modified: Fri, 03 Oct 2025 17:07:47 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.0-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:d7381fa06c8275c17d5e128e8ffe09b5da39eb3e8af48dd9b249316673239c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71190674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f458ec5b7496b07e3c6124e1edb26f921eb5e0291749ec9f7fb91d2be49adcf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.5.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:288801d6b3cdcdd95811bed6b33669ba7e4a9291f0803185af8cba15f3a43326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c159a7f1feae003fde9b008e8ea0a16bb293f6dc4a2131b493431ba075f28d4`

```dockerfile
```

-	Layers:
	-	`sha256:fb2fa30f269ea814e093ddff016eaecae13a50ff05d306e058913baf73667f5c`  
		Last Modified: Fri, 03 Oct 2025 17:07:50 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.0-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:bb7ef8a43ddb42bea13ec4c076ada0fb84a1187d43d5a485d1857244574d25dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70181198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b28aaf2092e123a0a50c48ec059da72a6b792fc5ad10d81c3c61e0f4f57e412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.5.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:b53b2a0dfffaf54e3c1624ca1acfe05f386da5c9a30462d4f81b2ac6efbad288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e3716ca95c952691eb8a96e068b1721637e70962ee86e71f5249766dc0ce19`

```dockerfile
```

-	Layers:
	-	`sha256:fda163a204484dc73af895db49f72864ac1701fb57029233d7ddc220474c8610`  
		Last Modified: Fri, 03 Oct 2025 17:07:53 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.5.0-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c0724b17cc1213826a3286add14ace28d271de874fa36db2ee89bd4dace4f3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71652939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dffc628b273a3882ea3e3ba84bb32e497b0a22f0c102b4d59362d4fe31fcac6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.5.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:522c2cc4ffb9267687aef6f8d72730ea70ceca998330ee32f74c9816c9a1acbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b98ac9778851ce1834f2ea2b1f14805861737c19429ba5d5ad7902bd7ded272`

```dockerfile
```

-	Layers:
	-	`sha256:bb5f4b80b573216b93fcd1b186a648d54c90b671162a8e1cf7cac20bc8679899`  
		Last Modified: Fri, 03 Oct 2025 17:07:56 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.5.0-dind`

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

### `docker:28.5.0-dind` - linux; amd64

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

### `docker:28.5.0-dind` - unknown; unknown

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

### `docker:28.5.0-dind` - linux; arm variant v6

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

### `docker:28.5.0-dind` - unknown; unknown

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

### `docker:28.5.0-dind` - linux; arm variant v7

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

### `docker:28.5.0-dind` - unknown; unknown

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

### `docker:28.5.0-dind` - linux; arm64 variant v8

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

### `docker:28.5.0-dind` - unknown; unknown

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

## `docker:28.5.0-dind-alpine3.22`

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

### `docker:28.5.0-dind-alpine3.22` - linux; amd64

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

### `docker:28.5.0-dind-alpine3.22` - unknown; unknown

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

### `docker:28.5.0-dind-alpine3.22` - linux; arm variant v6

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

### `docker:28.5.0-dind-alpine3.22` - unknown; unknown

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

### `docker:28.5.0-dind-alpine3.22` - linux; arm variant v7

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

### `docker:28.5.0-dind-alpine3.22` - unknown; unknown

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

### `docker:28.5.0-dind-alpine3.22` - linux; arm64 variant v8

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

### `docker:28.5.0-dind-alpine3.22` - unknown; unknown

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

## `docker:28.5.0-dind-rootless`

```console
$ docker pull docker@sha256:eeb43ad630a5165c910f03041a590147ddb1c2632be3a3c397e9b2c2b4efa7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.5.0-dind-rootless` - linux; amd64

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

### `docker:28.5.0-dind-rootless` - unknown; unknown

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

### `docker:28.5.0-dind-rootless` - linux; arm64 variant v8

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

### `docker:28.5.0-dind-rootless` - unknown; unknown

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

## `docker:28.5.0-windowsservercore`

```console
$ docker pull docker@sha256:0ef80f9aee78421ad00cb9465c8d1f248f547c926315728845aa35ddc93b63d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:28.5.0-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:ad136d080029be1c9cf7792be1903931d264f5381e42166d3f3e7f1cfb01ea39
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638399147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a2b67a7be1525f868135b1a1c818f62ea909ae749a6bb5b517794cd4079df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Fri, 03 Oct 2025 15:43:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:38 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:45:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:00 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:45:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:45:02 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:45:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:45:12 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eac7129a35b3f3d93c10663cb922ac94175a7659ab43177cd29b8385d27396`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736095fdc18733277b021a61df3a3e30ce7092927089af31f6692fda83cace32`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 387.0 KB (386985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d353df5347d8893329766ad323f55f264ba05d9a3aac24528687197623c4ce0`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b067755f7397460b020f2cc400bd867b894ced17e4c67e655baa97401f6df86`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cf9b648dddc92e1677712ec6e0bae6d9a44e3648499cd72518c52fb94fb638`  
		Last Modified: Fri, 03 Oct 2025 15:58:03 GMT  
		Size: 20.8 MB (20792951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2af40a7d166840f2088865abe2618fec08f1764ebf29f2c95eaad97a5808c09`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f0b14cc909cb5745c3ddf411f5554cb3266e8a84577d7ca3786d71658b0e1`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420ccf00c9a5ac48828c2db2e12d31e69b900387f51aa2e08fcf0d82d599fd3`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8df219328e6f8e13ea4ce0e6f4e259f30e86c01f2cf4b0e935b34d182f2d99e`  
		Last Modified: Fri, 03 Oct 2025 15:58:16 GMT  
		Size: 23.2 MB (23173234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557962edd46b4b31a288d5f51205186b0bbbe6d695dd9c58cf749f07272beded`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55536c08291034b8fd66f7eb66d704bdd91734ed084ef651a0e6def838bd3ddf`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0bc4bd86cc52355181c183581a4717dbd9fa11425954465150b60ddc54db89`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c62fdb98b4bcde258cbda8487f9c4beacc78ab1e94f47db066289a37859dc0c`  
		Last Modified: Fri, 03 Oct 2025 15:58:01 GMT  
		Size: 22.6 MB (22594497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.5.0-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:beb061eb6549b25fd99d8cabf410d457746a606589a7c2ae5aaf3f93da667b34
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349086539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5cb3226376ec4297559382e05ed2b5b66cccb4f94ae0332cb304ad7ccf0335`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 03 Oct 2025 15:43:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:12 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:44:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:29 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:44:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:44:32 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:44:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:44:51 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa8a1e68a053fb59ee6d7717ce3dd08bb123234150d6c4f204b79c4babf6f96`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31091b97f76c2d01280909a82b19ec67be3458d552c83d1c3412bb1ada372478`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 375.6 KB (375595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe433c7244e17c134d5228a182610dd844018e175f0b7156d52e7a52b8c86db`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c85d8d7af1aafc8bd20e85d1d8a691a264d31a4819e86d6c7312e07aee8304`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0070dbe9d2e0f165d892573932fb485610fd5fc96f45f8094a36f5058b12e5a`  
		Last Modified: Fri, 03 Oct 2025 15:52:17 GMT  
		Size: 20.8 MB (20789973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213aa569cb703a24a789f517fe56a6ae497c99175c3d2cd373c89fa1f1089b4e`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7de2afae7847412112e197ac1c25ec2a40c9581eea75463412a97252857436`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85316e22a17d0d25c44a17c27c81262dfc1d7b2a3ab2928fb437761164e0c9`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f657f72b51307aef095c995e842dc3864c6bab5f77c72502b408e99fde4c0555`  
		Last Modified: Fri, 03 Oct 2025 15:52:35 GMT  
		Size: 23.2 MB (23171772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc17bee33fd2a219b6c8c2e719be2eee0413c0498eabf36c7df35feacde51`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca46b7935b2586b3219f0dcbb26f056695aa4d2780b86eef9c123323d12e442`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40563864091199f7c4bd7971379390f2a0eb68602bd84363d0d619d389081a66`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120ec86946b04b2ce643f75ca4da1136e61282d75f9079ce2dbe6439377e191c`  
		Last Modified: Fri, 03 Oct 2025 15:52:19 GMT  
		Size: 22.6 MB (22592462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0ba9c9b2ed57e14d1f504dee1e427cfba36d706f3fb4aed03f518b850f8f59b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:28.5.0-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:beb061eb6549b25fd99d8cabf410d457746a606589a7c2ae5aaf3f93da667b34
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349086539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5cb3226376ec4297559382e05ed2b5b66cccb4f94ae0332cb304ad7ccf0335`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 03 Oct 2025 15:43:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:12 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:44:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:29 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:44:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:44:32 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:44:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:44:51 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa8a1e68a053fb59ee6d7717ce3dd08bb123234150d6c4f204b79c4babf6f96`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31091b97f76c2d01280909a82b19ec67be3458d552c83d1c3412bb1ada372478`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 375.6 KB (375595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe433c7244e17c134d5228a182610dd844018e175f0b7156d52e7a52b8c86db`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c85d8d7af1aafc8bd20e85d1d8a691a264d31a4819e86d6c7312e07aee8304`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0070dbe9d2e0f165d892573932fb485610fd5fc96f45f8094a36f5058b12e5a`  
		Last Modified: Fri, 03 Oct 2025 15:52:17 GMT  
		Size: 20.8 MB (20789973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213aa569cb703a24a789f517fe56a6ae497c99175c3d2cd373c89fa1f1089b4e`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7de2afae7847412112e197ac1c25ec2a40c9581eea75463412a97252857436`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85316e22a17d0d25c44a17c27c81262dfc1d7b2a3ab2928fb437761164e0c9`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f657f72b51307aef095c995e842dc3864c6bab5f77c72502b408e99fde4c0555`  
		Last Modified: Fri, 03 Oct 2025 15:52:35 GMT  
		Size: 23.2 MB (23171772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc17bee33fd2a219b6c8c2e719be2eee0413c0498eabf36c7df35feacde51`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca46b7935b2586b3219f0dcbb26f056695aa4d2780b86eef9c123323d12e442`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40563864091199f7c4bd7971379390f2a0eb68602bd84363d0d619d389081a66`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120ec86946b04b2ce643f75ca4da1136e61282d75f9079ce2dbe6439377e191c`  
		Last Modified: Fri, 03 Oct 2025 15:52:19 GMT  
		Size: 22.6 MB (22592462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.5.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:805b80eb5838dff72fb60586d27489abce0602489110a4c8936a08781e407c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:28.5.0-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:ad136d080029be1c9cf7792be1903931d264f5381e42166d3f3e7f1cfb01ea39
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638399147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a2b67a7be1525f868135b1a1c818f62ea909ae749a6bb5b517794cd4079df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Fri, 03 Oct 2025 15:43:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:38 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:45:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:00 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:45:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:45:02 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:45:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:45:12 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eac7129a35b3f3d93c10663cb922ac94175a7659ab43177cd29b8385d27396`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736095fdc18733277b021a61df3a3e30ce7092927089af31f6692fda83cace32`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 387.0 KB (386985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d353df5347d8893329766ad323f55f264ba05d9a3aac24528687197623c4ce0`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b067755f7397460b020f2cc400bd867b894ced17e4c67e655baa97401f6df86`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cf9b648dddc92e1677712ec6e0bae6d9a44e3648499cd72518c52fb94fb638`  
		Last Modified: Fri, 03 Oct 2025 15:58:03 GMT  
		Size: 20.8 MB (20792951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2af40a7d166840f2088865abe2618fec08f1764ebf29f2c95eaad97a5808c09`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f0b14cc909cb5745c3ddf411f5554cb3266e8a84577d7ca3786d71658b0e1`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420ccf00c9a5ac48828c2db2e12d31e69b900387f51aa2e08fcf0d82d599fd3`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8df219328e6f8e13ea4ce0e6f4e259f30e86c01f2cf4b0e935b34d182f2d99e`  
		Last Modified: Fri, 03 Oct 2025 15:58:16 GMT  
		Size: 23.2 MB (23173234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557962edd46b4b31a288d5f51205186b0bbbe6d695dd9c58cf749f07272beded`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55536c08291034b8fd66f7eb66d704bdd91734ed084ef651a0e6def838bd3ddf`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0bc4bd86cc52355181c183581a4717dbd9fa11425954465150b60ddc54db89`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c62fdb98b4bcde258cbda8487f9c4beacc78ab1e94f47db066289a37859dc0c`  
		Last Modified: Fri, 03 Oct 2025 15:58:01 GMT  
		Size: 22.6 MB (22594497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:9346c5506bb395e8d543072b8a42e55b6ac4c1ee2bb49ea1e6dbcdae058d6413
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

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:d5eea7f642a97e37c6cfb144bbf1c621a921d6bd6770925ca46083b6022e72ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76252652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5318c07034b1070773327332274ae100cfd2b187005a9b16f0560bcaf24f6374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:b0a855e3980a26a067b2d2a0781a2320c0ebb0b95cdd8969e3d1e63c41977d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9a5a518442282d243de3bf9659aab9d1324488d38cf20df6f68901e7a70638`

```dockerfile
```

-	Layers:
	-	`sha256:b23b75fb095cd2bcd99a74b495c36431098c714483d3aee226f206d2f69e78d9`  
		Last Modified: Fri, 03 Oct 2025 17:07:47 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:d7381fa06c8275c17d5e128e8ffe09b5da39eb3e8af48dd9b249316673239c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71190674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f458ec5b7496b07e3c6124e1edb26f921eb5e0291749ec9f7fb91d2be49adcf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:288801d6b3cdcdd95811bed6b33669ba7e4a9291f0803185af8cba15f3a43326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c159a7f1feae003fde9b008e8ea0a16bb293f6dc4a2131b493431ba075f28d4`

```dockerfile
```

-	Layers:
	-	`sha256:fb2fa30f269ea814e093ddff016eaecae13a50ff05d306e058913baf73667f5c`  
		Last Modified: Fri, 03 Oct 2025 17:07:50 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:bb7ef8a43ddb42bea13ec4c076ada0fb84a1187d43d5a485d1857244574d25dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70181198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b28aaf2092e123a0a50c48ec059da72a6b792fc5ad10d81c3c61e0f4f57e412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:b53b2a0dfffaf54e3c1624ca1acfe05f386da5c9a30462d4f81b2ac6efbad288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e3716ca95c952691eb8a96e068b1721637e70962ee86e71f5249766dc0ce19`

```dockerfile
```

-	Layers:
	-	`sha256:fda163a204484dc73af895db49f72864ac1701fb57029233d7ddc220474c8610`  
		Last Modified: Fri, 03 Oct 2025 17:07:53 GMT  
		Size: 38.3 KB (38282 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c0724b17cc1213826a3286add14ace28d271de874fa36db2ee89bd4dace4f3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71652939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dffc628b273a3882ea3e3ba84bb32e497b0a22f0c102b4d59362d4fe31fcac6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:522c2cc4ffb9267687aef6f8d72730ea70ceca998330ee32f74c9816c9a1acbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b98ac9778851ce1834f2ea2b1f14805861737c19429ba5d5ad7902bd7ded272`

```dockerfile
```

-	Layers:
	-	`sha256:bb5f4b80b573216b93fcd1b186a648d54c90b671162a8e1cf7cac20bc8679899`  
		Last Modified: Fri, 03 Oct 2025 17:07:56 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

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

## `docker:latest`

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

### `docker:latest` - linux; amd64

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

### `docker:latest` - unknown; unknown

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

### `docker:latest` - linux; arm variant v6

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

### `docker:latest` - unknown; unknown

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

### `docker:latest` - linux; arm variant v7

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

### `docker:latest` - unknown; unknown

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

### `docker:latest` - linux; arm64 variant v8

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

### `docker:latest` - unknown; unknown

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

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:0ef80f9aee78421ad00cb9465c8d1f248f547c926315728845aa35ddc93b63d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `docker:windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:ad136d080029be1c9cf7792be1903931d264f5381e42166d3f3e7f1cfb01ea39
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638399147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a2b67a7be1525f868135b1a1c818f62ea909ae749a6bb5b517794cd4079df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Fri, 03 Oct 2025 15:43:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:38 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:45:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:00 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:45:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:45:02 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:45:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:45:12 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eac7129a35b3f3d93c10663cb922ac94175a7659ab43177cd29b8385d27396`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736095fdc18733277b021a61df3a3e30ce7092927089af31f6692fda83cace32`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 387.0 KB (386985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d353df5347d8893329766ad323f55f264ba05d9a3aac24528687197623c4ce0`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b067755f7397460b020f2cc400bd867b894ced17e4c67e655baa97401f6df86`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cf9b648dddc92e1677712ec6e0bae6d9a44e3648499cd72518c52fb94fb638`  
		Last Modified: Fri, 03 Oct 2025 15:58:03 GMT  
		Size: 20.8 MB (20792951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2af40a7d166840f2088865abe2618fec08f1764ebf29f2c95eaad97a5808c09`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f0b14cc909cb5745c3ddf411f5554cb3266e8a84577d7ca3786d71658b0e1`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420ccf00c9a5ac48828c2db2e12d31e69b900387f51aa2e08fcf0d82d599fd3`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8df219328e6f8e13ea4ce0e6f4e259f30e86c01f2cf4b0e935b34d182f2d99e`  
		Last Modified: Fri, 03 Oct 2025 15:58:16 GMT  
		Size: 23.2 MB (23173234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557962edd46b4b31a288d5f51205186b0bbbe6d695dd9c58cf749f07272beded`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55536c08291034b8fd66f7eb66d704bdd91734ed084ef651a0e6def838bd3ddf`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0bc4bd86cc52355181c183581a4717dbd9fa11425954465150b60ddc54db89`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c62fdb98b4bcde258cbda8487f9c4beacc78ab1e94f47db066289a37859dc0c`  
		Last Modified: Fri, 03 Oct 2025 15:58:01 GMT  
		Size: 22.6 MB (22594497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:beb061eb6549b25fd99d8cabf410d457746a606589a7c2ae5aaf3f93da667b34
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349086539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5cb3226376ec4297559382e05ed2b5b66cccb4f94ae0332cb304ad7ccf0335`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 03 Oct 2025 15:43:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:12 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:44:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:29 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:44:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:44:32 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:44:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:44:51 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa8a1e68a053fb59ee6d7717ce3dd08bb123234150d6c4f204b79c4babf6f96`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31091b97f76c2d01280909a82b19ec67be3458d552c83d1c3412bb1ada372478`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 375.6 KB (375595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe433c7244e17c134d5228a182610dd844018e175f0b7156d52e7a52b8c86db`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c85d8d7af1aafc8bd20e85d1d8a691a264d31a4819e86d6c7312e07aee8304`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0070dbe9d2e0f165d892573932fb485610fd5fc96f45f8094a36f5058b12e5a`  
		Last Modified: Fri, 03 Oct 2025 15:52:17 GMT  
		Size: 20.8 MB (20789973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213aa569cb703a24a789f517fe56a6ae497c99175c3d2cd373c89fa1f1089b4e`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7de2afae7847412112e197ac1c25ec2a40c9581eea75463412a97252857436`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85316e22a17d0d25c44a17c27c81262dfc1d7b2a3ab2928fb437761164e0c9`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f657f72b51307aef095c995e842dc3864c6bab5f77c72502b408e99fde4c0555`  
		Last Modified: Fri, 03 Oct 2025 15:52:35 GMT  
		Size: 23.2 MB (23171772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc17bee33fd2a219b6c8c2e719be2eee0413c0498eabf36c7df35feacde51`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca46b7935b2586b3219f0dcbb26f056695aa4d2780b86eef9c123323d12e442`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40563864091199f7c4bd7971379390f2a0eb68602bd84363d0d619d389081a66`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120ec86946b04b2ce643f75ca4da1136e61282d75f9079ce2dbe6439377e191c`  
		Last Modified: Fri, 03 Oct 2025 15:52:19 GMT  
		Size: 22.6 MB (22592462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0ba9c9b2ed57e14d1f504dee1e427cfba36d706f3fb4aed03f518b850f8f59b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull docker@sha256:beb061eb6549b25fd99d8cabf410d457746a606589a7c2ae5aaf3f93da667b34
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2349086539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5cb3226376ec4297559382e05ed2b5b66cccb4f94ae0332cb304ad7ccf0335`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 03 Oct 2025 15:43:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:12 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:44:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:29 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:44:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:44:32 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:44:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:44:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:44:51 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa8a1e68a053fb59ee6d7717ce3dd08bb123234150d6c4f204b79c4babf6f96`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31091b97f76c2d01280909a82b19ec67be3458d552c83d1c3412bb1ada372478`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 375.6 KB (375595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe433c7244e17c134d5228a182610dd844018e175f0b7156d52e7a52b8c86db`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c85d8d7af1aafc8bd20e85d1d8a691a264d31a4819e86d6c7312e07aee8304`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0070dbe9d2e0f165d892573932fb485610fd5fc96f45f8094a36f5058b12e5a`  
		Last Modified: Fri, 03 Oct 2025 15:52:17 GMT  
		Size: 20.8 MB (20789973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213aa569cb703a24a789f517fe56a6ae497c99175c3d2cd373c89fa1f1089b4e`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7de2afae7847412112e197ac1c25ec2a40c9581eea75463412a97252857436`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85316e22a17d0d25c44a17c27c81262dfc1d7b2a3ab2928fb437761164e0c9`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f657f72b51307aef095c995e842dc3864c6bab5f77c72502b408e99fde4c0555`  
		Last Modified: Fri, 03 Oct 2025 15:52:35 GMT  
		Size: 23.2 MB (23171772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc17bee33fd2a219b6c8c2e719be2eee0413c0498eabf36c7df35feacde51`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca46b7935b2586b3219f0dcbb26f056695aa4d2780b86eef9c123323d12e442`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40563864091199f7c4bd7971379390f2a0eb68602bd84363d0d619d389081a66`  
		Last Modified: Fri, 03 Oct 2025 15:52:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120ec86946b04b2ce643f75ca4da1136e61282d75f9079ce2dbe6439377e191c`  
		Last Modified: Fri, 03 Oct 2025 15:52:19 GMT  
		Size: 22.6 MB (22592462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:805b80eb5838dff72fb60586d27489abce0602489110a4c8936a08781e407c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull docker@sha256:ad136d080029be1c9cf7792be1903931d264f5381e42166d3f3e7f1cfb01ea39
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3638399147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8a2b67a7be1525f868135b1a1c818f62ea909ae749a6bb5b517794cd4079df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Fri, 03 Oct 2025 15:43:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Oct 2025 15:44:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Oct 2025 15:44:38 GMT
ENV DOCKER_VERSION=28.5.0
# Fri, 03 Oct 2025 15:44:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.0.zip
# Fri, 03 Oct 2025 15:45:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:00 GMT
ENV DOCKER_BUILDX_VERSION=0.29.0
# Fri, 03 Oct 2025 15:45:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.0/buildx-v0.29.0.windows-amd64.exe
# Fri, 03 Oct 2025 15:45:02 GMT
ENV DOCKER_BUILDX_SHA256=d58e5a3eeef59fff460cc2a7f3b501222ce137e6afeb4cc528c658d9363cac26
# Fri, 03 Oct 2025 15:45:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.4
# Fri, 03 Oct 2025 15:45:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.4/docker-compose-windows-x86_64.exe
# Fri, 03 Oct 2025 15:45:12 GMT
ENV DOCKER_COMPOSE_SHA256=6b3bccfabcdd172e1d9e15d011b54c9b5b13b93b1153148108f55e4349055955
# Fri, 03 Oct 2025 15:45:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eac7129a35b3f3d93c10663cb922ac94175a7659ab43177cd29b8385d27396`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736095fdc18733277b021a61df3a3e30ce7092927089af31f6692fda83cace32`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 387.0 KB (386985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d353df5347d8893329766ad323f55f264ba05d9a3aac24528687197623c4ce0`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b067755f7397460b020f2cc400bd867b894ced17e4c67e655baa97401f6df86`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cf9b648dddc92e1677712ec6e0bae6d9a44e3648499cd72518c52fb94fb638`  
		Last Modified: Fri, 03 Oct 2025 15:58:03 GMT  
		Size: 20.8 MB (20792951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2af40a7d166840f2088865abe2618fec08f1764ebf29f2c95eaad97a5808c09`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f0b14cc909cb5745c3ddf411f5554cb3266e8a84577d7ca3786d71658b0e1`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420ccf00c9a5ac48828c2db2e12d31e69b900387f51aa2e08fcf0d82d599fd3`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8df219328e6f8e13ea4ce0e6f4e259f30e86c01f2cf4b0e935b34d182f2d99e`  
		Last Modified: Fri, 03 Oct 2025 15:58:16 GMT  
		Size: 23.2 MB (23173234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557962edd46b4b31a288d5f51205186b0bbbe6d695dd9c58cf749f07272beded`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55536c08291034b8fd66f7eb66d704bdd91734ed084ef651a0e6def838bd3ddf`  
		Last Modified: Fri, 03 Oct 2025 15:58:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0bc4bd86cc52355181c183581a4717dbd9fa11425954465150b60ddc54db89`  
		Last Modified: Fri, 03 Oct 2025 15:57:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c62fdb98b4bcde258cbda8487f9c4beacc78ab1e94f47db066289a37859dc0c`  
		Last Modified: Fri, 03 Oct 2025 15:58:01 GMT  
		Size: 22.6 MB (22594497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-1809`](#docker28-windowsservercore-1809)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.0`](#docker280)
-	[`docker:28.0-cli`](#docker280-cli)
-	[`docker:28.0-dind`](#docker280-dind)
-	[`docker:28.0-dind-rootless`](#docker280-dind-rootless)
-	[`docker:28.0-windowsservercore`](#docker280-windowsservercore)
-	[`docker:28.0-windowsservercore-1809`](#docker280-windowsservercore-1809)
-	[`docker:28.0-windowsservercore-ltsc2022`](#docker280-windowsservercore-ltsc2022)
-	[`docker:28.0-windowsservercore-ltsc2025`](#docker280-windowsservercore-ltsc2025)
-	[`docker:28.0.4`](#docker2804)
-	[`docker:28.0.4-alpine3.21`](#docker2804-alpine321)
-	[`docker:28.0.4-cli`](#docker2804-cli)
-	[`docker:28.0.4-cli-alpine3.21`](#docker2804-cli-alpine321)
-	[`docker:28.0.4-dind`](#docker2804-dind)
-	[`docker:28.0.4-dind-alpine3.21`](#docker2804-dind-alpine321)
-	[`docker:28.0.4-dind-rootless`](#docker2804-dind-rootless)
-	[`docker:28.0.4-windowsservercore`](#docker2804-windowsservercore)
-	[`docker:28.0.4-windowsservercore-1809`](#docker2804-windowsservercore-1809)
-	[`docker:28.0.4-windowsservercore-ltsc2022`](#docker2804-windowsservercore-ltsc2022)
-	[`docker:28.0.4-windowsservercore-ltsc2025`](#docker2804-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:4924fece44d61eeec47f619a4c35cd70fa2a31cd36b6283943a122369549fb82
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
$ docker pull docker@sha256:c4b520b9a63e5115f6d9843c62522b6560756164554b5c9a3a9c20bcb552e3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141638455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7ea23310b3fff4bbef36e8b08d5235dffa4d1aef78d84779d009e52daf7199`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:147e7c33d9e0781984a50137a65ab2801e4cbb5f519794b0b305a0f10539b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae01ef61862c7d28c4e48daaf3bcab61392d36b8995d1a304c28484403104db7`

```dockerfile
```

-	Layers:
	-	`sha256:01580a980dc523731ae2593398ec17f2aee10cc2224a12eec7f40edd279f0c15`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:acd9933ad265f50391c17d366e6b8b2774345d83655ac9eb52b18eb42a1140dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132245125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811d9a6156b3817de2198edbebe33a6c8cc87db51c522c2551723096b7fe9e55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0bf2e3301b433097f02a64cb68c64719a9d601c4c4e8199753a97d2eca08f5`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 7.0 MB (7036910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bea1f449ae4828750de8d364675e658773d2395554fb8f6e5b27abf6650d4a`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50285df7a34e25624ea34e42fcd0a315257b55c57443f5e1c9f7d87a64844be`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e48adef24818df5086795a0b59c0920fcbeab02b52b14b3d2948aa8dae560e`  
		Last Modified: Tue, 25 Mar 2025 21:57:04 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e6cc859de766f4621a9057c7a584c0bae06240f47f49125d0a53b0ccf2817`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b02adeb27e77008de20f43b04c15f9400674028dde877ca2c85db228d63833`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:a062c1bae3694f2dc57a86f1a0a31f0646edbe073ba3b5332b7ea703fc95439a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6e9ff128ff3dd627ea97a881ed9d45513bfbbdd3ae431e585925664bcb1073`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b93d052b010bed3a7a457c00779ec2ccbd5200b802737da2302f23898bf0d`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:5aec0cd9338b8c87a48d32538f1126aa1ea564bab5e0f88c2c3711887986e8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130582961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c8e6ea19a06349bd3fff8b36b6edc473d618f00fa98e0cf2b2245a333ec036`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e99727b81f4572b85e4f50bb748f74834c084c2be0336f0861ec92f578aab1d`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 6.4 MB (6366260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a406bc3246700b25d15b9a21a2c297aa03294574c920835f8e279fd40a99248c`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274227b3189ab05a7bcf8b5bca0a03e2da5a20fb0b29a005f653109f8307f13f`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d83b5ee45ba8b5cca7c66e593eed8890a19086546cc5b73e7aef977003052f7`  
		Last Modified: Tue, 25 Mar 2025 21:57:07 GMT  
		Size: 55.7 MB (55741247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82e270939ba77481d58f0731a8190051ed151ddeaf18ae9c71a711f5b23b19`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468d9090d7bb5417d46894a189d2c10a477709d8025de53c9684d708d936fbc`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:ef399f39c3375b2b26eef2b816ef0bc918beeebc2df752d98f6c8ff3d8af56e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba96e9df1e9b4b3f8af60be57bcef0cf7e05ce7cbdc423ad8100ccc83513eff`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a457447e187312ae0fcbe8833d37bc3524eca92d733dd57cbb2e2ce0e584a`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:223d046021f324792db4fbd1396746b63ffb93f00861ea390d7fbbaf392585e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132967037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a69ac0c9fe38a13675c478cc22e49748128d1bab3e99eb0e2c6be27dfd7d3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:64a2e28c40f0a0dfc87d02ef347ac0bc427ba0ffcc4b786312c6c94774615d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa29ab3f950e5f22976c193db0590a2c8448a680d52dc5423896788a0af100b1`

```dockerfile
```

-	Layers:
	-	`sha256:8d5656be0e9638a2cdce9ab5a83f7e3464efca3bceb222bd596af0b060d128a9`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:c5e0b27a15f49b571f968defe19cc9a072d531ee90300ba5a1d2ea4dffa760e4
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
$ docker pull docker@sha256:23b5b1a900c5676eaee32c38dbdf727a37a6ace0c5980885a9ec21da619608f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74456477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6539186f04a7291f29d299010b9ab4b55d15e95c6b0e5a7ed5343225ebaeca47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1133514976c34d263934880176c7466336c52b261e542275beeba2b0e5917292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966754ba178f5be30b512dcf67885f9543d39a53d5299d73a475f5f65ab3c216`

```dockerfile
```

-	Layers:
	-	`sha256:45b02f14e5b651223c3c46b95436ebab9917894f4d446223811103debafdf45f`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1c3cb277d90221fcd05b69ef6a0f498fe66939317b75f5018c1cc3ca76387ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69371203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a418a759b70319d7bb3094bb667c222c2e70891d056076f8f9348a047f66c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b03cfc87f30735938381fcba67b7d48fb8e172a0426952a5c613717a6ba5126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0842d83a60027d875a0955c917c99c19935a96ef9827c37e655d72673286f2`

```dockerfile
```

-	Layers:
	-	`sha256:75aa001f9acf4b60bb11607334f3dfb7fc38dab3bc1b6fc5d19c4e11403b62a1`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:a38772a4376f984332843064dcd64529345698a31a522d9e743987c6e9fcf062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68383198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272d56ce0b6289e34fdc69a110e200627da4edddfd7d75df5a3d35e50091e40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a80bd51374d59cccbe39550e29f3c75a4898d5c2b280388e8af740da9b07164b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f168959aace97d67eaf1304c91ac8dfbee2d113d5d8603c5813758c285776`

```dockerfile
```

-	Layers:
	-	`sha256:2810d6f734119f2a44d1165a8f025decfb025d213521b3e85924d093fb8f1354`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a00c0bc47f8908b1a966cb40ffdd06470593dc098b4d6c7ac356c7f7134f9de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70172005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0075144f78e3fc8d804eb929c2cf866a2ae0295c47f80dd57a7074863ba2736b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c97d9cee1f1276f1b5c4f148387ce7f92a0f69d5d5805e39bf0a839fb8305949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7899ba69a193c95da9272216327b56babf9364894e32734aa60a0fc96bd2c0`

```dockerfile
```

-	Layers:
	-	`sha256:225c9a7352f7eb6df35d3bd7852ecf7eb0f840312b66c6ae6e88d4847326bf7e`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:4924fece44d61eeec47f619a4c35cd70fa2a31cd36b6283943a122369549fb82
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
$ docker pull docker@sha256:c4b520b9a63e5115f6d9843c62522b6560756164554b5c9a3a9c20bcb552e3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141638455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7ea23310b3fff4bbef36e8b08d5235dffa4d1aef78d84779d009e52daf7199`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:147e7c33d9e0781984a50137a65ab2801e4cbb5f519794b0b305a0f10539b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae01ef61862c7d28c4e48daaf3bcab61392d36b8995d1a304c28484403104db7`

```dockerfile
```

-	Layers:
	-	`sha256:01580a980dc523731ae2593398ec17f2aee10cc2224a12eec7f40edd279f0c15`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:acd9933ad265f50391c17d366e6b8b2774345d83655ac9eb52b18eb42a1140dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132245125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811d9a6156b3817de2198edbebe33a6c8cc87db51c522c2551723096b7fe9e55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0bf2e3301b433097f02a64cb68c64719a9d601c4c4e8199753a97d2eca08f5`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 7.0 MB (7036910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bea1f449ae4828750de8d364675e658773d2395554fb8f6e5b27abf6650d4a`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50285df7a34e25624ea34e42fcd0a315257b55c57443f5e1c9f7d87a64844be`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e48adef24818df5086795a0b59c0920fcbeab02b52b14b3d2948aa8dae560e`  
		Last Modified: Tue, 25 Mar 2025 21:57:04 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e6cc859de766f4621a9057c7a584c0bae06240f47f49125d0a53b0ccf2817`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b02adeb27e77008de20f43b04c15f9400674028dde877ca2c85db228d63833`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a062c1bae3694f2dc57a86f1a0a31f0646edbe073ba3b5332b7ea703fc95439a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6e9ff128ff3dd627ea97a881ed9d45513bfbbdd3ae431e585925664bcb1073`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b93d052b010bed3a7a457c00779ec2ccbd5200b802737da2302f23898bf0d`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5aec0cd9338b8c87a48d32538f1126aa1ea564bab5e0f88c2c3711887986e8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130582961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c8e6ea19a06349bd3fff8b36b6edc473d618f00fa98e0cf2b2245a333ec036`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e99727b81f4572b85e4f50bb748f74834c084c2be0336f0861ec92f578aab1d`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 6.4 MB (6366260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a406bc3246700b25d15b9a21a2c297aa03294574c920835f8e279fd40a99248c`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274227b3189ab05a7bcf8b5bca0a03e2da5a20fb0b29a005f653109f8307f13f`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d83b5ee45ba8b5cca7c66e593eed8890a19086546cc5b73e7aef977003052f7`  
		Last Modified: Tue, 25 Mar 2025 21:57:07 GMT  
		Size: 55.7 MB (55741247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82e270939ba77481d58f0731a8190051ed151ddeaf18ae9c71a711f5b23b19`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468d9090d7bb5417d46894a189d2c10a477709d8025de53c9684d708d936fbc`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ef399f39c3375b2b26eef2b816ef0bc918beeebc2df752d98f6c8ff3d8af56e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba96e9df1e9b4b3f8af60be57bcef0cf7e05ce7cbdc423ad8100ccc83513eff`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a457447e187312ae0fcbe8833d37bc3524eca92d733dd57cbb2e2ce0e584a`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:223d046021f324792db4fbd1396746b63ffb93f00861ea390d7fbbaf392585e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132967037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a69ac0c9fe38a13675c478cc22e49748128d1bab3e99eb0e2c6be27dfd7d3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:64a2e28c40f0a0dfc87d02ef347ac0bc427ba0ffcc4b786312c6c94774615d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa29ab3f950e5f22976c193db0590a2c8448a680d52dc5423896788a0af100b1`

```dockerfile
```

-	Layers:
	-	`sha256:8d5656be0e9638a2cdce9ab5a83f7e3464efca3bceb222bd596af0b060d128a9`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:a5090d7c11c05a862ae22fbb478c62a4e9643fa431eaf7a9a7812fef7a67a859
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c06be5bc3b0e24f7f4b5ffbbcd8ca9ab02519562d691cb456f5d6b98f29c39c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159797561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13bdb47aeff8daa8094c59742ad7afc5ad9e580eec39dd8f76368cc62b7ce87`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded84039e564b9475ac7b125bcf4fb9502f33f947c0ddd3536f43effc60d6a54`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 986.6 KB (986584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40aafab5cc59e8f5cb5e26668f818b42db849fe877e95d7a3529e90d4a3c8bd9`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6da82905025ead3a593c912e1918488b0874da3fe3299e2a42bdb1cc934be3`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654321f2b23758f8b02e88231bb7f7f6dee732758055aea66fd4dce0973416a`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 17.2 MB (17171184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3959b7e18a4fbdba386c18493c321ff4ca8830103acfcd3d187205a34cd112a9`  
		Last Modified: Tue, 25 Mar 2025 22:07:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bca820a790106f4866c59edf3d44fe79e09e9fa614e0a9f876c8919a5083f221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3323bffc2b5312b105253768c2c98037a504a39c4c7af0e7d7e1520aa6fb44`

```dockerfile
```

-	Layers:
	-	`sha256:e38eb0dfbf00e9814744fe5742ba05c41d5fa87629943046da2c159f210fa232`  
		Last Modified: Tue, 25 Mar 2025 22:07:39 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18a046138bef9eba3e6cf40129dd21388ec0a65d78a43003f1d93c8c8a4a075a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153264716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaf59ab004246a3948261b2eb47e4829eb00058acc9da25a1df6cff853a3f5b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cec22076d04d53956a39ca4217e9df0953e2089d2e7bc1927bef33d1228f4ce`  
		Last Modified: Tue, 25 Mar 2025 22:07:55 GMT  
		Size: 1.0 MB (1014208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a832bc3a23d3053414b32a049f9513b8654a574152e2b5d59d5616d4ab21e7`  
		Last Modified: Tue, 25 Mar 2025 22:07:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9308d557624dd27d66f0684ea0043bab12df8101320568cc69a8cdfead8367ed`  
		Last Modified: Tue, 25 Mar 2025 22:07:54 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48c2c7bc6b3fe5cf98c66408a3d4a051eaf3a7ef3c1aff1d2ebcb92c7d5e394`  
		Last Modified: Tue, 25 Mar 2025 22:07:55 GMT  
		Size: 19.3 MB (19282130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe93e7f39bff732dc1b6bad18045bb6d77a906b8672b73f15e5437aecdc1b9e`  
		Last Modified: Tue, 25 Mar 2025 22:07:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e4e4429f44acdd9a71ddee3e2e7db9d16cba204c73232fab6e85b41970d037dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7504d9409f225cb85c9078ba600e2b30c8e50444f521f6fa12ebd5a20c6703ae`

```dockerfile
```

-	Layers:
	-	`sha256:6d6cd4b0e7f4511463caf0aa1389476e27c5b8ef1a2ca5681666010a6d33f5de`  
		Last Modified: Tue, 25 Mar 2025 22:07:54 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:fdbf04adec3070897345d1e057af86328464a4e11f3f7426fc7b27e94e2eb517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:37fbf58c618a1e257ff62a5c17597a58c612390d9b8248b12de620ff0dc27116
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974098228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d876f863caff9ced5d2166306316ea67c3e8f29ecd77f820b472be5e597514de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 21:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:36:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:36:02 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:36:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:36:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:14 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:36:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:36:16 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:36:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:36:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230d8f91a46ec72be09fa76d5ed5c5c953b39e08a445f5dc09dacc9ee44eb74a`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497744dd92652df503964233d52071afe6b6da69fcc9d699ecdef8a81132716`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 393.8 KB (393794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bbe029cc51bac0aa9cdd3ec3325e113f38f3632cef853c3d488b1b1641adae`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e6465d36bb7dd3cbd69b2e9a38b3544b7eab714dd64a6c38788e616627500b`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9179050a0c68ba8475bf29ed21dd34e7d54d5f314a7ac42b2fca85710f90f32`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 19.9 MB (19904481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3871cbf913d4865bf43a87c7cbf2227b2705afa74b1281dba34fe25af1a73e5b`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae86510368ad79d177019fd99371ebda2255844ae98eed60c771294d11b158db`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1c6e4bc9abf47f577d2fea496c8dd7cd245ef59f6342b8274eb1e1bfe3deb3`  
		Last Modified: Tue, 25 Mar 2025 21:36:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944b89a3759e186bd3d1e0373910a72d0c398b453c235e4e3859f193aafb6f7d`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.8 MB (22807812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3fe3114e244b2f87a8272a1e53a7be89778c0f0609da78972fa83adf80028`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3bb7f5e52b615856b2468cacce7cfda132ef42d917ec6c7b1ed45144fd6574`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711261a97010fbb377d12b5a0adc589d06fbb8b0d5fe5b15131e5124210a14d5`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0375e49eb81a62ee6208594c9fd6c9c2faede214b7a1c4d4a263bd1908edb436`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.3 MB (22332711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:f99d03d930f93e2749004c210255ac7f6b52149af0a79f27716da370fa7b1eb6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335275907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c5fa0da0dfcdf03eeb0a5cc8d07e757bd37f4f77b4f8a064d43809c323c1c8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 25 Mar 2025 21:37:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:38:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:38:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:38:21 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:38:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:38:30 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:38:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e87728e165e6772cede047713a447fd6e30659d8dd65ce204231ed4a7dbb0e`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe917f396787792b92fc9c8f5959b2f8be7522c5b2d400aed59e46867d04a`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 371.5 KB (371494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c896757855fa4e3de01285214ef7138cbe36c12ca479b1124f575ee219dcac`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4036332907e21a93b9f46503d71b483e433e9268f61846e8fd3669ad8e8260`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f2151a5c434f05d2e41c3bf031037cf88d7a152683a0aa34b1e6d50e55f5d6`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 19.9 MB (19873533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd21b973a1b5c558975227864cfb89ba209e894f4a446b40afd17ec3b9ee9a80`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce9542ef040e9bf201f9a54875111a9eba23bb63caf4a022c127d73bb8fc7b8`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb91e206b539328afd55e6043c5c2825cfc67484bb8ff7055f76034431f02a83`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111bedc1382fe6bceb4dc527c273e3e88d670a978f867793f8cb11dace8ab00`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.8 MB (22775231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9293f4095824ab934e2ea69a23a4ea9e5b880f5e5d4a0f1bbf1cc5543e5a9`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f1c82a5ed7da58754739b095aac5f1ec0fe3aea0d48069290cfc0c9af4c4d`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608603ddb53750c36f5d27ef3c6d70b3d90ebe2430701772a11a1dc8ab625795`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63caecab4c5855f0c5198d61e2ec9cb95d046b983b51c66bdafcfe9383dad979`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.3 MB (22302869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:a07b73a00a3c52cf508c570e374efc24be0c453d86c9452fcea303ba531ffc8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216893552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a9a00b1e30a51e5c8dc78b5d38184a68cda33f84d782e8bf6ef53aa9e235d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 21:33:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:34:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:34:13 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:34:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:34:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:25 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:34:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:34:27 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:34:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:34:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:34:38 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:34:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a524a0e9cb7afa4d4cd71cd32e949c44f21cba76046ad004d2d6d09870f93ca`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847dbfeb702fcf37b419ad4ed9aa7e21d43d27bf895a29d8da424b6b58d57dc`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 340.0 KB (339963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edce44d57bdec9498491ec04581f5193d08ac7cfe87170c1368d3f2456d40268`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c046029f114363dc51b43457767bcb3f623e3c8f32e8ca7f9b2db9d7972f56`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ee9950b1bd1e3a417a9674a6ed4ba90d4b0101a2aad3d904faf071830bd11`  
		Last Modified: Tue, 25 Mar 2025 21:34:58 GMT  
		Size: 19.9 MB (19859748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5786612fd2d55be281d632baaa5e172f6bd8458061b5ecf3bffedb71d6de9`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0a2088c740ff617b174a979824713e0ad78fe077aa205af5340a6aa886e39`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71a201934e91595d89a5cda2c3f1824c4766cda3ae640a1e8f7dd00e3a33ad`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dd615d0c7c6f688705646fd983a540cca62d8d975b8fd767e83954950ba82d`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.8 MB (22763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e870735d52bdad39865ea0295c463823531285214d901abdf128dca151e17c5`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e5d174601f7707cecf5521b4bdf1b1198187a4844a00a623a89d78257bdb1`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7fcbbabcb3464ee277100b9f6fd1c395109f1ce5de50e92adc5431a6beb04`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176d290ac87077c88ca4ce30853fd4d9020a6eb3dbc3df72610e011d5869d562`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.3 MB (22283549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:c8052ef5f90cd2fa3c44394fec8378a887db5d87c66f6d5af683b3082f4f3658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:a07b73a00a3c52cf508c570e374efc24be0c453d86c9452fcea303ba531ffc8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216893552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a9a00b1e30a51e5c8dc78b5d38184a68cda33f84d782e8bf6ef53aa9e235d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 21:33:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:34:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:34:13 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:34:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:34:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:25 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:34:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:34:27 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:34:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:34:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:34:38 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:34:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a524a0e9cb7afa4d4cd71cd32e949c44f21cba76046ad004d2d6d09870f93ca`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847dbfeb702fcf37b419ad4ed9aa7e21d43d27bf895a29d8da424b6b58d57dc`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 340.0 KB (339963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edce44d57bdec9498491ec04581f5193d08ac7cfe87170c1368d3f2456d40268`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c046029f114363dc51b43457767bcb3f623e3c8f32e8ca7f9b2db9d7972f56`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ee9950b1bd1e3a417a9674a6ed4ba90d4b0101a2aad3d904faf071830bd11`  
		Last Modified: Tue, 25 Mar 2025 21:34:58 GMT  
		Size: 19.9 MB (19859748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5786612fd2d55be281d632baaa5e172f6bd8458061b5ecf3bffedb71d6de9`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0a2088c740ff617b174a979824713e0ad78fe077aa205af5340a6aa886e39`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71a201934e91595d89a5cda2c3f1824c4766cda3ae640a1e8f7dd00e3a33ad`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dd615d0c7c6f688705646fd983a540cca62d8d975b8fd767e83954950ba82d`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.8 MB (22763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e870735d52bdad39865ea0295c463823531285214d901abdf128dca151e17c5`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e5d174601f7707cecf5521b4bdf1b1198187a4844a00a623a89d78257bdb1`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7fcbbabcb3464ee277100b9f6fd1c395109f1ce5de50e92adc5431a6beb04`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176d290ac87077c88ca4ce30853fd4d9020a6eb3dbc3df72610e011d5869d562`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.3 MB (22283549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ae68b9f2e53406551f2704648cf0197fc3499d7003d00f8dbde54b97cd9f1a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:f99d03d930f93e2749004c210255ac7f6b52149af0a79f27716da370fa7b1eb6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335275907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c5fa0da0dfcdf03eeb0a5cc8d07e757bd37f4f77b4f8a064d43809c323c1c8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 25 Mar 2025 21:37:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:38:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:38:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:38:21 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:38:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:38:30 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:38:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e87728e165e6772cede047713a447fd6e30659d8dd65ce204231ed4a7dbb0e`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe917f396787792b92fc9c8f5959b2f8be7522c5b2d400aed59e46867d04a`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 371.5 KB (371494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c896757855fa4e3de01285214ef7138cbe36c12ca479b1124f575ee219dcac`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4036332907e21a93b9f46503d71b483e433e9268f61846e8fd3669ad8e8260`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f2151a5c434f05d2e41c3bf031037cf88d7a152683a0aa34b1e6d50e55f5d6`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 19.9 MB (19873533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd21b973a1b5c558975227864cfb89ba209e894f4a446b40afd17ec3b9ee9a80`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce9542ef040e9bf201f9a54875111a9eba23bb63caf4a022c127d73bb8fc7b8`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb91e206b539328afd55e6043c5c2825cfc67484bb8ff7055f76034431f02a83`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111bedc1382fe6bceb4dc527c273e3e88d670a978f867793f8cb11dace8ab00`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.8 MB (22775231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9293f4095824ab934e2ea69a23a4ea9e5b880f5e5d4a0f1bbf1cc5543e5a9`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f1c82a5ed7da58754739b095aac5f1ec0fe3aea0d48069290cfc0c9af4c4d`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608603ddb53750c36f5d27ef3c6d70b3d90ebe2430701772a11a1dc8ab625795`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63caecab4c5855f0c5198d61e2ec9cb95d046b983b51c66bdafcfe9383dad979`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.3 MB (22302869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b25d93a59fbdb43e27ccd5ff42b9a530d1c07616c048664e2a9858300a0817ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:37fbf58c618a1e257ff62a5c17597a58c612390d9b8248b12de620ff0dc27116
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974098228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d876f863caff9ced5d2166306316ea67c3e8f29ecd77f820b472be5e597514de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 21:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:36:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:36:02 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:36:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:36:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:14 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:36:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:36:16 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:36:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:36:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230d8f91a46ec72be09fa76d5ed5c5c953b39e08a445f5dc09dacc9ee44eb74a`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497744dd92652df503964233d52071afe6b6da69fcc9d699ecdef8a81132716`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 393.8 KB (393794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bbe029cc51bac0aa9cdd3ec3325e113f38f3632cef853c3d488b1b1641adae`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e6465d36bb7dd3cbd69b2e9a38b3544b7eab714dd64a6c38788e616627500b`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9179050a0c68ba8475bf29ed21dd34e7d54d5f314a7ac42b2fca85710f90f32`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 19.9 MB (19904481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3871cbf913d4865bf43a87c7cbf2227b2705afa74b1281dba34fe25af1a73e5b`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae86510368ad79d177019fd99371ebda2255844ae98eed60c771294d11b158db`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1c6e4bc9abf47f577d2fea496c8dd7cd245ef59f6342b8274eb1e1bfe3deb3`  
		Last Modified: Tue, 25 Mar 2025 21:36:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944b89a3759e186bd3d1e0373910a72d0c398b453c235e4e3859f193aafb6f7d`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.8 MB (22807812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3fe3114e244b2f87a8272a1e53a7be89778c0f0609da78972fa83adf80028`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3bb7f5e52b615856b2468cacce7cfda132ef42d917ec6c7b1ed45144fd6574`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711261a97010fbb377d12b5a0adc589d06fbb8b0d5fe5b15131e5124210a14d5`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0375e49eb81a62ee6208594c9fd6c9c2faede214b7a1c4d4a263bd1908edb436`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.3 MB (22332711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0`

```console
$ docker pull docker@sha256:4924fece44d61eeec47f619a4c35cd70fa2a31cd36b6283943a122369549fb82
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

### `docker:28.0` - linux; amd64

```console
$ docker pull docker@sha256:c4b520b9a63e5115f6d9843c62522b6560756164554b5c9a3a9c20bcb552e3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141638455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7ea23310b3fff4bbef36e8b08d5235dffa4d1aef78d84779d009e52daf7199`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:147e7c33d9e0781984a50137a65ab2801e4cbb5f519794b0b305a0f10539b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae01ef61862c7d28c4e48daaf3bcab61392d36b8995d1a304c28484403104db7`

```dockerfile
```

-	Layers:
	-	`sha256:01580a980dc523731ae2593398ec17f2aee10cc2224a12eec7f40edd279f0c15`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:acd9933ad265f50391c17d366e6b8b2774345d83655ac9eb52b18eb42a1140dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132245125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811d9a6156b3817de2198edbebe33a6c8cc87db51c522c2551723096b7fe9e55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0bf2e3301b433097f02a64cb68c64719a9d601c4c4e8199753a97d2eca08f5`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 7.0 MB (7036910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bea1f449ae4828750de8d364675e658773d2395554fb8f6e5b27abf6650d4a`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50285df7a34e25624ea34e42fcd0a315257b55c57443f5e1c9f7d87a64844be`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e48adef24818df5086795a0b59c0920fcbeab02b52b14b3d2948aa8dae560e`  
		Last Modified: Tue, 25 Mar 2025 21:57:04 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e6cc859de766f4621a9057c7a584c0bae06240f47f49125d0a53b0ccf2817`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b02adeb27e77008de20f43b04c15f9400674028dde877ca2c85db228d63833`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:a062c1bae3694f2dc57a86f1a0a31f0646edbe073ba3b5332b7ea703fc95439a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6e9ff128ff3dd627ea97a881ed9d45513bfbbdd3ae431e585925664bcb1073`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b93d052b010bed3a7a457c00779ec2ccbd5200b802737da2302f23898bf0d`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:5aec0cd9338b8c87a48d32538f1126aa1ea564bab5e0f88c2c3711887986e8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130582961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c8e6ea19a06349bd3fff8b36b6edc473d618f00fa98e0cf2b2245a333ec036`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e99727b81f4572b85e4f50bb748f74834c084c2be0336f0861ec92f578aab1d`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 6.4 MB (6366260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a406bc3246700b25d15b9a21a2c297aa03294574c920835f8e279fd40a99248c`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274227b3189ab05a7bcf8b5bca0a03e2da5a20fb0b29a005f653109f8307f13f`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d83b5ee45ba8b5cca7c66e593eed8890a19086546cc5b73e7aef977003052f7`  
		Last Modified: Tue, 25 Mar 2025 21:57:07 GMT  
		Size: 55.7 MB (55741247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82e270939ba77481d58f0731a8190051ed151ddeaf18ae9c71a711f5b23b19`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468d9090d7bb5417d46894a189d2c10a477709d8025de53c9684d708d936fbc`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:ef399f39c3375b2b26eef2b816ef0bc918beeebc2df752d98f6c8ff3d8af56e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba96e9df1e9b4b3f8af60be57bcef0cf7e05ce7cbdc423ad8100ccc83513eff`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a457447e187312ae0fcbe8833d37bc3524eca92d733dd57cbb2e2ce0e584a`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:223d046021f324792db4fbd1396746b63ffb93f00861ea390d7fbbaf392585e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132967037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a69ac0c9fe38a13675c478cc22e49748128d1bab3e99eb0e2c6be27dfd7d3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:64a2e28c40f0a0dfc87d02ef347ac0bc427ba0ffcc4b786312c6c94774615d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa29ab3f950e5f22976c193db0590a2c8448a680d52dc5423896788a0af100b1`

```dockerfile
```

-	Layers:
	-	`sha256:8d5656be0e9638a2cdce9ab5a83f7e3464efca3bceb222bd596af0b060d128a9`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-cli`

```console
$ docker pull docker@sha256:c5e0b27a15f49b571f968defe19cc9a072d531ee90300ba5a1d2ea4dffa760e4
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

### `docker:28.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:23b5b1a900c5676eaee32c38dbdf727a37a6ace0c5980885a9ec21da619608f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74456477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6539186f04a7291f29d299010b9ab4b55d15e95c6b0e5a7ed5343225ebaeca47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1133514976c34d263934880176c7466336c52b261e542275beeba2b0e5917292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966754ba178f5be30b512dcf67885f9543d39a53d5299d73a475f5f65ab3c216`

```dockerfile
```

-	Layers:
	-	`sha256:45b02f14e5b651223c3c46b95436ebab9917894f4d446223811103debafdf45f`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1c3cb277d90221fcd05b69ef6a0f498fe66939317b75f5018c1cc3ca76387ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69371203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a418a759b70319d7bb3094bb667c222c2e70891d056076f8f9348a047f66c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b03cfc87f30735938381fcba67b7d48fb8e172a0426952a5c613717a6ba5126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0842d83a60027d875a0955c917c99c19935a96ef9827c37e655d72673286f2`

```dockerfile
```

-	Layers:
	-	`sha256:75aa001f9acf4b60bb11607334f3dfb7fc38dab3bc1b6fc5d19c4e11403b62a1`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:a38772a4376f984332843064dcd64529345698a31a522d9e743987c6e9fcf062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68383198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272d56ce0b6289e34fdc69a110e200627da4edddfd7d75df5a3d35e50091e40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a80bd51374d59cccbe39550e29f3c75a4898d5c2b280388e8af740da9b07164b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f168959aace97d67eaf1304c91ac8dfbee2d113d5d8603c5813758c285776`

```dockerfile
```

-	Layers:
	-	`sha256:2810d6f734119f2a44d1165a8f025decfb025d213521b3e85924d093fb8f1354`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a00c0bc47f8908b1a966cb40ffdd06470593dc098b4d6c7ac356c7f7134f9de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70172005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0075144f78e3fc8d804eb929c2cf866a2ae0295c47f80dd57a7074863ba2736b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c97d9cee1f1276f1b5c4f148387ce7f92a0f69d5d5805e39bf0a839fb8305949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7899ba69a193c95da9272216327b56babf9364894e32734aa60a0fc96bd2c0`

```dockerfile
```

-	Layers:
	-	`sha256:225c9a7352f7eb6df35d3bd7852ecf7eb0f840312b66c6ae6e88d4847326bf7e`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-dind`

```console
$ docker pull docker@sha256:4924fece44d61eeec47f619a4c35cd70fa2a31cd36b6283943a122369549fb82
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

### `docker:28.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:c4b520b9a63e5115f6d9843c62522b6560756164554b5c9a3a9c20bcb552e3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141638455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7ea23310b3fff4bbef36e8b08d5235dffa4d1aef78d84779d009e52daf7199`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:147e7c33d9e0781984a50137a65ab2801e4cbb5f519794b0b305a0f10539b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae01ef61862c7d28c4e48daaf3bcab61392d36b8995d1a304c28484403104db7`

```dockerfile
```

-	Layers:
	-	`sha256:01580a980dc523731ae2593398ec17f2aee10cc2224a12eec7f40edd279f0c15`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:acd9933ad265f50391c17d366e6b8b2774345d83655ac9eb52b18eb42a1140dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132245125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811d9a6156b3817de2198edbebe33a6c8cc87db51c522c2551723096b7fe9e55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0bf2e3301b433097f02a64cb68c64719a9d601c4c4e8199753a97d2eca08f5`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 7.0 MB (7036910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bea1f449ae4828750de8d364675e658773d2395554fb8f6e5b27abf6650d4a`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50285df7a34e25624ea34e42fcd0a315257b55c57443f5e1c9f7d87a64844be`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e48adef24818df5086795a0b59c0920fcbeab02b52b14b3d2948aa8dae560e`  
		Last Modified: Tue, 25 Mar 2025 21:57:04 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e6cc859de766f4621a9057c7a584c0bae06240f47f49125d0a53b0ccf2817`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b02adeb27e77008de20f43b04c15f9400674028dde877ca2c85db228d63833`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a062c1bae3694f2dc57a86f1a0a31f0646edbe073ba3b5332b7ea703fc95439a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6e9ff128ff3dd627ea97a881ed9d45513bfbbdd3ae431e585925664bcb1073`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b93d052b010bed3a7a457c00779ec2ccbd5200b802737da2302f23898bf0d`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5aec0cd9338b8c87a48d32538f1126aa1ea564bab5e0f88c2c3711887986e8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130582961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c8e6ea19a06349bd3fff8b36b6edc473d618f00fa98e0cf2b2245a333ec036`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e99727b81f4572b85e4f50bb748f74834c084c2be0336f0861ec92f578aab1d`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 6.4 MB (6366260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a406bc3246700b25d15b9a21a2c297aa03294574c920835f8e279fd40a99248c`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274227b3189ab05a7bcf8b5bca0a03e2da5a20fb0b29a005f653109f8307f13f`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d83b5ee45ba8b5cca7c66e593eed8890a19086546cc5b73e7aef977003052f7`  
		Last Modified: Tue, 25 Mar 2025 21:57:07 GMT  
		Size: 55.7 MB (55741247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82e270939ba77481d58f0731a8190051ed151ddeaf18ae9c71a711f5b23b19`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468d9090d7bb5417d46894a189d2c10a477709d8025de53c9684d708d936fbc`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ef399f39c3375b2b26eef2b816ef0bc918beeebc2df752d98f6c8ff3d8af56e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba96e9df1e9b4b3f8af60be57bcef0cf7e05ce7cbdc423ad8100ccc83513eff`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a457447e187312ae0fcbe8833d37bc3524eca92d733dd57cbb2e2ce0e584a`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:223d046021f324792db4fbd1396746b63ffb93f00861ea390d7fbbaf392585e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132967037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a69ac0c9fe38a13675c478cc22e49748128d1bab3e99eb0e2c6be27dfd7d3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:64a2e28c40f0a0dfc87d02ef347ac0bc427ba0ffcc4b786312c6c94774615d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa29ab3f950e5f22976c193db0590a2c8448a680d52dc5423896788a0af100b1`

```dockerfile
```

-	Layers:
	-	`sha256:8d5656be0e9638a2cdce9ab5a83f7e3464efca3bceb222bd596af0b060d128a9`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-dind-rootless`

```console
$ docker pull docker@sha256:a5090d7c11c05a862ae22fbb478c62a4e9643fa431eaf7a9a7812fef7a67a859
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c06be5bc3b0e24f7f4b5ffbbcd8ca9ab02519562d691cb456f5d6b98f29c39c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159797561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13bdb47aeff8daa8094c59742ad7afc5ad9e580eec39dd8f76368cc62b7ce87`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded84039e564b9475ac7b125bcf4fb9502f33f947c0ddd3536f43effc60d6a54`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 986.6 KB (986584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40aafab5cc59e8f5cb5e26668f818b42db849fe877e95d7a3529e90d4a3c8bd9`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6da82905025ead3a593c912e1918488b0874da3fe3299e2a42bdb1cc934be3`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654321f2b23758f8b02e88231bb7f7f6dee732758055aea66fd4dce0973416a`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 17.2 MB (17171184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3959b7e18a4fbdba386c18493c321ff4ca8830103acfcd3d187205a34cd112a9`  
		Last Modified: Tue, 25 Mar 2025 22:07:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bca820a790106f4866c59edf3d44fe79e09e9fa614e0a9f876c8919a5083f221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3323bffc2b5312b105253768c2c98037a504a39c4c7af0e7d7e1520aa6fb44`

```dockerfile
```

-	Layers:
	-	`sha256:e38eb0dfbf00e9814744fe5742ba05c41d5fa87629943046da2c159f210fa232`  
		Last Modified: Tue, 25 Mar 2025 22:07:39 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18a046138bef9eba3e6cf40129dd21388ec0a65d78a43003f1d93c8c8a4a075a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153264716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaf59ab004246a3948261b2eb47e4829eb00058acc9da25a1df6cff853a3f5b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cec22076d04d53956a39ca4217e9df0953e2089d2e7bc1927bef33d1228f4ce`  
		Last Modified: Tue, 25 Mar 2025 22:07:55 GMT  
		Size: 1.0 MB (1014208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a832bc3a23d3053414b32a049f9513b8654a574152e2b5d59d5616d4ab21e7`  
		Last Modified: Tue, 25 Mar 2025 22:07:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9308d557624dd27d66f0684ea0043bab12df8101320568cc69a8cdfead8367ed`  
		Last Modified: Tue, 25 Mar 2025 22:07:54 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48c2c7bc6b3fe5cf98c66408a3d4a051eaf3a7ef3c1aff1d2ebcb92c7d5e394`  
		Last Modified: Tue, 25 Mar 2025 22:07:55 GMT  
		Size: 19.3 MB (19282130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe93e7f39bff732dc1b6bad18045bb6d77a906b8672b73f15e5437aecdc1b9e`  
		Last Modified: Tue, 25 Mar 2025 22:07:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e4e4429f44acdd9a71ddee3e2e7db9d16cba204c73232fab6e85b41970d037dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7504d9409f225cb85c9078ba600e2b30c8e50444f521f6fa12ebd5a20c6703ae`

```dockerfile
```

-	Layers:
	-	`sha256:6d6cd4b0e7f4511463caf0aa1389476e27c5b8ef1a2ca5681666010a6d33f5de`  
		Last Modified: Tue, 25 Mar 2025 22:07:54 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-windowsservercore`

```console
$ docker pull docker@sha256:fdbf04adec3070897345d1e057af86328464a4e11f3f7426fc7b27e94e2eb517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:28.0-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:37fbf58c618a1e257ff62a5c17597a58c612390d9b8248b12de620ff0dc27116
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974098228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d876f863caff9ced5d2166306316ea67c3e8f29ecd77f820b472be5e597514de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 21:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:36:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:36:02 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:36:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:36:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:14 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:36:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:36:16 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:36:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:36:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230d8f91a46ec72be09fa76d5ed5c5c953b39e08a445f5dc09dacc9ee44eb74a`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497744dd92652df503964233d52071afe6b6da69fcc9d699ecdef8a81132716`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 393.8 KB (393794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bbe029cc51bac0aa9cdd3ec3325e113f38f3632cef853c3d488b1b1641adae`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e6465d36bb7dd3cbd69b2e9a38b3544b7eab714dd64a6c38788e616627500b`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9179050a0c68ba8475bf29ed21dd34e7d54d5f314a7ac42b2fca85710f90f32`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 19.9 MB (19904481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3871cbf913d4865bf43a87c7cbf2227b2705afa74b1281dba34fe25af1a73e5b`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae86510368ad79d177019fd99371ebda2255844ae98eed60c771294d11b158db`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1c6e4bc9abf47f577d2fea496c8dd7cd245ef59f6342b8274eb1e1bfe3deb3`  
		Last Modified: Tue, 25 Mar 2025 21:36:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944b89a3759e186bd3d1e0373910a72d0c398b453c235e4e3859f193aafb6f7d`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.8 MB (22807812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3fe3114e244b2f87a8272a1e53a7be89778c0f0609da78972fa83adf80028`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3bb7f5e52b615856b2468cacce7cfda132ef42d917ec6c7b1ed45144fd6574`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711261a97010fbb377d12b5a0adc589d06fbb8b0d5fe5b15131e5124210a14d5`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0375e49eb81a62ee6208594c9fd6c9c2faede214b7a1c4d4a263bd1908edb436`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.3 MB (22332711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:f99d03d930f93e2749004c210255ac7f6b52149af0a79f27716da370fa7b1eb6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335275907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c5fa0da0dfcdf03eeb0a5cc8d07e757bd37f4f77b4f8a064d43809c323c1c8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 25 Mar 2025 21:37:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:38:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:38:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:38:21 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:38:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:38:30 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:38:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e87728e165e6772cede047713a447fd6e30659d8dd65ce204231ed4a7dbb0e`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe917f396787792b92fc9c8f5959b2f8be7522c5b2d400aed59e46867d04a`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 371.5 KB (371494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c896757855fa4e3de01285214ef7138cbe36c12ca479b1124f575ee219dcac`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4036332907e21a93b9f46503d71b483e433e9268f61846e8fd3669ad8e8260`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f2151a5c434f05d2e41c3bf031037cf88d7a152683a0aa34b1e6d50e55f5d6`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 19.9 MB (19873533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd21b973a1b5c558975227864cfb89ba209e894f4a446b40afd17ec3b9ee9a80`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce9542ef040e9bf201f9a54875111a9eba23bb63caf4a022c127d73bb8fc7b8`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb91e206b539328afd55e6043c5c2825cfc67484bb8ff7055f76034431f02a83`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111bedc1382fe6bceb4dc527c273e3e88d670a978f867793f8cb11dace8ab00`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.8 MB (22775231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9293f4095824ab934e2ea69a23a4ea9e5b880f5e5d4a0f1bbf1cc5543e5a9`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f1c82a5ed7da58754739b095aac5f1ec0fe3aea0d48069290cfc0c9af4c4d`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608603ddb53750c36f5d27ef3c6d70b3d90ebe2430701772a11a1dc8ab625795`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63caecab4c5855f0c5198d61e2ec9cb95d046b983b51c66bdafcfe9383dad979`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.3 MB (22302869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:a07b73a00a3c52cf508c570e374efc24be0c453d86c9452fcea303ba531ffc8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216893552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a9a00b1e30a51e5c8dc78b5d38184a68cda33f84d782e8bf6ef53aa9e235d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 21:33:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:34:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:34:13 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:34:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:34:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:25 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:34:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:34:27 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:34:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:34:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:34:38 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:34:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a524a0e9cb7afa4d4cd71cd32e949c44f21cba76046ad004d2d6d09870f93ca`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847dbfeb702fcf37b419ad4ed9aa7e21d43d27bf895a29d8da424b6b58d57dc`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 340.0 KB (339963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edce44d57bdec9498491ec04581f5193d08ac7cfe87170c1368d3f2456d40268`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c046029f114363dc51b43457767bcb3f623e3c8f32e8ca7f9b2db9d7972f56`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ee9950b1bd1e3a417a9674a6ed4ba90d4b0101a2aad3d904faf071830bd11`  
		Last Modified: Tue, 25 Mar 2025 21:34:58 GMT  
		Size: 19.9 MB (19859748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5786612fd2d55be281d632baaa5e172f6bd8458061b5ecf3bffedb71d6de9`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0a2088c740ff617b174a979824713e0ad78fe077aa205af5340a6aa886e39`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71a201934e91595d89a5cda2c3f1824c4766cda3ae640a1e8f7dd00e3a33ad`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dd615d0c7c6f688705646fd983a540cca62d8d975b8fd767e83954950ba82d`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.8 MB (22763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e870735d52bdad39865ea0295c463823531285214d901abdf128dca151e17c5`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e5d174601f7707cecf5521b4bdf1b1198187a4844a00a623a89d78257bdb1`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7fcbbabcb3464ee277100b9f6fd1c395109f1ce5de50e92adc5431a6beb04`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176d290ac87077c88ca4ce30853fd4d9020a6eb3dbc3df72610e011d5869d562`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.3 MB (22283549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:c8052ef5f90cd2fa3c44394fec8378a887db5d87c66f6d5af683b3082f4f3658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:28.0-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:a07b73a00a3c52cf508c570e374efc24be0c453d86c9452fcea303ba531ffc8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216893552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a9a00b1e30a51e5c8dc78b5d38184a68cda33f84d782e8bf6ef53aa9e235d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 21:33:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:34:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:34:13 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:34:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:34:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:25 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:34:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:34:27 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:34:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:34:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:34:38 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:34:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a524a0e9cb7afa4d4cd71cd32e949c44f21cba76046ad004d2d6d09870f93ca`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847dbfeb702fcf37b419ad4ed9aa7e21d43d27bf895a29d8da424b6b58d57dc`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 340.0 KB (339963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edce44d57bdec9498491ec04581f5193d08ac7cfe87170c1368d3f2456d40268`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c046029f114363dc51b43457767bcb3f623e3c8f32e8ca7f9b2db9d7972f56`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ee9950b1bd1e3a417a9674a6ed4ba90d4b0101a2aad3d904faf071830bd11`  
		Last Modified: Tue, 25 Mar 2025 21:34:58 GMT  
		Size: 19.9 MB (19859748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5786612fd2d55be281d632baaa5e172f6bd8458061b5ecf3bffedb71d6de9`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0a2088c740ff617b174a979824713e0ad78fe077aa205af5340a6aa886e39`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71a201934e91595d89a5cda2c3f1824c4766cda3ae640a1e8f7dd00e3a33ad`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dd615d0c7c6f688705646fd983a540cca62d8d975b8fd767e83954950ba82d`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.8 MB (22763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e870735d52bdad39865ea0295c463823531285214d901abdf128dca151e17c5`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e5d174601f7707cecf5521b4bdf1b1198187a4844a00a623a89d78257bdb1`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7fcbbabcb3464ee277100b9f6fd1c395109f1ce5de50e92adc5431a6beb04`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176d290ac87077c88ca4ce30853fd4d9020a6eb3dbc3df72610e011d5869d562`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.3 MB (22283549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ae68b9f2e53406551f2704648cf0197fc3499d7003d00f8dbde54b97cd9f1a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:28.0-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:f99d03d930f93e2749004c210255ac7f6b52149af0a79f27716da370fa7b1eb6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335275907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c5fa0da0dfcdf03eeb0a5cc8d07e757bd37f4f77b4f8a064d43809c323c1c8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 25 Mar 2025 21:37:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:38:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:38:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:38:21 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:38:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:38:30 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:38:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e87728e165e6772cede047713a447fd6e30659d8dd65ce204231ed4a7dbb0e`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe917f396787792b92fc9c8f5959b2f8be7522c5b2d400aed59e46867d04a`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 371.5 KB (371494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c896757855fa4e3de01285214ef7138cbe36c12ca479b1124f575ee219dcac`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4036332907e21a93b9f46503d71b483e433e9268f61846e8fd3669ad8e8260`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f2151a5c434f05d2e41c3bf031037cf88d7a152683a0aa34b1e6d50e55f5d6`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 19.9 MB (19873533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd21b973a1b5c558975227864cfb89ba209e894f4a446b40afd17ec3b9ee9a80`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce9542ef040e9bf201f9a54875111a9eba23bb63caf4a022c127d73bb8fc7b8`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb91e206b539328afd55e6043c5c2825cfc67484bb8ff7055f76034431f02a83`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111bedc1382fe6bceb4dc527c273e3e88d670a978f867793f8cb11dace8ab00`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.8 MB (22775231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9293f4095824ab934e2ea69a23a4ea9e5b880f5e5d4a0f1bbf1cc5543e5a9`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f1c82a5ed7da58754739b095aac5f1ec0fe3aea0d48069290cfc0c9af4c4d`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608603ddb53750c36f5d27ef3c6d70b3d90ebe2430701772a11a1dc8ab625795`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63caecab4c5855f0c5198d61e2ec9cb95d046b983b51c66bdafcfe9383dad979`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.3 MB (22302869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b25d93a59fbdb43e27ccd5ff42b9a530d1c07616c048664e2a9858300a0817ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:28.0-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:37fbf58c618a1e257ff62a5c17597a58c612390d9b8248b12de620ff0dc27116
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974098228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d876f863caff9ced5d2166306316ea67c3e8f29ecd77f820b472be5e597514de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 21:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:36:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:36:02 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:36:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:36:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:14 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:36:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:36:16 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:36:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:36:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230d8f91a46ec72be09fa76d5ed5c5c953b39e08a445f5dc09dacc9ee44eb74a`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497744dd92652df503964233d52071afe6b6da69fcc9d699ecdef8a81132716`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 393.8 KB (393794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bbe029cc51bac0aa9cdd3ec3325e113f38f3632cef853c3d488b1b1641adae`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e6465d36bb7dd3cbd69b2e9a38b3544b7eab714dd64a6c38788e616627500b`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9179050a0c68ba8475bf29ed21dd34e7d54d5f314a7ac42b2fca85710f90f32`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 19.9 MB (19904481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3871cbf913d4865bf43a87c7cbf2227b2705afa74b1281dba34fe25af1a73e5b`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae86510368ad79d177019fd99371ebda2255844ae98eed60c771294d11b158db`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1c6e4bc9abf47f577d2fea496c8dd7cd245ef59f6342b8274eb1e1bfe3deb3`  
		Last Modified: Tue, 25 Mar 2025 21:36:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944b89a3759e186bd3d1e0373910a72d0c398b453c235e4e3859f193aafb6f7d`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.8 MB (22807812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3fe3114e244b2f87a8272a1e53a7be89778c0f0609da78972fa83adf80028`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3bb7f5e52b615856b2468cacce7cfda132ef42d917ec6c7b1ed45144fd6574`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711261a97010fbb377d12b5a0adc589d06fbb8b0d5fe5b15131e5124210a14d5`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0375e49eb81a62ee6208594c9fd6c9c2faede214b7a1c4d4a263bd1908edb436`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.3 MB (22332711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.4`

```console
$ docker pull docker@sha256:4924fece44d61eeec47f619a4c35cd70fa2a31cd36b6283943a122369549fb82
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

### `docker:28.0.4` - linux; amd64

```console
$ docker pull docker@sha256:c4b520b9a63e5115f6d9843c62522b6560756164554b5c9a3a9c20bcb552e3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141638455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7ea23310b3fff4bbef36e8b08d5235dffa4d1aef78d84779d009e52daf7199`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4` - unknown; unknown

```console
$ docker pull docker@sha256:147e7c33d9e0781984a50137a65ab2801e4cbb5f519794b0b305a0f10539b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae01ef61862c7d28c4e48daaf3bcab61392d36b8995d1a304c28484403104db7`

```dockerfile
```

-	Layers:
	-	`sha256:01580a980dc523731ae2593398ec17f2aee10cc2224a12eec7f40edd279f0c15`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4` - linux; arm variant v6

```console
$ docker pull docker@sha256:acd9933ad265f50391c17d366e6b8b2774345d83655ac9eb52b18eb42a1140dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132245125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811d9a6156b3817de2198edbebe33a6c8cc87db51c522c2551723096b7fe9e55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0bf2e3301b433097f02a64cb68c64719a9d601c4c4e8199753a97d2eca08f5`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 7.0 MB (7036910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bea1f449ae4828750de8d364675e658773d2395554fb8f6e5b27abf6650d4a`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50285df7a34e25624ea34e42fcd0a315257b55c57443f5e1c9f7d87a64844be`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e48adef24818df5086795a0b59c0920fcbeab02b52b14b3d2948aa8dae560e`  
		Last Modified: Tue, 25 Mar 2025 21:57:04 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e6cc859de766f4621a9057c7a584c0bae06240f47f49125d0a53b0ccf2817`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b02adeb27e77008de20f43b04c15f9400674028dde877ca2c85db228d63833`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4` - unknown; unknown

```console
$ docker pull docker@sha256:a062c1bae3694f2dc57a86f1a0a31f0646edbe073ba3b5332b7ea703fc95439a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6e9ff128ff3dd627ea97a881ed9d45513bfbbdd3ae431e585925664bcb1073`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b93d052b010bed3a7a457c00779ec2ccbd5200b802737da2302f23898bf0d`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4` - linux; arm variant v7

```console
$ docker pull docker@sha256:5aec0cd9338b8c87a48d32538f1126aa1ea564bab5e0f88c2c3711887986e8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130582961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c8e6ea19a06349bd3fff8b36b6edc473d618f00fa98e0cf2b2245a333ec036`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e99727b81f4572b85e4f50bb748f74834c084c2be0336f0861ec92f578aab1d`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 6.4 MB (6366260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a406bc3246700b25d15b9a21a2c297aa03294574c920835f8e279fd40a99248c`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274227b3189ab05a7bcf8b5bca0a03e2da5a20fb0b29a005f653109f8307f13f`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d83b5ee45ba8b5cca7c66e593eed8890a19086546cc5b73e7aef977003052f7`  
		Last Modified: Tue, 25 Mar 2025 21:57:07 GMT  
		Size: 55.7 MB (55741247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82e270939ba77481d58f0731a8190051ed151ddeaf18ae9c71a711f5b23b19`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468d9090d7bb5417d46894a189d2c10a477709d8025de53c9684d708d936fbc`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4` - unknown; unknown

```console
$ docker pull docker@sha256:ef399f39c3375b2b26eef2b816ef0bc918beeebc2df752d98f6c8ff3d8af56e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba96e9df1e9b4b3f8af60be57bcef0cf7e05ce7cbdc423ad8100ccc83513eff`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a457447e187312ae0fcbe8833d37bc3524eca92d733dd57cbb2e2ce0e584a`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:223d046021f324792db4fbd1396746b63ffb93f00861ea390d7fbbaf392585e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132967037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a69ac0c9fe38a13675c478cc22e49748128d1bab3e99eb0e2c6be27dfd7d3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4` - unknown; unknown

```console
$ docker pull docker@sha256:64a2e28c40f0a0dfc87d02ef347ac0bc427ba0ffcc4b786312c6c94774615d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa29ab3f950e5f22976c193db0590a2c8448a680d52dc5423896788a0af100b1`

```dockerfile
```

-	Layers:
	-	`sha256:8d5656be0e9638a2cdce9ab5a83f7e3464efca3bceb222bd596af0b060d128a9`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-alpine3.21`

```console
$ docker pull docker@sha256:4924fece44d61eeec47f619a4c35cd70fa2a31cd36b6283943a122369549fb82
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

### `docker:28.0.4-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:c4b520b9a63e5115f6d9843c62522b6560756164554b5c9a3a9c20bcb552e3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141638455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7ea23310b3fff4bbef36e8b08d5235dffa4d1aef78d84779d009e52daf7199`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:147e7c33d9e0781984a50137a65ab2801e4cbb5f519794b0b305a0f10539b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae01ef61862c7d28c4e48daaf3bcab61392d36b8995d1a304c28484403104db7`

```dockerfile
```

-	Layers:
	-	`sha256:01580a980dc523731ae2593398ec17f2aee10cc2224a12eec7f40edd279f0c15`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:acd9933ad265f50391c17d366e6b8b2774345d83655ac9eb52b18eb42a1140dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132245125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811d9a6156b3817de2198edbebe33a6c8cc87db51c522c2551723096b7fe9e55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0bf2e3301b433097f02a64cb68c64719a9d601c4c4e8199753a97d2eca08f5`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 7.0 MB (7036910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bea1f449ae4828750de8d364675e658773d2395554fb8f6e5b27abf6650d4a`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50285df7a34e25624ea34e42fcd0a315257b55c57443f5e1c9f7d87a64844be`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e48adef24818df5086795a0b59c0920fcbeab02b52b14b3d2948aa8dae560e`  
		Last Modified: Tue, 25 Mar 2025 21:57:04 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e6cc859de766f4621a9057c7a584c0bae06240f47f49125d0a53b0ccf2817`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b02adeb27e77008de20f43b04c15f9400674028dde877ca2c85db228d63833`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:a062c1bae3694f2dc57a86f1a0a31f0646edbe073ba3b5332b7ea703fc95439a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6e9ff128ff3dd627ea97a881ed9d45513bfbbdd3ae431e585925664bcb1073`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b93d052b010bed3a7a457c00779ec2ccbd5200b802737da2302f23898bf0d`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:5aec0cd9338b8c87a48d32538f1126aa1ea564bab5e0f88c2c3711887986e8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130582961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c8e6ea19a06349bd3fff8b36b6edc473d618f00fa98e0cf2b2245a333ec036`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e99727b81f4572b85e4f50bb748f74834c084c2be0336f0861ec92f578aab1d`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 6.4 MB (6366260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a406bc3246700b25d15b9a21a2c297aa03294574c920835f8e279fd40a99248c`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274227b3189ab05a7bcf8b5bca0a03e2da5a20fb0b29a005f653109f8307f13f`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d83b5ee45ba8b5cca7c66e593eed8890a19086546cc5b73e7aef977003052f7`  
		Last Modified: Tue, 25 Mar 2025 21:57:07 GMT  
		Size: 55.7 MB (55741247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82e270939ba77481d58f0731a8190051ed151ddeaf18ae9c71a711f5b23b19`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468d9090d7bb5417d46894a189d2c10a477709d8025de53c9684d708d936fbc`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:ef399f39c3375b2b26eef2b816ef0bc918beeebc2df752d98f6c8ff3d8af56e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba96e9df1e9b4b3f8af60be57bcef0cf7e05ce7cbdc423ad8100ccc83513eff`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a457447e187312ae0fcbe8833d37bc3524eca92d733dd57cbb2e2ce0e584a`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:223d046021f324792db4fbd1396746b63ffb93f00861ea390d7fbbaf392585e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132967037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a69ac0c9fe38a13675c478cc22e49748128d1bab3e99eb0e2c6be27dfd7d3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:64a2e28c40f0a0dfc87d02ef347ac0bc427ba0ffcc4b786312c6c94774615d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa29ab3f950e5f22976c193db0590a2c8448a680d52dc5423896788a0af100b1`

```dockerfile
```

-	Layers:
	-	`sha256:8d5656be0e9638a2cdce9ab5a83f7e3464efca3bceb222bd596af0b060d128a9`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-cli`

```console
$ docker pull docker@sha256:c5e0b27a15f49b571f968defe19cc9a072d531ee90300ba5a1d2ea4dffa760e4
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

### `docker:28.0.4-cli` - linux; amd64

```console
$ docker pull docker@sha256:23b5b1a900c5676eaee32c38dbdf727a37a6ace0c5980885a9ec21da619608f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74456477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6539186f04a7291f29d299010b9ab4b55d15e95c6b0e5a7ed5343225ebaeca47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1133514976c34d263934880176c7466336c52b261e542275beeba2b0e5917292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966754ba178f5be30b512dcf67885f9543d39a53d5299d73a475f5f65ab3c216`

```dockerfile
```

-	Layers:
	-	`sha256:45b02f14e5b651223c3c46b95436ebab9917894f4d446223811103debafdf45f`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1c3cb277d90221fcd05b69ef6a0f498fe66939317b75f5018c1cc3ca76387ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69371203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a418a759b70319d7bb3094bb667c222c2e70891d056076f8f9348a047f66c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b03cfc87f30735938381fcba67b7d48fb8e172a0426952a5c613717a6ba5126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0842d83a60027d875a0955c917c99c19935a96ef9827c37e655d72673286f2`

```dockerfile
```

-	Layers:
	-	`sha256:75aa001f9acf4b60bb11607334f3dfb7fc38dab3bc1b6fc5d19c4e11403b62a1`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:a38772a4376f984332843064dcd64529345698a31a522d9e743987c6e9fcf062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68383198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272d56ce0b6289e34fdc69a110e200627da4edddfd7d75df5a3d35e50091e40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a80bd51374d59cccbe39550e29f3c75a4898d5c2b280388e8af740da9b07164b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f168959aace97d67eaf1304c91ac8dfbee2d113d5d8603c5813758c285776`

```dockerfile
```

-	Layers:
	-	`sha256:2810d6f734119f2a44d1165a8f025decfb025d213521b3e85924d093fb8f1354`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a00c0bc47f8908b1a966cb40ffdd06470593dc098b4d6c7ac356c7f7134f9de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70172005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0075144f78e3fc8d804eb929c2cf866a2ae0295c47f80dd57a7074863ba2736b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c97d9cee1f1276f1b5c4f148387ce7f92a0f69d5d5805e39bf0a839fb8305949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7899ba69a193c95da9272216327b56babf9364894e32734aa60a0fc96bd2c0`

```dockerfile
```

-	Layers:
	-	`sha256:225c9a7352f7eb6df35d3bd7852ecf7eb0f840312b66c6ae6e88d4847326bf7e`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-cli-alpine3.21`

```console
$ docker pull docker@sha256:c5e0b27a15f49b571f968defe19cc9a072d531ee90300ba5a1d2ea4dffa760e4
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

### `docker:28.0.4-cli-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:23b5b1a900c5676eaee32c38dbdf727a37a6ace0c5980885a9ec21da619608f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74456477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6539186f04a7291f29d299010b9ab4b55d15e95c6b0e5a7ed5343225ebaeca47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:1133514976c34d263934880176c7466336c52b261e542275beeba2b0e5917292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966754ba178f5be30b512dcf67885f9543d39a53d5299d73a475f5f65ab3c216`

```dockerfile
```

-	Layers:
	-	`sha256:45b02f14e5b651223c3c46b95436ebab9917894f4d446223811103debafdf45f`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1c3cb277d90221fcd05b69ef6a0f498fe66939317b75f5018c1cc3ca76387ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69371203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a418a759b70319d7bb3094bb667c222c2e70891d056076f8f9348a047f66c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:4b03cfc87f30735938381fcba67b7d48fb8e172a0426952a5c613717a6ba5126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0842d83a60027d875a0955c917c99c19935a96ef9827c37e655d72673286f2`

```dockerfile
```

-	Layers:
	-	`sha256:75aa001f9acf4b60bb11607334f3dfb7fc38dab3bc1b6fc5d19c4e11403b62a1`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-cli-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:a38772a4376f984332843064dcd64529345698a31a522d9e743987c6e9fcf062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68383198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272d56ce0b6289e34fdc69a110e200627da4edddfd7d75df5a3d35e50091e40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:a80bd51374d59cccbe39550e29f3c75a4898d5c2b280388e8af740da9b07164b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f168959aace97d67eaf1304c91ac8dfbee2d113d5d8603c5813758c285776`

```dockerfile
```

-	Layers:
	-	`sha256:2810d6f734119f2a44d1165a8f025decfb025d213521b3e85924d093fb8f1354`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a00c0bc47f8908b1a966cb40ffdd06470593dc098b4d6c7ac356c7f7134f9de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70172005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0075144f78e3fc8d804eb929c2cf866a2ae0295c47f80dd57a7074863ba2736b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:c97d9cee1f1276f1b5c4f148387ce7f92a0f69d5d5805e39bf0a839fb8305949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7899ba69a193c95da9272216327b56babf9364894e32734aa60a0fc96bd2c0`

```dockerfile
```

-	Layers:
	-	`sha256:225c9a7352f7eb6df35d3bd7852ecf7eb0f840312b66c6ae6e88d4847326bf7e`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-dind`

```console
$ docker pull docker@sha256:4924fece44d61eeec47f619a4c35cd70fa2a31cd36b6283943a122369549fb82
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

### `docker:28.0.4-dind` - linux; amd64

```console
$ docker pull docker@sha256:c4b520b9a63e5115f6d9843c62522b6560756164554b5c9a3a9c20bcb552e3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141638455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7ea23310b3fff4bbef36e8b08d5235dffa4d1aef78d84779d009e52daf7199`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:147e7c33d9e0781984a50137a65ab2801e4cbb5f519794b0b305a0f10539b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae01ef61862c7d28c4e48daaf3bcab61392d36b8995d1a304c28484403104db7`

```dockerfile
```

-	Layers:
	-	`sha256:01580a980dc523731ae2593398ec17f2aee10cc2224a12eec7f40edd279f0c15`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:acd9933ad265f50391c17d366e6b8b2774345d83655ac9eb52b18eb42a1140dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132245125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811d9a6156b3817de2198edbebe33a6c8cc87db51c522c2551723096b7fe9e55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0bf2e3301b433097f02a64cb68c64719a9d601c4c4e8199753a97d2eca08f5`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 7.0 MB (7036910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bea1f449ae4828750de8d364675e658773d2395554fb8f6e5b27abf6650d4a`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50285df7a34e25624ea34e42fcd0a315257b55c57443f5e1c9f7d87a64844be`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e48adef24818df5086795a0b59c0920fcbeab02b52b14b3d2948aa8dae560e`  
		Last Modified: Tue, 25 Mar 2025 21:57:04 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e6cc859de766f4621a9057c7a584c0bae06240f47f49125d0a53b0ccf2817`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b02adeb27e77008de20f43b04c15f9400674028dde877ca2c85db228d63833`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a062c1bae3694f2dc57a86f1a0a31f0646edbe073ba3b5332b7ea703fc95439a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6e9ff128ff3dd627ea97a881ed9d45513bfbbdd3ae431e585925664bcb1073`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b93d052b010bed3a7a457c00779ec2ccbd5200b802737da2302f23898bf0d`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5aec0cd9338b8c87a48d32538f1126aa1ea564bab5e0f88c2c3711887986e8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130582961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c8e6ea19a06349bd3fff8b36b6edc473d618f00fa98e0cf2b2245a333ec036`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e99727b81f4572b85e4f50bb748f74834c084c2be0336f0861ec92f578aab1d`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 6.4 MB (6366260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a406bc3246700b25d15b9a21a2c297aa03294574c920835f8e279fd40a99248c`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274227b3189ab05a7bcf8b5bca0a03e2da5a20fb0b29a005f653109f8307f13f`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d83b5ee45ba8b5cca7c66e593eed8890a19086546cc5b73e7aef977003052f7`  
		Last Modified: Tue, 25 Mar 2025 21:57:07 GMT  
		Size: 55.7 MB (55741247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82e270939ba77481d58f0731a8190051ed151ddeaf18ae9c71a711f5b23b19`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468d9090d7bb5417d46894a189d2c10a477709d8025de53c9684d708d936fbc`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ef399f39c3375b2b26eef2b816ef0bc918beeebc2df752d98f6c8ff3d8af56e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba96e9df1e9b4b3f8af60be57bcef0cf7e05ce7cbdc423ad8100ccc83513eff`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a457447e187312ae0fcbe8833d37bc3524eca92d733dd57cbb2e2ce0e584a`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:223d046021f324792db4fbd1396746b63ffb93f00861ea390d7fbbaf392585e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132967037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a69ac0c9fe38a13675c478cc22e49748128d1bab3e99eb0e2c6be27dfd7d3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:64a2e28c40f0a0dfc87d02ef347ac0bc427ba0ffcc4b786312c6c94774615d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa29ab3f950e5f22976c193db0590a2c8448a680d52dc5423896788a0af100b1`

```dockerfile
```

-	Layers:
	-	`sha256:8d5656be0e9638a2cdce9ab5a83f7e3464efca3bceb222bd596af0b060d128a9`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-dind-alpine3.21`

```console
$ docker pull docker@sha256:4924fece44d61eeec47f619a4c35cd70fa2a31cd36b6283943a122369549fb82
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

### `docker:28.0.4-dind-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:c4b520b9a63e5115f6d9843c62522b6560756164554b5c9a3a9c20bcb552e3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141638455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7ea23310b3fff4bbef36e8b08d5235dffa4d1aef78d84779d009e52daf7199`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:147e7c33d9e0781984a50137a65ab2801e4cbb5f519794b0b305a0f10539b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae01ef61862c7d28c4e48daaf3bcab61392d36b8995d1a304c28484403104db7`

```dockerfile
```

-	Layers:
	-	`sha256:01580a980dc523731ae2593398ec17f2aee10cc2224a12eec7f40edd279f0c15`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:acd9933ad265f50391c17d366e6b8b2774345d83655ac9eb52b18eb42a1140dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132245125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811d9a6156b3817de2198edbebe33a6c8cc87db51c522c2551723096b7fe9e55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0bf2e3301b433097f02a64cb68c64719a9d601c4c4e8199753a97d2eca08f5`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 7.0 MB (7036910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bea1f449ae4828750de8d364675e658773d2395554fb8f6e5b27abf6650d4a`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50285df7a34e25624ea34e42fcd0a315257b55c57443f5e1c9f7d87a64844be`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e48adef24818df5086795a0b59c0920fcbeab02b52b14b3d2948aa8dae560e`  
		Last Modified: Tue, 25 Mar 2025 21:57:04 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e6cc859de766f4621a9057c7a584c0bae06240f47f49125d0a53b0ccf2817`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b02adeb27e77008de20f43b04c15f9400674028dde877ca2c85db228d63833`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:a062c1bae3694f2dc57a86f1a0a31f0646edbe073ba3b5332b7ea703fc95439a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6e9ff128ff3dd627ea97a881ed9d45513bfbbdd3ae431e585925664bcb1073`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b93d052b010bed3a7a457c00779ec2ccbd5200b802737da2302f23898bf0d`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:5aec0cd9338b8c87a48d32538f1126aa1ea564bab5e0f88c2c3711887986e8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130582961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c8e6ea19a06349bd3fff8b36b6edc473d618f00fa98e0cf2b2245a333ec036`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e99727b81f4572b85e4f50bb748f74834c084c2be0336f0861ec92f578aab1d`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 6.4 MB (6366260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a406bc3246700b25d15b9a21a2c297aa03294574c920835f8e279fd40a99248c`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274227b3189ab05a7bcf8b5bca0a03e2da5a20fb0b29a005f653109f8307f13f`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d83b5ee45ba8b5cca7c66e593eed8890a19086546cc5b73e7aef977003052f7`  
		Last Modified: Tue, 25 Mar 2025 21:57:07 GMT  
		Size: 55.7 MB (55741247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82e270939ba77481d58f0731a8190051ed151ddeaf18ae9c71a711f5b23b19`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468d9090d7bb5417d46894a189d2c10a477709d8025de53c9684d708d936fbc`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:ef399f39c3375b2b26eef2b816ef0bc918beeebc2df752d98f6c8ff3d8af56e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba96e9df1e9b4b3f8af60be57bcef0cf7e05ce7cbdc423ad8100ccc83513eff`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a457447e187312ae0fcbe8833d37bc3524eca92d733dd57cbb2e2ce0e584a`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:223d046021f324792db4fbd1396746b63ffb93f00861ea390d7fbbaf392585e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132967037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a69ac0c9fe38a13675c478cc22e49748128d1bab3e99eb0e2c6be27dfd7d3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:64a2e28c40f0a0dfc87d02ef347ac0bc427ba0ffcc4b786312c6c94774615d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa29ab3f950e5f22976c193db0590a2c8448a680d52dc5423896788a0af100b1`

```dockerfile
```

-	Layers:
	-	`sha256:8d5656be0e9638a2cdce9ab5a83f7e3464efca3bceb222bd596af0b060d128a9`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-dind-rootless`

```console
$ docker pull docker@sha256:a5090d7c11c05a862ae22fbb478c62a4e9643fa431eaf7a9a7812fef7a67a859
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.0.4-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c06be5bc3b0e24f7f4b5ffbbcd8ca9ab02519562d691cb456f5d6b98f29c39c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159797561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13bdb47aeff8daa8094c59742ad7afc5ad9e580eec39dd8f76368cc62b7ce87`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded84039e564b9475ac7b125bcf4fb9502f33f947c0ddd3536f43effc60d6a54`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 986.6 KB (986584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40aafab5cc59e8f5cb5e26668f818b42db849fe877e95d7a3529e90d4a3c8bd9`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6da82905025ead3a593c912e1918488b0874da3fe3299e2a42bdb1cc934be3`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654321f2b23758f8b02e88231bb7f7f6dee732758055aea66fd4dce0973416a`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 17.2 MB (17171184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3959b7e18a4fbdba386c18493c321ff4ca8830103acfcd3d187205a34cd112a9`  
		Last Modified: Tue, 25 Mar 2025 22:07:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bca820a790106f4866c59edf3d44fe79e09e9fa614e0a9f876c8919a5083f221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3323bffc2b5312b105253768c2c98037a504a39c4c7af0e7d7e1520aa6fb44`

```dockerfile
```

-	Layers:
	-	`sha256:e38eb0dfbf00e9814744fe5742ba05c41d5fa87629943046da2c159f210fa232`  
		Last Modified: Tue, 25 Mar 2025 22:07:39 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18a046138bef9eba3e6cf40129dd21388ec0a65d78a43003f1d93c8c8a4a075a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153264716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaf59ab004246a3948261b2eb47e4829eb00058acc9da25a1df6cff853a3f5b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cec22076d04d53956a39ca4217e9df0953e2089d2e7bc1927bef33d1228f4ce`  
		Last Modified: Tue, 25 Mar 2025 22:07:55 GMT  
		Size: 1.0 MB (1014208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a832bc3a23d3053414b32a049f9513b8654a574152e2b5d59d5616d4ab21e7`  
		Last Modified: Tue, 25 Mar 2025 22:07:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9308d557624dd27d66f0684ea0043bab12df8101320568cc69a8cdfead8367ed`  
		Last Modified: Tue, 25 Mar 2025 22:07:54 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48c2c7bc6b3fe5cf98c66408a3d4a051eaf3a7ef3c1aff1d2ebcb92c7d5e394`  
		Last Modified: Tue, 25 Mar 2025 22:07:55 GMT  
		Size: 19.3 MB (19282130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe93e7f39bff732dc1b6bad18045bb6d77a906b8672b73f15e5437aecdc1b9e`  
		Last Modified: Tue, 25 Mar 2025 22:07:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e4e4429f44acdd9a71ddee3e2e7db9d16cba204c73232fab6e85b41970d037dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7504d9409f225cb85c9078ba600e2b30c8e50444f521f6fa12ebd5a20c6703ae`

```dockerfile
```

-	Layers:
	-	`sha256:6d6cd4b0e7f4511463caf0aa1389476e27c5b8ef1a2ca5681666010a6d33f5de`  
		Last Modified: Tue, 25 Mar 2025 22:07:54 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-windowsservercore`

```console
$ docker pull docker@sha256:fdbf04adec3070897345d1e057af86328464a4e11f3f7426fc7b27e94e2eb517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:28.0.4-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:37fbf58c618a1e257ff62a5c17597a58c612390d9b8248b12de620ff0dc27116
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974098228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d876f863caff9ced5d2166306316ea67c3e8f29ecd77f820b472be5e597514de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 21:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:36:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:36:02 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:36:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:36:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:14 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:36:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:36:16 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:36:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:36:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230d8f91a46ec72be09fa76d5ed5c5c953b39e08a445f5dc09dacc9ee44eb74a`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497744dd92652df503964233d52071afe6b6da69fcc9d699ecdef8a81132716`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 393.8 KB (393794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bbe029cc51bac0aa9cdd3ec3325e113f38f3632cef853c3d488b1b1641adae`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e6465d36bb7dd3cbd69b2e9a38b3544b7eab714dd64a6c38788e616627500b`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9179050a0c68ba8475bf29ed21dd34e7d54d5f314a7ac42b2fca85710f90f32`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 19.9 MB (19904481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3871cbf913d4865bf43a87c7cbf2227b2705afa74b1281dba34fe25af1a73e5b`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae86510368ad79d177019fd99371ebda2255844ae98eed60c771294d11b158db`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1c6e4bc9abf47f577d2fea496c8dd7cd245ef59f6342b8274eb1e1bfe3deb3`  
		Last Modified: Tue, 25 Mar 2025 21:36:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944b89a3759e186bd3d1e0373910a72d0c398b453c235e4e3859f193aafb6f7d`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.8 MB (22807812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3fe3114e244b2f87a8272a1e53a7be89778c0f0609da78972fa83adf80028`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3bb7f5e52b615856b2468cacce7cfda132ef42d917ec6c7b1ed45144fd6574`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711261a97010fbb377d12b5a0adc589d06fbb8b0d5fe5b15131e5124210a14d5`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0375e49eb81a62ee6208594c9fd6c9c2faede214b7a1c4d4a263bd1908edb436`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.3 MB (22332711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0.4-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:f99d03d930f93e2749004c210255ac7f6b52149af0a79f27716da370fa7b1eb6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335275907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c5fa0da0dfcdf03eeb0a5cc8d07e757bd37f4f77b4f8a064d43809c323c1c8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 25 Mar 2025 21:37:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:38:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:38:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:38:21 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:38:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:38:30 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:38:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e87728e165e6772cede047713a447fd6e30659d8dd65ce204231ed4a7dbb0e`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe917f396787792b92fc9c8f5959b2f8be7522c5b2d400aed59e46867d04a`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 371.5 KB (371494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c896757855fa4e3de01285214ef7138cbe36c12ca479b1124f575ee219dcac`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4036332907e21a93b9f46503d71b483e433e9268f61846e8fd3669ad8e8260`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f2151a5c434f05d2e41c3bf031037cf88d7a152683a0aa34b1e6d50e55f5d6`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 19.9 MB (19873533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd21b973a1b5c558975227864cfb89ba209e894f4a446b40afd17ec3b9ee9a80`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce9542ef040e9bf201f9a54875111a9eba23bb63caf4a022c127d73bb8fc7b8`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb91e206b539328afd55e6043c5c2825cfc67484bb8ff7055f76034431f02a83`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111bedc1382fe6bceb4dc527c273e3e88d670a978f867793f8cb11dace8ab00`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.8 MB (22775231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9293f4095824ab934e2ea69a23a4ea9e5b880f5e5d4a0f1bbf1cc5543e5a9`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f1c82a5ed7da58754739b095aac5f1ec0fe3aea0d48069290cfc0c9af4c4d`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608603ddb53750c36f5d27ef3c6d70b3d90ebe2430701772a11a1dc8ab625795`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63caecab4c5855f0c5198d61e2ec9cb95d046b983b51c66bdafcfe9383dad979`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.3 MB (22302869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0.4-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:a07b73a00a3c52cf508c570e374efc24be0c453d86c9452fcea303ba531ffc8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216893552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a9a00b1e30a51e5c8dc78b5d38184a68cda33f84d782e8bf6ef53aa9e235d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 21:33:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:34:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:34:13 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:34:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:34:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:25 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:34:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:34:27 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:34:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:34:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:34:38 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:34:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a524a0e9cb7afa4d4cd71cd32e949c44f21cba76046ad004d2d6d09870f93ca`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847dbfeb702fcf37b419ad4ed9aa7e21d43d27bf895a29d8da424b6b58d57dc`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 340.0 KB (339963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edce44d57bdec9498491ec04581f5193d08ac7cfe87170c1368d3f2456d40268`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c046029f114363dc51b43457767bcb3f623e3c8f32e8ca7f9b2db9d7972f56`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ee9950b1bd1e3a417a9674a6ed4ba90d4b0101a2aad3d904faf071830bd11`  
		Last Modified: Tue, 25 Mar 2025 21:34:58 GMT  
		Size: 19.9 MB (19859748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5786612fd2d55be281d632baaa5e172f6bd8458061b5ecf3bffedb71d6de9`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0a2088c740ff617b174a979824713e0ad78fe077aa205af5340a6aa886e39`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71a201934e91595d89a5cda2c3f1824c4766cda3ae640a1e8f7dd00e3a33ad`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dd615d0c7c6f688705646fd983a540cca62d8d975b8fd767e83954950ba82d`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.8 MB (22763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e870735d52bdad39865ea0295c463823531285214d901abdf128dca151e17c5`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e5d174601f7707cecf5521b4bdf1b1198187a4844a00a623a89d78257bdb1`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7fcbbabcb3464ee277100b9f6fd1c395109f1ce5de50e92adc5431a6beb04`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176d290ac87077c88ca4ce30853fd4d9020a6eb3dbc3df72610e011d5869d562`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.3 MB (22283549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.4-windowsservercore-1809`

```console
$ docker pull docker@sha256:c8052ef5f90cd2fa3c44394fec8378a887db5d87c66f6d5af683b3082f4f3658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:28.0.4-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:a07b73a00a3c52cf508c570e374efc24be0c453d86c9452fcea303ba531ffc8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216893552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a9a00b1e30a51e5c8dc78b5d38184a68cda33f84d782e8bf6ef53aa9e235d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 21:33:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:34:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:34:13 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:34:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:34:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:25 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:34:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:34:27 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:34:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:34:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:34:38 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:34:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a524a0e9cb7afa4d4cd71cd32e949c44f21cba76046ad004d2d6d09870f93ca`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847dbfeb702fcf37b419ad4ed9aa7e21d43d27bf895a29d8da424b6b58d57dc`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 340.0 KB (339963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edce44d57bdec9498491ec04581f5193d08ac7cfe87170c1368d3f2456d40268`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c046029f114363dc51b43457767bcb3f623e3c8f32e8ca7f9b2db9d7972f56`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ee9950b1bd1e3a417a9674a6ed4ba90d4b0101a2aad3d904faf071830bd11`  
		Last Modified: Tue, 25 Mar 2025 21:34:58 GMT  
		Size: 19.9 MB (19859748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5786612fd2d55be281d632baaa5e172f6bd8458061b5ecf3bffedb71d6de9`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0a2088c740ff617b174a979824713e0ad78fe077aa205af5340a6aa886e39`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71a201934e91595d89a5cda2c3f1824c4766cda3ae640a1e8f7dd00e3a33ad`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dd615d0c7c6f688705646fd983a540cca62d8d975b8fd767e83954950ba82d`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.8 MB (22763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e870735d52bdad39865ea0295c463823531285214d901abdf128dca151e17c5`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e5d174601f7707cecf5521b4bdf1b1198187a4844a00a623a89d78257bdb1`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7fcbbabcb3464ee277100b9f6fd1c395109f1ce5de50e92adc5431a6beb04`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176d290ac87077c88ca4ce30853fd4d9020a6eb3dbc3df72610e011d5869d562`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.3 MB (22283549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.4-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ae68b9f2e53406551f2704648cf0197fc3499d7003d00f8dbde54b97cd9f1a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:28.0.4-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:f99d03d930f93e2749004c210255ac7f6b52149af0a79f27716da370fa7b1eb6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335275907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c5fa0da0dfcdf03eeb0a5cc8d07e757bd37f4f77b4f8a064d43809c323c1c8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 25 Mar 2025 21:37:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:38:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:38:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:38:21 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:38:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:38:30 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:38:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e87728e165e6772cede047713a447fd6e30659d8dd65ce204231ed4a7dbb0e`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe917f396787792b92fc9c8f5959b2f8be7522c5b2d400aed59e46867d04a`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 371.5 KB (371494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c896757855fa4e3de01285214ef7138cbe36c12ca479b1124f575ee219dcac`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4036332907e21a93b9f46503d71b483e433e9268f61846e8fd3669ad8e8260`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f2151a5c434f05d2e41c3bf031037cf88d7a152683a0aa34b1e6d50e55f5d6`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 19.9 MB (19873533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd21b973a1b5c558975227864cfb89ba209e894f4a446b40afd17ec3b9ee9a80`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce9542ef040e9bf201f9a54875111a9eba23bb63caf4a022c127d73bb8fc7b8`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb91e206b539328afd55e6043c5c2825cfc67484bb8ff7055f76034431f02a83`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111bedc1382fe6bceb4dc527c273e3e88d670a978f867793f8cb11dace8ab00`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.8 MB (22775231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9293f4095824ab934e2ea69a23a4ea9e5b880f5e5d4a0f1bbf1cc5543e5a9`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f1c82a5ed7da58754739b095aac5f1ec0fe3aea0d48069290cfc0c9af4c4d`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608603ddb53750c36f5d27ef3c6d70b3d90ebe2430701772a11a1dc8ab625795`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63caecab4c5855f0c5198d61e2ec9cb95d046b983b51c66bdafcfe9383dad979`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.3 MB (22302869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.4-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b25d93a59fbdb43e27ccd5ff42b9a530d1c07616c048664e2a9858300a0817ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:28.0.4-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:37fbf58c618a1e257ff62a5c17597a58c612390d9b8248b12de620ff0dc27116
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974098228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d876f863caff9ced5d2166306316ea67c3e8f29ecd77f820b472be5e597514de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 21:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:36:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:36:02 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:36:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:36:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:14 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:36:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:36:16 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:36:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:36:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230d8f91a46ec72be09fa76d5ed5c5c953b39e08a445f5dc09dacc9ee44eb74a`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497744dd92652df503964233d52071afe6b6da69fcc9d699ecdef8a81132716`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 393.8 KB (393794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bbe029cc51bac0aa9cdd3ec3325e113f38f3632cef853c3d488b1b1641adae`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e6465d36bb7dd3cbd69b2e9a38b3544b7eab714dd64a6c38788e616627500b`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9179050a0c68ba8475bf29ed21dd34e7d54d5f314a7ac42b2fca85710f90f32`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 19.9 MB (19904481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3871cbf913d4865bf43a87c7cbf2227b2705afa74b1281dba34fe25af1a73e5b`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae86510368ad79d177019fd99371ebda2255844ae98eed60c771294d11b158db`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1c6e4bc9abf47f577d2fea496c8dd7cd245ef59f6342b8274eb1e1bfe3deb3`  
		Last Modified: Tue, 25 Mar 2025 21:36:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944b89a3759e186bd3d1e0373910a72d0c398b453c235e4e3859f193aafb6f7d`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.8 MB (22807812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3fe3114e244b2f87a8272a1e53a7be89778c0f0609da78972fa83adf80028`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3bb7f5e52b615856b2468cacce7cfda132ef42d917ec6c7b1ed45144fd6574`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711261a97010fbb377d12b5a0adc589d06fbb8b0d5fe5b15131e5124210a14d5`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0375e49eb81a62ee6208594c9fd6c9c2faede214b7a1c4d4a263bd1908edb436`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.3 MB (22332711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:c5e0b27a15f49b571f968defe19cc9a072d531ee90300ba5a1d2ea4dffa760e4
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
$ docker pull docker@sha256:23b5b1a900c5676eaee32c38dbdf727a37a6ace0c5980885a9ec21da619608f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74456477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6539186f04a7291f29d299010b9ab4b55d15e95c6b0e5a7ed5343225ebaeca47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:1133514976c34d263934880176c7466336c52b261e542275beeba2b0e5917292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966754ba178f5be30b512dcf67885f9543d39a53d5299d73a475f5f65ab3c216`

```dockerfile
```

-	Layers:
	-	`sha256:45b02f14e5b651223c3c46b95436ebab9917894f4d446223811103debafdf45f`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1c3cb277d90221fcd05b69ef6a0f498fe66939317b75f5018c1cc3ca76387ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69371203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a418a759b70319d7bb3094bb667c222c2e70891d056076f8f9348a047f66c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4b03cfc87f30735938381fcba67b7d48fb8e172a0426952a5c613717a6ba5126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0842d83a60027d875a0955c917c99c19935a96ef9827c37e655d72673286f2`

```dockerfile
```

-	Layers:
	-	`sha256:75aa001f9acf4b60bb11607334f3dfb7fc38dab3bc1b6fc5d19c4e11403b62a1`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:a38772a4376f984332843064dcd64529345698a31a522d9e743987c6e9fcf062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68383198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272d56ce0b6289e34fdc69a110e200627da4edddfd7d75df5a3d35e50091e40b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a80bd51374d59cccbe39550e29f3c75a4898d5c2b280388e8af740da9b07164b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f168959aace97d67eaf1304c91ac8dfbee2d113d5d8603c5813758c285776`

```dockerfile
```

-	Layers:
	-	`sha256:2810d6f734119f2a44d1165a8f025decfb025d213521b3e85924d093fb8f1354`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a00c0bc47f8908b1a966cb40ffdd06470593dc098b4d6c7ac356c7f7134f9de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70172005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0075144f78e3fc8d804eb929c2cf866a2ae0295c47f80dd57a7074863ba2736b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:c97d9cee1f1276f1b5c4f148387ce7f92a0f69d5d5805e39bf0a839fb8305949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7899ba69a193c95da9272216327b56babf9364894e32734aa60a0fc96bd2c0`

```dockerfile
```

-	Layers:
	-	`sha256:225c9a7352f7eb6df35d3bd7852ecf7eb0f840312b66c6ae6e88d4847326bf7e`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:4924fece44d61eeec47f619a4c35cd70fa2a31cd36b6283943a122369549fb82
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
$ docker pull docker@sha256:c4b520b9a63e5115f6d9843c62522b6560756164554b5c9a3a9c20bcb552e3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141638455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7ea23310b3fff4bbef36e8b08d5235dffa4d1aef78d84779d009e52daf7199`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:147e7c33d9e0781984a50137a65ab2801e4cbb5f519794b0b305a0f10539b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae01ef61862c7d28c4e48daaf3bcab61392d36b8995d1a304c28484403104db7`

```dockerfile
```

-	Layers:
	-	`sha256:01580a980dc523731ae2593398ec17f2aee10cc2224a12eec7f40edd279f0c15`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:acd9933ad265f50391c17d366e6b8b2774345d83655ac9eb52b18eb42a1140dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132245125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811d9a6156b3817de2198edbebe33a6c8cc87db51c522c2551723096b7fe9e55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0bf2e3301b433097f02a64cb68c64719a9d601c4c4e8199753a97d2eca08f5`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 7.0 MB (7036910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bea1f449ae4828750de8d364675e658773d2395554fb8f6e5b27abf6650d4a`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50285df7a34e25624ea34e42fcd0a315257b55c57443f5e1c9f7d87a64844be`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e48adef24818df5086795a0b59c0920fcbeab02b52b14b3d2948aa8dae560e`  
		Last Modified: Tue, 25 Mar 2025 21:57:04 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e6cc859de766f4621a9057c7a584c0bae06240f47f49125d0a53b0ccf2817`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b02adeb27e77008de20f43b04c15f9400674028dde877ca2c85db228d63833`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a062c1bae3694f2dc57a86f1a0a31f0646edbe073ba3b5332b7ea703fc95439a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6e9ff128ff3dd627ea97a881ed9d45513bfbbdd3ae431e585925664bcb1073`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b93d052b010bed3a7a457c00779ec2ccbd5200b802737da2302f23898bf0d`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5aec0cd9338b8c87a48d32538f1126aa1ea564bab5e0f88c2c3711887986e8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130582961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c8e6ea19a06349bd3fff8b36b6edc473d618f00fa98e0cf2b2245a333ec036`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e99727b81f4572b85e4f50bb748f74834c084c2be0336f0861ec92f578aab1d`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 6.4 MB (6366260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a406bc3246700b25d15b9a21a2c297aa03294574c920835f8e279fd40a99248c`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274227b3189ab05a7bcf8b5bca0a03e2da5a20fb0b29a005f653109f8307f13f`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d83b5ee45ba8b5cca7c66e593eed8890a19086546cc5b73e7aef977003052f7`  
		Last Modified: Tue, 25 Mar 2025 21:57:07 GMT  
		Size: 55.7 MB (55741247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82e270939ba77481d58f0731a8190051ed151ddeaf18ae9c71a711f5b23b19`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468d9090d7bb5417d46894a189d2c10a477709d8025de53c9684d708d936fbc`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:ef399f39c3375b2b26eef2b816ef0bc918beeebc2df752d98f6c8ff3d8af56e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba96e9df1e9b4b3f8af60be57bcef0cf7e05ce7cbdc423ad8100ccc83513eff`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a457447e187312ae0fcbe8833d37bc3524eca92d733dd57cbb2e2ce0e584a`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:223d046021f324792db4fbd1396746b63ffb93f00861ea390d7fbbaf392585e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132967037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a69ac0c9fe38a13675c478cc22e49748128d1bab3e99eb0e2c6be27dfd7d3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:64a2e28c40f0a0dfc87d02ef347ac0bc427ba0ffcc4b786312c6c94774615d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa29ab3f950e5f22976c193db0590a2c8448a680d52dc5423896788a0af100b1`

```dockerfile
```

-	Layers:
	-	`sha256:8d5656be0e9638a2cdce9ab5a83f7e3464efca3bceb222bd596af0b060d128a9`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:a5090d7c11c05a862ae22fbb478c62a4e9643fa431eaf7a9a7812fef7a67a859
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c06be5bc3b0e24f7f4b5ffbbcd8ca9ab02519562d691cb456f5d6b98f29c39c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159797561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13bdb47aeff8daa8094c59742ad7afc5ad9e580eec39dd8f76368cc62b7ce87`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded84039e564b9475ac7b125bcf4fb9502f33f947c0ddd3536f43effc60d6a54`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 986.6 KB (986584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40aafab5cc59e8f5cb5e26668f818b42db849fe877e95d7a3529e90d4a3c8bd9`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6da82905025ead3a593c912e1918488b0874da3fe3299e2a42bdb1cc934be3`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654321f2b23758f8b02e88231bb7f7f6dee732758055aea66fd4dce0973416a`  
		Last Modified: Tue, 25 Mar 2025 22:07:40 GMT  
		Size: 17.2 MB (17171184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3959b7e18a4fbdba386c18493c321ff4ca8830103acfcd3d187205a34cd112a9`  
		Last Modified: Tue, 25 Mar 2025 22:07:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bca820a790106f4866c59edf3d44fe79e09e9fa614e0a9f876c8919a5083f221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3323bffc2b5312b105253768c2c98037a504a39c4c7af0e7d7e1520aa6fb44`

```dockerfile
```

-	Layers:
	-	`sha256:e38eb0dfbf00e9814744fe5742ba05c41d5fa87629943046da2c159f210fa232`  
		Last Modified: Tue, 25 Mar 2025 22:07:39 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18a046138bef9eba3e6cf40129dd21388ec0a65d78a43003f1d93c8c8a4a075a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153264716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaf59ab004246a3948261b2eb47e4829eb00058acc9da25a1df6cff853a3f5b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cec22076d04d53956a39ca4217e9df0953e2089d2e7bc1927bef33d1228f4ce`  
		Last Modified: Tue, 25 Mar 2025 22:07:55 GMT  
		Size: 1.0 MB (1014208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a832bc3a23d3053414b32a049f9513b8654a574152e2b5d59d5616d4ab21e7`  
		Last Modified: Tue, 25 Mar 2025 22:07:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9308d557624dd27d66f0684ea0043bab12df8101320568cc69a8cdfead8367ed`  
		Last Modified: Tue, 25 Mar 2025 22:07:54 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48c2c7bc6b3fe5cf98c66408a3d4a051eaf3a7ef3c1aff1d2ebcb92c7d5e394`  
		Last Modified: Tue, 25 Mar 2025 22:07:55 GMT  
		Size: 19.3 MB (19282130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe93e7f39bff732dc1b6bad18045bb6d77a906b8672b73f15e5437aecdc1b9e`  
		Last Modified: Tue, 25 Mar 2025 22:07:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e4e4429f44acdd9a71ddee3e2e7db9d16cba204c73232fab6e85b41970d037dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7504d9409f225cb85c9078ba600e2b30c8e50444f521f6fa12ebd5a20c6703ae`

```dockerfile
```

-	Layers:
	-	`sha256:6d6cd4b0e7f4511463caf0aa1389476e27c5b8ef1a2ca5681666010a6d33f5de`  
		Last Modified: Tue, 25 Mar 2025 22:07:54 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:4924fece44d61eeec47f619a4c35cd70fa2a31cd36b6283943a122369549fb82
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
$ docker pull docker@sha256:c4b520b9a63e5115f6d9843c62522b6560756164554b5c9a3a9c20bcb552e3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141638455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7ea23310b3fff4bbef36e8b08d5235dffa4d1aef78d84779d009e52daf7199`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532d671d7887ad0d1a6f44050877e541618d2be51ea853e2ec0fe4f5a04a490d`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 8.1 MB (8062978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e69770cd7d2c3413809de64b4e7d342923e04f81c99489551f3dc11a9a905`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91a67d14af0329462e7c6e119d845e6ac6265627edc870b75faffb84881bb78`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 19.5 MB (19543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f9b60406823800ae1591ba1f57d9db2aafa4ea525abeead3d7253b0c05760`  
		Last Modified: Tue, 25 Mar 2025 21:31:07 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992adfb269ce5acb7f2c05a5f845d5f199b58f366a2ee488006719ff858b9d34`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 21.4 MB (21357078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632c4828a15d2768effca1ea6eb38d19938aae5abc1311d544c0cffec47000`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d9202faad59c1ea51b397a2c11b5686bf3abd66c09133931e9045237609b9`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971f1ed96862c2d678673f0e1726616ed6a927aa6506f1247165ac51c07726b`  
		Last Modified: Tue, 25 Mar 2025 21:31:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40a16065be58cd597a1a532b22ea63b37aa7a027f6de71f64d1c111a2d2623`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e0f30d232a0e91dd1e50f79e5cfb5baff9f9c99ea03becff3d27c9314d0ae`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 90.3 KB (90332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6257f3aeaf073dda3ea1320f5ebcc80d993616d1a63284ee4e8ac329b31e159`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a779817a636688ea167ab3907831dcd62f77a23906e559fbba1f32f462ba8f`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 60.4 MB (60352705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58914f08e9d9c2b35a572dc271a3d5080bfa1db8edec62c2f669ccd1dcbc6107`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f454196713ae68cc42c9bb4e1b320967277e1997d1e925590809f72ff298bd4`  
		Last Modified: Tue, 25 Mar 2025 21:57:21 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:147e7c33d9e0781984a50137a65ab2801e4cbb5f519794b0b305a0f10539b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae01ef61862c7d28c4e48daaf3bcab61392d36b8995d1a304c28484403104db7`

```dockerfile
```

-	Layers:
	-	`sha256:01580a980dc523731ae2593398ec17f2aee10cc2224a12eec7f40edd279f0c15`  
		Last Modified: Tue, 25 Mar 2025 21:57:20 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:acd9933ad265f50391c17d366e6b8b2774345d83655ac9eb52b18eb42a1140dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132245125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811d9a6156b3817de2198edbebe33a6c8cc87db51c522c2551723096b7fe9e55`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e62421f550cd2c2a129ac8d2f25e666bab9ec8df1eb0522d2e36c9d40efdf7`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.1 MB (20082306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ca9a8bb5dfda083058341925835e55e813c4f4c0edadaef94634944455751`  
		Last Modified: Tue, 25 Mar 2025 21:31:31 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8da1901492e5b4bcbcc5847fffd5546e858159f70ed4c790ba104c96e82600`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d38c6f1f0277ba6a19005d28e6828e708f4ea189eb8731930bf189b4e96c`  
		Last Modified: Tue, 25 Mar 2025 21:31:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0bf2e3301b433097f02a64cb68c64719a9d601c4c4e8199753a97d2eca08f5`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 7.0 MB (7036910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bea1f449ae4828750de8d364675e658773d2395554fb8f6e5b27abf6650d4a`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 89.9 KB (89864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50285df7a34e25624ea34e42fcd0a315257b55c57443f5e1c9f7d87a64844be`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e48adef24818df5086795a0b59c0920fcbeab02b52b14b3d2948aa8dae560e`  
		Last Modified: Tue, 25 Mar 2025 21:57:04 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e6cc859de766f4621a9057c7a584c0bae06240f47f49125d0a53b0ccf2817`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b02adeb27e77008de20f43b04c15f9400674028dde877ca2c85db228d63833`  
		Last Modified: Tue, 25 Mar 2025 21:57:03 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a062c1bae3694f2dc57a86f1a0a31f0646edbe073ba3b5332b7ea703fc95439a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6e9ff128ff3dd627ea97a881ed9d45513bfbbdd3ae431e585925664bcb1073`

```dockerfile
```

-	Layers:
	-	`sha256:9d6b93d052b010bed3a7a457c00779ec2ccbd5200b802737da2302f23898bf0d`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:5aec0cd9338b8c87a48d32538f1126aa1ea564bab5e0f88c2c3711887986e8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130582961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c8e6ea19a06349bd3fff8b36b6edc473d618f00fa98e0cf2b2245a333ec036`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd7bddb2ccf1f07d92bfc4a81eb5803b250de652881055e35f90436ee4abf9`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 7.3 MB (7300662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb3576c08b6921b2e40016468d0bc96cbae6a5bd1f30a1822e9193765c62ac`  
		Last Modified: Wed, 19 Mar 2025 04:32:31 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f950a10395805c827f4f7924974daedcaec49169a553fc5918b64d0f8046a054`  
		Last Modified: Tue, 25 Mar 2025 21:31:04 GMT  
		Size: 17.5 MB (17486336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476134ebe76085f5724e522d3cebb7586f591d0c0dbcbb90bcfac458339514d`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.4 MB (20429564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628987ff573f4ed7824f0603a1f701a6dab1d36e5dd7e54f46f27e85b21f0547`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 20.1 MB (20066348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463799688e4daf7bc16dab7b02a4699b92ae1dbca872f95f31a4ff0b098096f`  
		Last Modified: Tue, 25 Mar 2025 21:31:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42902832a9963a13f94d1e2e18e433b479abd67ebeb8088e541e20f755f4c0`  
		Last Modified: Tue, 25 Mar 2025 21:31:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f0d670ac84b2e56c1faaaa4a16495ddbc014b16ef15cd503e95bd7fad44f42`  
		Last Modified: Tue, 25 Mar 2025 21:31:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e99727b81f4572b85e4f50bb748f74834c084c2be0336f0861ec92f578aab1d`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 6.4 MB (6366260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a406bc3246700b25d15b9a21a2c297aa03294574c920835f8e279fd40a99248c`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274227b3189ab05a7bcf8b5bca0a03e2da5a20fb0b29a005f653109f8307f13f`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d83b5ee45ba8b5cca7c66e593eed8890a19086546cc5b73e7aef977003052f7`  
		Last Modified: Tue, 25 Mar 2025 21:57:07 GMT  
		Size: 55.7 MB (55741247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82e270939ba77481d58f0731a8190051ed151ddeaf18ae9c71a711f5b23b19`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468d9090d7bb5417d46894a189d2c10a477709d8025de53c9684d708d936fbc`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:ef399f39c3375b2b26eef2b816ef0bc918beeebc2df752d98f6c8ff3d8af56e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba96e9df1e9b4b3f8af60be57bcef0cf7e05ce7cbdc423ad8100ccc83513eff`

```dockerfile
```

-	Layers:
	-	`sha256:fe1a457447e187312ae0fcbe8833d37bc3524eca92d733dd57cbb2e2ce0e584a`  
		Last Modified: Tue, 25 Mar 2025 21:56:59 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:223d046021f324792db4fbd1396746b63ffb93f00861ea390d7fbbaf392585e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132967037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a69ac0c9fe38a13675c478cc22e49748128d1bab3e99eb0e2c6be27dfd7d3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61622ecb2cecf37b3100c34e9d1a4a84e59dcfb134d0252acc226ec0498a485`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 8.1 MB (8076616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16494c114cd37717129974da809751157ee671adff9246ce093d1d8ae68be08`  
		Last Modified: Tue, 25 Mar 2025 21:42:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77aa33f5637ec21c236f4e8356f4463a4a7eaf48afceec7a86193546bc8af15`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 18.5 MB (18457147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d053f9df941bb3eda7825567c1f216f686503af9f7ca966c1e79b3869376e9`  
		Last Modified: Tue, 25 Mar 2025 21:42:08 GMT  
		Size: 20.1 MB (20061171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebaf976d730825098b867ab3aa2644c747198ed4142947194dabaa5f6206009`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 19.6 MB (19581889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb520adbb16bf8e547aea5596db14827361b3bc36fe30be7f002b595fcaf4e`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c95f1d6a231ee889e70be2d9c74b7445bfaf303ce171b18e7b344bd964be11`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd63d1a1ff03a69fd42d737b9abdc1d58865ad8414b5cdef227900f09155de6`  
		Last Modified: Tue, 25 Mar 2025 21:42:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd0d76ef0d30deb2c4192a94299d5c4ea6facb898a0b0578f4ae069d78c00a7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 7.0 MB (6978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ddb316d364d6772fc25fe9f57b2ec7cf436bc1952faa6a0cfefed6d343bb7`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a224a01ea8a93baa91e3d699e5cbe9e3b18a50b290568a6ba884c775eb93a4`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b998ffd0151bc6bdcfe96eb34ade91cf898ad70c9856709185e2ba0ef868f8bf`  
		Last Modified: Tue, 25 Mar 2025 21:57:02 GMT  
		Size: 55.7 MB (55710877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5f37bae6ea1cb744771e61e6c55f727698cc903626098b552791420244bd9`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9acc67c804289fb3f4eab2c4034b983adc8f77e65399afca34a494551843000`  
		Last Modified: Tue, 25 Mar 2025 21:57:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:64a2e28c40f0a0dfc87d02ef347ac0bc427ba0ffcc4b786312c6c94774615d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa29ab3f950e5f22976c193db0590a2c8448a680d52dc5423896788a0af100b1`

```dockerfile
```

-	Layers:
	-	`sha256:8d5656be0e9638a2cdce9ab5a83f7e3464efca3bceb222bd596af0b060d128a9`  
		Last Modified: Tue, 25 Mar 2025 21:57:00 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:fdbf04adec3070897345d1e057af86328464a4e11f3f7426fc7b27e94e2eb517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:37fbf58c618a1e257ff62a5c17597a58c612390d9b8248b12de620ff0dc27116
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974098228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d876f863caff9ced5d2166306316ea67c3e8f29ecd77f820b472be5e597514de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 21:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:36:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:36:02 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:36:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:36:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:14 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:36:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:36:16 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:36:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:36:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230d8f91a46ec72be09fa76d5ed5c5c953b39e08a445f5dc09dacc9ee44eb74a`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497744dd92652df503964233d52071afe6b6da69fcc9d699ecdef8a81132716`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 393.8 KB (393794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bbe029cc51bac0aa9cdd3ec3325e113f38f3632cef853c3d488b1b1641adae`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e6465d36bb7dd3cbd69b2e9a38b3544b7eab714dd64a6c38788e616627500b`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9179050a0c68ba8475bf29ed21dd34e7d54d5f314a7ac42b2fca85710f90f32`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 19.9 MB (19904481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3871cbf913d4865bf43a87c7cbf2227b2705afa74b1281dba34fe25af1a73e5b`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae86510368ad79d177019fd99371ebda2255844ae98eed60c771294d11b158db`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1c6e4bc9abf47f577d2fea496c8dd7cd245ef59f6342b8274eb1e1bfe3deb3`  
		Last Modified: Tue, 25 Mar 2025 21:36:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944b89a3759e186bd3d1e0373910a72d0c398b453c235e4e3859f193aafb6f7d`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.8 MB (22807812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3fe3114e244b2f87a8272a1e53a7be89778c0f0609da78972fa83adf80028`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3bb7f5e52b615856b2468cacce7cfda132ef42d917ec6c7b1ed45144fd6574`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711261a97010fbb377d12b5a0adc589d06fbb8b0d5fe5b15131e5124210a14d5`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0375e49eb81a62ee6208594c9fd6c9c2faede214b7a1c4d4a263bd1908edb436`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.3 MB (22332711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:f99d03d930f93e2749004c210255ac7f6b52149af0a79f27716da370fa7b1eb6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335275907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c5fa0da0dfcdf03eeb0a5cc8d07e757bd37f4f77b4f8a064d43809c323c1c8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 25 Mar 2025 21:37:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:38:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:38:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:38:21 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:38:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:38:30 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:38:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e87728e165e6772cede047713a447fd6e30659d8dd65ce204231ed4a7dbb0e`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe917f396787792b92fc9c8f5959b2f8be7522c5b2d400aed59e46867d04a`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 371.5 KB (371494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c896757855fa4e3de01285214ef7138cbe36c12ca479b1124f575ee219dcac`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4036332907e21a93b9f46503d71b483e433e9268f61846e8fd3669ad8e8260`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f2151a5c434f05d2e41c3bf031037cf88d7a152683a0aa34b1e6d50e55f5d6`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 19.9 MB (19873533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd21b973a1b5c558975227864cfb89ba209e894f4a446b40afd17ec3b9ee9a80`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce9542ef040e9bf201f9a54875111a9eba23bb63caf4a022c127d73bb8fc7b8`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb91e206b539328afd55e6043c5c2825cfc67484bb8ff7055f76034431f02a83`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111bedc1382fe6bceb4dc527c273e3e88d670a978f867793f8cb11dace8ab00`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.8 MB (22775231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9293f4095824ab934e2ea69a23a4ea9e5b880f5e5d4a0f1bbf1cc5543e5a9`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f1c82a5ed7da58754739b095aac5f1ec0fe3aea0d48069290cfc0c9af4c4d`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608603ddb53750c36f5d27ef3c6d70b3d90ebe2430701772a11a1dc8ab625795`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63caecab4c5855f0c5198d61e2ec9cb95d046b983b51c66bdafcfe9383dad979`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.3 MB (22302869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:a07b73a00a3c52cf508c570e374efc24be0c453d86c9452fcea303ba531ffc8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216893552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a9a00b1e30a51e5c8dc78b5d38184a68cda33f84d782e8bf6ef53aa9e235d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 21:33:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:34:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:34:13 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:34:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:34:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:25 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:34:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:34:27 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:34:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:34:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:34:38 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:34:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a524a0e9cb7afa4d4cd71cd32e949c44f21cba76046ad004d2d6d09870f93ca`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847dbfeb702fcf37b419ad4ed9aa7e21d43d27bf895a29d8da424b6b58d57dc`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 340.0 KB (339963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edce44d57bdec9498491ec04581f5193d08ac7cfe87170c1368d3f2456d40268`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c046029f114363dc51b43457767bcb3f623e3c8f32e8ca7f9b2db9d7972f56`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ee9950b1bd1e3a417a9674a6ed4ba90d4b0101a2aad3d904faf071830bd11`  
		Last Modified: Tue, 25 Mar 2025 21:34:58 GMT  
		Size: 19.9 MB (19859748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5786612fd2d55be281d632baaa5e172f6bd8458061b5ecf3bffedb71d6de9`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0a2088c740ff617b174a979824713e0ad78fe077aa205af5340a6aa886e39`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71a201934e91595d89a5cda2c3f1824c4766cda3ae640a1e8f7dd00e3a33ad`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dd615d0c7c6f688705646fd983a540cca62d8d975b8fd767e83954950ba82d`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.8 MB (22763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e870735d52bdad39865ea0295c463823531285214d901abdf128dca151e17c5`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e5d174601f7707cecf5521b4bdf1b1198187a4844a00a623a89d78257bdb1`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7fcbbabcb3464ee277100b9f6fd1c395109f1ce5de50e92adc5431a6beb04`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176d290ac87077c88ca4ce30853fd4d9020a6eb3dbc3df72610e011d5869d562`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.3 MB (22283549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:c8052ef5f90cd2fa3c44394fec8378a887db5d87c66f6d5af683b3082f4f3658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:a07b73a00a3c52cf508c570e374efc24be0c453d86c9452fcea303ba531ffc8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216893552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a9a00b1e30a51e5c8dc78b5d38184a68cda33f84d782e8bf6ef53aa9e235d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 21:33:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:34:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:34:13 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:34:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:34:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:25 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:34:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:34:27 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:34:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:34:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:34:38 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:34:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a524a0e9cb7afa4d4cd71cd32e949c44f21cba76046ad004d2d6d09870f93ca`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847dbfeb702fcf37b419ad4ed9aa7e21d43d27bf895a29d8da424b6b58d57dc`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 340.0 KB (339963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edce44d57bdec9498491ec04581f5193d08ac7cfe87170c1368d3f2456d40268`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c046029f114363dc51b43457767bcb3f623e3c8f32e8ca7f9b2db9d7972f56`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ee9950b1bd1e3a417a9674a6ed4ba90d4b0101a2aad3d904faf071830bd11`  
		Last Modified: Tue, 25 Mar 2025 21:34:58 GMT  
		Size: 19.9 MB (19859748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5786612fd2d55be281d632baaa5e172f6bd8458061b5ecf3bffedb71d6de9`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0a2088c740ff617b174a979824713e0ad78fe077aa205af5340a6aa886e39`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71a201934e91595d89a5cda2c3f1824c4766cda3ae640a1e8f7dd00e3a33ad`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dd615d0c7c6f688705646fd983a540cca62d8d975b8fd767e83954950ba82d`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.8 MB (22763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e870735d52bdad39865ea0295c463823531285214d901abdf128dca151e17c5`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e5d174601f7707cecf5521b4bdf1b1198187a4844a00a623a89d78257bdb1`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7fcbbabcb3464ee277100b9f6fd1c395109f1ce5de50e92adc5431a6beb04`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176d290ac87077c88ca4ce30853fd4d9020a6eb3dbc3df72610e011d5869d562`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.3 MB (22283549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ae68b9f2e53406551f2704648cf0197fc3499d7003d00f8dbde54b97cd9f1a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:f99d03d930f93e2749004c210255ac7f6b52149af0a79f27716da370fa7b1eb6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335275907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c5fa0da0dfcdf03eeb0a5cc8d07e757bd37f4f77b4f8a064d43809c323c1c8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Tue, 25 Mar 2025 21:37:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:38:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:38:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:38:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:38:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:38:21 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:38:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:38:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:38:30 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:38:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e87728e165e6772cede047713a447fd6e30659d8dd65ce204231ed4a7dbb0e`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe917f396787792b92fc9c8f5959b2f8be7522c5b2d400aed59e46867d04a`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 371.5 KB (371494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c896757855fa4e3de01285214ef7138cbe36c12ca479b1124f575ee219dcac`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4036332907e21a93b9f46503d71b483e433e9268f61846e8fd3669ad8e8260`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f2151a5c434f05d2e41c3bf031037cf88d7a152683a0aa34b1e6d50e55f5d6`  
		Last Modified: Tue, 25 Mar 2025 21:38:48 GMT  
		Size: 19.9 MB (19873533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd21b973a1b5c558975227864cfb89ba209e894f4a446b40afd17ec3b9ee9a80`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce9542ef040e9bf201f9a54875111a9eba23bb63caf4a022c127d73bb8fc7b8`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb91e206b539328afd55e6043c5c2825cfc67484bb8ff7055f76034431f02a83`  
		Last Modified: Tue, 25 Mar 2025 21:38:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111bedc1382fe6bceb4dc527c273e3e88d670a978f867793f8cb11dace8ab00`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.8 MB (22775231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f9293f4095824ab934e2ea69a23a4ea9e5b880f5e5d4a0f1bbf1cc5543e5a9`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f1c82a5ed7da58754739b095aac5f1ec0fe3aea0d48069290cfc0c9af4c4d`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608603ddb53750c36f5d27ef3c6d70b3d90ebe2430701772a11a1dc8ab625795`  
		Last Modified: Tue, 25 Mar 2025 21:38:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63caecab4c5855f0c5198d61e2ec9cb95d046b983b51c66bdafcfe9383dad979`  
		Last Modified: Tue, 25 Mar 2025 21:38:46 GMT  
		Size: 22.3 MB (22302869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:b25d93a59fbdb43e27ccd5ff42b9a530d1c07616c048664e2a9858300a0817ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:37fbf58c618a1e257ff62a5c17597a58c612390d9b8248b12de620ff0dc27116
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2974098228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d876f863caff9ced5d2166306316ea67c3e8f29ecd77f820b472be5e597514de`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Tue, 25 Mar 2025 21:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:36:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:36:02 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:36:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:36:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:14 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:36:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:36:16 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:36:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:36:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:36:26 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:36:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230d8f91a46ec72be09fa76d5ed5c5c953b39e08a445f5dc09dacc9ee44eb74a`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497744dd92652df503964233d52071afe6b6da69fcc9d699ecdef8a81132716`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 393.8 KB (393794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bbe029cc51bac0aa9cdd3ec3325e113f38f3632cef853c3d488b1b1641adae`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e6465d36bb7dd3cbd69b2e9a38b3544b7eab714dd64a6c38788e616627500b`  
		Last Modified: Tue, 25 Mar 2025 21:36:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9179050a0c68ba8475bf29ed21dd34e7d54d5f314a7ac42b2fca85710f90f32`  
		Last Modified: Tue, 25 Mar 2025 21:36:46 GMT  
		Size: 19.9 MB (19904481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3871cbf913d4865bf43a87c7cbf2227b2705afa74b1281dba34fe25af1a73e5b`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae86510368ad79d177019fd99371ebda2255844ae98eed60c771294d11b158db`  
		Last Modified: Tue, 25 Mar 2025 21:36:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1c6e4bc9abf47f577d2fea496c8dd7cd245ef59f6342b8274eb1e1bfe3deb3`  
		Last Modified: Tue, 25 Mar 2025 21:36:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944b89a3759e186bd3d1e0373910a72d0c398b453c235e4e3859f193aafb6f7d`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.8 MB (22807812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d3fe3114e244b2f87a8272a1e53a7be89778c0f0609da78972fa83adf80028`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3bb7f5e52b615856b2468cacce7cfda132ef42d917ec6c7b1ed45144fd6574`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711261a97010fbb377d12b5a0adc589d06fbb8b0d5fe5b15131e5124210a14d5`  
		Last Modified: Tue, 25 Mar 2025 21:36:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0375e49eb81a62ee6208594c9fd6c9c2faede214b7a1c4d4a263bd1908edb436`  
		Last Modified: Tue, 25 Mar 2025 21:36:43 GMT  
		Size: 22.3 MB (22332711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

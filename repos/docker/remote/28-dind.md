## `docker:28-dind`

```console
$ docker pull docker@sha256:bb13057e7a4c3d0523d83958633bf2b20b4cb38b623dea953d6dcfad26b1813d
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
$ docker pull docker@sha256:ba9e6ab104fa645c666c812507daa07fdd02945ab5316e085ab713509300692c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141417240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1c1104d634c82285e9d424191f9f62b408ec1d9a46b197eab113030595f758`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cddd6035f6ee430367640bd7af33091d7cd51aef46fd6a646e82e59a5722336`  
		Last Modified: Fri, 14 Mar 2025 20:15:34 GMT  
		Size: 8.1 MB (8062960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18545da70da8de902aa7945d6834808f55c56985af572adf86a2ddc74e5a5809`  
		Last Modified: Fri, 14 Mar 2025 20:15:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220f4179a2b2b881086f568e1f6ad14ca78012d3075c8892db29a36c52400ebe`  
		Last Modified: Fri, 14 Mar 2025 20:15:35 GMT  
		Size: 19.5 MB (19500687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9220993bed801cd864971e8b0ae3de720553b5b0002cceb48f8a0294c2dc5c9d`  
		Last Modified: Fri, 14 Mar 2025 20:15:35 GMT  
		Size: 21.8 MB (21830051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef975247b87b11073125bb0aff8d52a75f567e2b707407b6cd2af31cff6010c`  
		Last Modified: Fri, 14 Mar 2025 20:15:35 GMT  
		Size: 21.4 MB (21357079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594be6b8b01a1895293ee747769d346c3a128a1feec8bdde1697ff74f2f78a99`  
		Last Modified: Fri, 14 Mar 2025 20:15:35 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7334c0b0e22860da65e28386ef15b30ad3d1f6fb6bf00bcd2ddfc55292224431`  
		Last Modified: Fri, 14 Mar 2025 20:15:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc080bf4714cb5ed3c83f271281258fe8e79f02525513b7df67940c6c5578d`  
		Last Modified: Fri, 14 Mar 2025 20:15:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a1c42642188e848cca62700d2d73b9d0556056a7b8d076c7906bbef7dc507`  
		Last Modified: Fri, 14 Mar 2025 21:12:37 GMT  
		Size: 6.7 MB (6733007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751900429f917e262b747b6000d73fc5ffa41d71e3a32d91bbccabe167f3a226`  
		Last Modified: Fri, 14 Mar 2025 21:12:36 GMT  
		Size: 90.3 KB (90323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3681dad7d9ca4c66d68cd23105a4d3e12c0046982ea228c2a18cf01c4ac7b4a`  
		Last Modified: Fri, 14 Mar 2025 21:12:36 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b738daae645c7c7a9f30dfc21ec7f228bf89a06e991f3f90df58ee1258bd70`  
		Last Modified: Fri, 14 Mar 2025 21:12:38 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449697c236e840ee51f8a3a2dbac933a5d01eca6608e74be15f0ab8eb693c19d`  
		Last Modified: Fri, 14 Mar 2025 21:12:37 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ab4a486c31108972495b0c24581798c04db66fe8599abe7061e93589141535`  
		Last Modified: Fri, 14 Mar 2025 21:12:37 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:33c375d0e5ac644fc087ee2bb6f819abfd3d22291039e59cd06fb428d5eedcb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e132df6268a3e2f033aee2979a41ccf324fb078ab3d3095c794d99184a7ec49`

```dockerfile
```

-	Layers:
	-	`sha256:91349722eaa9d569c9a1216055ffb88e1b63ead1ca63b9fd1b3b099438d7dc8f`  
		Last Modified: Fri, 14 Mar 2025 21:12:36 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:7af8b007c70db35b6b4d34ad7b1292dcc7827a6a43249dce772e585b75877f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132049135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca56e7951f5221a403ca9c15a11faffe8ad96027e7dacb2a1df1f1da5753387`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
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
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e4c620d7d7e2aa96674c0dc6283557c324f1cafd5f64c9e33624fa4153ad4e`  
		Last Modified: Fri, 14 Mar 2025 20:15:19 GMT  
		Size: 20.1 MB (20082307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa262714574647276ca6dfac8e5cff27a3d95d8d936ebce92285ae9eb4a0f68`  
		Last Modified: Fri, 14 Mar 2025 20:15:18 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db09fda4f9d4de8f56686826f58acff9104e23dc12584e07ce627c7bbd5296e5`  
		Last Modified: Fri, 14 Mar 2025 20:15:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee99e3d53c955251ac1d12c382fa92a253c614477948fd3e31bd6cd9e3481c2`  
		Last Modified: Fri, 14 Mar 2025 20:15:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56037fc5e1fa897202eb6f5ca93bd3eec1e6d8f3745b56f813f321d4389653c2`  
		Last Modified: Fri, 14 Mar 2025 21:12:10 GMT  
		Size: 7.0 MB (7036943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23743e2b72336f20b5c05575fb20ae833468288ac0d99987028b74a09b6932`  
		Last Modified: Fri, 14 Mar 2025 21:12:09 GMT  
		Size: 89.9 KB (89859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a729fc6c91a7c37da34c6a344bb5771e6c0e076de1d28006b81c2b8d1298417`  
		Last Modified: Fri, 14 Mar 2025 21:12:09 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f6b69dbd6a026c5796ebbc15d78e62eae36ad9ee406936702b31f7eabec890`  
		Last Modified: Fri, 14 Mar 2025 21:12:11 GMT  
		Size: 55.6 MB (55593692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14102c2fd80cd2d6dfa7d03eafe2c996152b71af2a25bd3613d80d7cbc21a092`  
		Last Modified: Fri, 14 Mar 2025 21:12:10 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ec845d40b9dda6b938ffdd5ca17769d4552fb94e0f4962dc59cfc42baffd49`  
		Last Modified: Fri, 14 Mar 2025 21:12:10 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:655e8440e0d9ecf5661dc4f1ed3dcfc004469aab6d478f2b2ec687c1fe0223f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dbcad21ecd0de247a29133db025d93f850d19e0577a064d44ef7a3cd55db93`

```dockerfile
```

-	Layers:
	-	`sha256:92b70dd7aa18033c7a2250f1b9c4e60d51b49e6722bf3e120670545070177d04`  
		Last Modified: Fri, 14 Mar 2025 21:12:09 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:05883987356d7f2b28e785e0c98411791033e75c7594688eb66d1a0db75a892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130382942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc322d32470857db2fae3bcdcd6f94fa963581539b2bb5205ccd14009f56f816`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac4f42926ddc5b3d221ef4c76a2980f784ef8a8e7f1bf1de6f246dc4b5974d`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 7.3 MB (7299504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34e0189da9d2b0a101d5c9978d1d2977cf9c409ba0d5341a29e06469df09c9`  
		Last Modified: Fri, 14 Mar 2025 20:15:43 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d16a61567634fdc8eac3b4e5fe387d97c0f6a08c1418e8b8fef8911b1d66707`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 17.5 MB (17453626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45e2e470f76c83eaa44d00a8ebcab9b2c9cb9ff8ac07cd9a99ec65c15e675f`  
		Last Modified: Fri, 14 Mar 2025 20:15:44 GMT  
		Size: 20.4 MB (20410963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f21db8449836680ec88782fd7529f4116b626741160a0459f7310d68037586`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 20.1 MB (20066347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c06e55db74c0432d6e0d6bb639d398e3c4bc66c2ee1a239d1033008c693412`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f0385aff3ff0b7fd0763daf50718bf4e8940a7883c7cdff795bcd204064cf3`  
		Last Modified: Fri, 14 Mar 2025 20:15:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989697c5dc6b6e622346d2f1e11f2c6f3ed997b332292d6a9eaedb0d29d4025`  
		Last Modified: Fri, 14 Mar 2025 20:15:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04248460f4f43dda114cf6e38bd72647f90344cc42043161295d8a77bb78f15a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 6.4 MB (6366336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a248db7df30a00f0d2a17263b4f5d6b39ac19a2f086f95f1f7ee5181fbd6ff1a`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 86.3 KB (86343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7413c171635e268ad441559ac341509383d0976e68d8a2e9db87346c6d946e2`  
		Last Modified: Fri, 14 Mar 2025 21:11:57 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2143b75dc215725319c90f47ba313cdbf7f5122e30ddb6f234dd5b6a770d`  
		Last Modified: Fri, 14 Mar 2025 21:11:59 GMT  
		Size: 55.6 MB (55593647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266db4b4f66e90d74f43dd7ded419a89c5a9e048191be6e81055e0e03d3f3a5a`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8cc5b9a67b353b2df6581e3a544618582ca576f2d7c79d45b87fb4ba98477`  
		Last Modified: Fri, 14 Mar 2025 21:11:58 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4a44e37e075a395cc4355a8aa3064dab865c450125c889f99cb5a8f470bf5bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d583b2c788713970578b9a323504d5586eec6c267e185a0b04bda8960c932fcb`

```dockerfile
```

-	Layers:
	-	`sha256:7e5ffd9071082203139db743e85aa7abfe2b617598eac876a4750cd6c30d3d8e`  
		Last Modified: Fri, 14 Mar 2025 21:11:56 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90ca9797ce316bce5ff74d335c304e85d41d6bd981f755a3281858072bfc839a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132411588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0250bf64dd26b5fe7a1a358ac561aa69a69de05ac454d6de509ef789813a11`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f5b23b2ecb5219b4fd968f4f0e77e03bd1739c249efd6cd9743ff73138a96a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e084d1513f7ecd8f052a99a580b237130bd85603d5bacaacf72d2e9508170e20`

```dockerfile
```

-	Layers:
	-	`sha256:36cdd24344a437d2b167b4b38ada68f9f95a41ad871c683e3146b271a927edca`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

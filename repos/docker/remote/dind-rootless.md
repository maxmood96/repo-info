## `docker:dind-rootless`

```console
$ docker pull docker@sha256:c3c62efbb921f12526e23305793bad43bc645ce70135ebf78540b6d11e993a2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:30a179564161ce3db68df4c238c13e3ea4db088ab8c5161ba2950574961f000a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159318571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929cb4542115a57c5a72c5b4189d8c412efaf84087a663749a738774e67ace6a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD []
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f5f64c726e2c31d560c8d9754340c9f1aeb301d60047e17b771570e92ee4de`  
		Last Modified: Mon, 19 May 2025 23:46:14 GMT  
		Size: 8.1 MB (8062931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1622324b9f32d2c28ed38601b18d9b823ae89f2e47af430b21692884ad1ab62e`  
		Last Modified: Mon, 19 May 2025 23:46:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8044a81615b9ecd78ed519e318c69de5cd2f77a95ff6f27f7376f005c40333`  
		Last Modified: Mon, 19 May 2025 23:46:18 GMT  
		Size: 19.6 MB (19565542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534946bec48bf3ce6f05f225e28d61d3e1c810174a98ff2fbe90c52d240132f9`  
		Last Modified: Mon, 19 May 2025 23:46:19 GMT  
		Size: 21.5 MB (21456661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d105ef29bbb02f078851b0019ed6241908d28d730a79b0896c39a8414e74ba77`  
		Last Modified: Mon, 19 May 2025 23:46:19 GMT  
		Size: 21.2 MB (21208008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bba9fb730a01da2b73429eb39827fcdbc65a19fe4af5d05db12698a1a6778fe`  
		Last Modified: Mon, 19 May 2025 23:46:15 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee246c8fb4e8702cdd4185e37c04495ff7c3f6857c21e1ec169eed0d1963c17`  
		Last Modified: Mon, 19 May 2025 23:46:15 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ab34ed322521e0a053c344589f8cfb12e95dd9b2cebe14be1c8a14272ab8e5`  
		Last Modified: Mon, 19 May 2025 23:46:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc414b40c5bb1fd10088625e86b2c5fb10acb7c89e9da592ef44518e0d62d82`  
		Last Modified: Tue, 20 May 2025 00:08:25 GMT  
		Size: 6.7 MB (6732944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc24f68ea2a77e7da1313297b1cbee79b32445f8ebc704d7b777887df25796f`  
		Last Modified: Tue, 20 May 2025 00:08:25 GMT  
		Size: 90.3 KB (90330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7296af326011b1111aadbd9e46349a053311cf3956ffa82695749af1628206f8`  
		Last Modified: Tue, 20 May 2025 00:08:25 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4173df17d998368c463573dfb5509963b8715648b8113c81908e65cd4a134c09`  
		Last Modified: Tue, 20 May 2025 00:08:46 GMT  
		Size: 60.4 MB (60382725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40017b6cebfecd1e367c53f56688105b07a577f4aa29001f4d1667bbb748162e`  
		Last Modified: Tue, 20 May 2025 00:08:25 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac5abd680038af59ceca0f8b22693c143278d2d96cdb421f49404248c1dc587`  
		Last Modified: Tue, 20 May 2025 00:08:25 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c859f4f0ce698349c4b1670feacf7f44f21d069d97cd0b4cbdf36f2d4d303d6c`  
		Last Modified: Tue, 20 May 2025 01:08:07 GMT  
		Size: 986.6 KB (986589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119186f245153c01d9260fafbac7e09be2730fb4b938abbc5fbceb9525138f09`  
		Last Modified: Tue, 20 May 2025 01:08:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ea745fac929a25186167d3c4b9e0a0c7386288411c8812c732d53447d2f466`  
		Last Modified: Tue, 20 May 2025 01:08:06 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14941c2cce58ed843a139518e632521deb14ed369c66458a4a1118931fdc8da1`  
		Last Modified: Tue, 20 May 2025 01:08:10 GMT  
		Size: 17.2 MB (17181095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41401dda02d62c7455ed8aac9b72c71ade69fdc4178038d71ae84dc189be9be4`  
		Last Modified: Tue, 20 May 2025 01:08:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3132df6bb834be1e1654ca817651e10ac94f93862c895389df7e18837ff02364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9535db92bfa840d5e7baa905f8141b1a8686bed1931f5949aca3a3181ea248bb`

```dockerfile
```

-	Layers:
	-	`sha256:ac3f34c9937a129e97c255328675b7843ace8887e65dd40d7a0c29c770b2b5e9`  
		Last Modified: Tue, 20 May 2025 02:07:52 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7a824e30fac00458a455f6acc5bbe10a77240c794965c593f7f7906784ad3da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152801026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5bf56503ac660b9ee950625000a392c7f0fd0c4410e2f46a5aef7b8b16d300`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD []
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fffdd893f2edce36ae9ef8552b4908e678780ed400d81510a7672b934b2c9b`  
		Last Modified: Mon, 19 May 2025 23:45:49 GMT  
		Size: 8.1 MB (8077199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d86e9e1048e11c509f223efe8388ce6b460fb5a34e23a02d017ec34b2c5bebd`  
		Last Modified: Mon, 19 May 2025 23:45:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8cfcc483cc0d3227380016efaba99a3dc92470f2827fa75dccc8ca8424a997`  
		Last Modified: Mon, 19 May 2025 23:46:33 GMT  
		Size: 18.5 MB (18485710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72096810dddbe61694cb28a92436375fdcdf8d04c0969f2e93abc8f5730dbd29`  
		Last Modified: Mon, 19 May 2025 23:46:33 GMT  
		Size: 19.7 MB (19692479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78d7b972c4bcf0f49e6b55911ae32a6ed70adbe9e1acbb9b8d6395d79f67655`  
		Last Modified: Mon, 19 May 2025 23:46:34 GMT  
		Size: 19.4 MB (19433940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc7f40ad492f29c1b857d995c206c26ea37323e4a5ee819db8b294f6bd1f34f`  
		Last Modified: Mon, 19 May 2025 23:46:34 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435f7c0924da6a8d18ba41fd7360142b67e4fc934e5642b344c9c3c65e37e50`  
		Last Modified: Mon, 19 May 2025 23:46:35 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27463e47c9a363d4fca5ee76f3fac35cf25f3871c0261aab9df41f56343195c0`  
		Last Modified: Mon, 19 May 2025 23:46:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0626b8202fa0d3ba00c0e04b37318d0af43b1835390466a69658720167f734`  
		Last Modified: Tue, 20 May 2025 00:26:33 GMT  
		Size: 7.0 MB (6978741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0204e09a249d4787244c6e9df4be2c5c17c36eacef272c7676bc09793c565dc`  
		Last Modified: Tue, 20 May 2025 00:26:33 GMT  
		Size: 99.4 KB (99404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe977f3312f0771485c86307665f961a9934106aa9a312e4135f4b0a26a608c2`  
		Last Modified: Tue, 20 May 2025 00:26:34 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec7a5f04f87228c778b5eb2168e49e2f4e9712748cb1be0e24c7be9fdd24e5a`  
		Last Modified: Tue, 20 May 2025 00:26:53 GMT  
		Size: 55.7 MB (55741026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbfbd56c712018c4f3e3a4ffa62c154884c36fd2331de765ee5f61a85fb2ad6`  
		Last Modified: Tue, 20 May 2025 00:26:34 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192d363e300d6b15499c1b596aaa197553dc8dc0f2eb65f9a81168793d1329ad`  
		Last Modified: Tue, 20 May 2025 00:26:35 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759a61a64bfcb5b28ea23d7d3f5b198a4d5b17d316346c6ac44cbc3703f7c996`  
		Last Modified: Tue, 20 May 2025 01:08:19 GMT  
		Size: 1.0 MB (1014223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9cb484bc0ce3a6ee6ac5c187198b9a47fbc08ad102e9ddfaaa8b146eb89c04`  
		Last Modified: Tue, 20 May 2025 01:08:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67f5617526a66ed84849f26bae6f8ec9367b12f8300fc19bacc7731aba970ae`  
		Last Modified: Tue, 20 May 2025 01:08:19 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62eaf6aceeedfbad6421bef7ae496e3c7f559fb753467c56b2492a00c2c4a54d`  
		Last Modified: Tue, 20 May 2025 01:08:24 GMT  
		Size: 19.3 MB (19275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13dcaf6ab704441a20cd1a1fc29ea76e8d690b3c85f44e6953a5556a738d3a9`  
		Last Modified: Tue, 20 May 2025 01:08:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:eda5bd10d1b757da84458d7712795f390d452f9040c71559bedb8e46ba509718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3965a48d2cd13eac8de489e4310f76f18c8b55d0edd6c27fc3a9f65f72d7c0`

```dockerfile
```

-	Layers:
	-	`sha256:e70ec430e9026ecc9a0c33c370f17f475f8730ca23c8f5181f89ab079fdee17d`  
		Last Modified: Tue, 20 May 2025 02:07:55 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

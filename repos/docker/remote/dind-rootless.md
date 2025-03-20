## `docker:dind-rootless`

```console
$ docker pull docker@sha256:a4de7e3355a5b9a09ac4c8288b9adf2c7e56d70d09483b1da17b5b09e7987025
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:1600a6dc72aeb81773819efb983225a91ef352da9bc5473aa80f5750aa8c292f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159763419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4036b4c226be938fa1d877e13f2839f89625affef5f0a233036a7cef0f3c38d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Mar 2025 22:58:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
ENV DOCKER_VERSION=28.0.2
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Mar 2025 22:58:31 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Mar 2025 22:58:31 GMT
CMD ["sh"]
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Mar 2025 22:58:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Mar 2025 22:58:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Mar 2025 22:58:31 GMT
CMD []
# Wed, 19 Mar 2025 22:58:31 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 19 Mar 2025 22:58:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ad2adead51c9244a4f7f5f371b8b26e26af8463b7f36bb03074a58fc14acd9`  
		Last Modified: Thu, 20 Mar 2025 17:43:04 GMT  
		Size: 8.1 MB (8062999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0f7aab4e132bd2b51770f057ac5ae1da7ccb362cb1c852d443fb58fc8dbb12`  
		Last Modified: Thu, 20 Mar 2025 17:43:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c38f784d71fb40e27f26144faf80d7c7f56ba3fe9fd8c980eda8614942ec9c`  
		Last Modified: Thu, 20 Mar 2025 17:43:04 GMT  
		Size: 19.5 MB (19529745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188479850f849ab4c479f85d0f465f914cf7afab1e0b55c6641a26bbba33bb76`  
		Last Modified: Thu, 20 Mar 2025 17:43:04 GMT  
		Size: 21.8 MB (21848940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0c76f1d3fadbad10843cf51a73fc5f2e96299a9a7170e5e8ace164e0e75a1c`  
		Last Modified: Thu, 20 Mar 2025 17:43:05 GMT  
		Size: 21.4 MB (21357077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416ec1224805c0293b7eddf8b3274f6bfb29cea1beb8c53548d8774395b18c3e`  
		Last Modified: Thu, 20 Mar 2025 17:43:05 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795298ab78ddc8ef23dfb85a0942df87594e19a3b54a465847eca38afeabb760`  
		Last Modified: Thu, 20 Mar 2025 17:43:05 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4b065260fd74d440330ef1b5f67ce2d5da4a7d9ac5623919772a16771ee82`  
		Last Modified: Thu, 20 Mar 2025 17:43:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7bd15afdc0a5796b49dc2e5bfb23076a8592fcd6dd525a7f8139da3fed54ed`  
		Last Modified: Thu, 20 Mar 2025 17:52:55 GMT  
		Size: 6.7 MB (6733051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83176913950647401370c4bcb5c907ec17d8432df9888eca56ce5ed1d7ed4584`  
		Last Modified: Thu, 20 Mar 2025 17:52:55 GMT  
		Size: 90.3 KB (90322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d06a8a04cdf6ee51f53fa695e5637063fbc65d84d56ceba45e21983580bbdd`  
		Last Modified: Thu, 20 Mar 2025 17:52:55 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e74ace81ad22e64fcccbe32e89f49c4cf59f831653321d636399c610e5038ed`  
		Last Modified: Thu, 20 Mar 2025 17:52:57 GMT  
		Size: 60.3 MB (60331905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acd4ffe0bcbce0d3c233c184943580980470786ed5323d2e7710c9e4dc6cac2`  
		Last Modified: Thu, 20 Mar 2025 17:52:56 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e39e22855a0e9f6d6a16f1f7591602b83a5f0e7be1f32aa57523c36f8a9c50`  
		Last Modified: Thu, 20 Mar 2025 17:52:56 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9caacd917b0730553161f256ae0f14eef42a4227a821417230e29343012ae59`  
		Last Modified: Thu, 20 Mar 2025 17:55:02 GMT  
		Size: 986.6 KB (986572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabe3bf25d5e6fa7b5e7939a5385d420ce4c9653a6865272d0be2aa8a2139631`  
		Last Modified: Thu, 20 Mar 2025 17:55:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645309b2533c4c20ef8d2be3b4eb5adcec7e938628015d5be57b3f60470c1149`  
		Last Modified: Thu, 20 Mar 2025 17:55:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf9a192605121e4d896a4b95906c07277a2fadbc5a95130344b34bf977b997`  
		Last Modified: Thu, 20 Mar 2025 17:55:05 GMT  
		Size: 17.2 MB (17171163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd8f6cfa4dfcec2275df430797f2a6b1ec6d50e2fd84fdfaf46cefe0dba91b5`  
		Last Modified: Thu, 20 Mar 2025 17:55:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bb881f7a4b6f39e50267759e69f4752d6cb666569acc876b0c3e97fc5531d698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a15dcabbbc38023e4a920bd7149e15e1b3497e580e3cb90b7a29eba23ebbd59`

```dockerfile
```

-	Layers:
	-	`sha256:bd12de0ba81464627234fbc349f4d83ecde651bba8fda2ed2f351d244dc27ea7`  
		Last Modified: Thu, 20 Mar 2025 17:55:01 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4cfc0bf12fc01f6bbc2bdfb5259c97de83b1df14c7009c1c3d92c6697d25bbcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153232364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171a162c99d4e048f5051beecec89524baf8c0390429a2888d9036d504c4fc83`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Mar 2025 22:58:31 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
ENV DOCKER_VERSION=28.0.2
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-x86_64'; 			sha256='94a416c6f2836a0a1ba5eb3feb00f2e700a9d98311f062c4c61494ccbf3cd457'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv6'; 			sha256='f581de955d332f10323ff98dc3faf4b13f7ba9c5372dac3b389ad28f8dc85b1e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-armv7'; 			sha256='9080c489047880546b0269b74d0750d94ef604fe4a3c11b2e5dfad436b1e4fa6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-aarch64'; 			sha256='cd1ef5eda1119edb9314c0224bac97cee14a9c31909a0f7aa0ddfe266e08adaa'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-ppc64le'; 			sha256='ec2c9e4083ce1bd6b3c30ddd30002bc5d9c83b4749a20e853ea73e1e14ad7b9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-riscv64'; 			sha256='5d3bf73eb9fa9f7576ba8f2bc2f231b684b453b747dc55b6cadde7566c34f6dc'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-linux-s390x'; 			sha256='558955aebe0f5965bd5e9449415a746905a7f4c58f8642946e576becf1745376'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Mar 2025 22:58:31 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Mar 2025 22:58:31 GMT
CMD ["sh"]
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Mar 2025 22:58:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Mar 2025 22:58:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Mar 2025 22:58:31 GMT
CMD []
# Wed, 19 Mar 2025 22:58:31 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 19 Mar 2025 22:58:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 19 Mar 2025 22:58:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b0177dca1b4e4c55a4ddbc4f30e34b34aa72ab96f1b8e0f32c0a60d7557338`  
		Last Modified: Thu, 20 Mar 2025 17:42:33 GMT  
		Size: 8.1 MB (8076592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879e45996fc250d1fa3967cc170b482e51205ab64d44fec9094e8d6340d08dce`  
		Last Modified: Thu, 20 Mar 2025 17:42:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f632584969e64bfa7b77277c3f75e5252b498c152271958f22fbb9b1dfc3ded3`  
		Last Modified: Thu, 20 Mar 2025 17:42:34 GMT  
		Size: 18.4 MB (18446281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87d0d56833a43d3510ba32a304e6675d9e4b2026203c5dd13d2a57a62f5e491`  
		Last Modified: Thu, 20 Mar 2025 17:42:34 GMT  
		Size: 20.1 MB (20061169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1958efd114b67f0eb40d6604e3873f0cfebd5f3a9b6b2b6f23a65902c8d4ed1e`  
		Last Modified: Thu, 20 Mar 2025 17:42:35 GMT  
		Size: 19.6 MB (19581867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dcb05dc006c81521b71e12f12bbf0d1379881e35d75e227ed4927ce29b7a9c`  
		Last Modified: Thu, 20 Mar 2025 17:42:34 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b460c36becec2cf6f1084e816f46bfd9940df8df09a4a6e7aaa71e607ec501`  
		Last Modified: Thu, 20 Mar 2025 17:42:35 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a3d915be4f748dba801cb4ceab89910010fbd579184240ff0f6a0ab4ba135f`  
		Last Modified: Thu, 20 Mar 2025 17:42:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73886a0179bdec95a9902597394cac86ea081c980ab0806bfb86ee892a7e8e77`  
		Last Modified: Thu, 20 Mar 2025 17:52:11 GMT  
		Size: 7.0 MB (6978860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ed0fa9efd99d06a0b4dc1e3d79833bc31f3b3125b7a5837f66866d99929d8d`  
		Last Modified: Thu, 20 Mar 2025 17:52:11 GMT  
		Size: 99.4 KB (99381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d444512896ccd3d0c5531f7da8c842617c9c0e3022e8f6ac615f4bd138e19fa8`  
		Last Modified: Thu, 20 Mar 2025 17:52:11 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f794f074c9455a04468cb9e202be04bf55d2b2a829e325d2b1205e1da1a8d8ea`  
		Last Modified: Thu, 20 Mar 2025 17:52:13 GMT  
		Size: 55.7 MB (55689449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64e5dc496fe1afd65582cf11e3e0b1895a8a3c94b70ccdbe9278d77088f3d9d`  
		Last Modified: Thu, 20 Mar 2025 17:52:12 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83610288459160413bfa1969199b8e234d872b304f8839cc845a96522cbdd3e8`  
		Last Modified: Thu, 20 Mar 2025 17:52:12 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9795eb300b4df43497627062f89a9c2fb874901d24ff719c0b7770abb2a8042`  
		Last Modified: Thu, 20 Mar 2025 17:56:04 GMT  
		Size: 1.0 MB (1014201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e0e1a0759249005c9c3963ccb19b6076e4a28a2f2732788d2c8f52eb7cdd3`  
		Last Modified: Thu, 20 Mar 2025 17:56:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb03373de2005d013442bd97c000c292eadb918580b066d862a20460ecf3e21`  
		Last Modified: Thu, 20 Mar 2025 17:56:04 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ee3ed1b31941646f0161042c5e2aff849300f25ca0e8794741e792b3e126b4`  
		Last Modified: Thu, 20 Mar 2025 17:56:08 GMT  
		Size: 19.3 MB (19282135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb69c982afaf8e6009df3ce5c8c105eaca1242d415245dc3cc1bf3e1c87849b`  
		Last Modified: Thu, 20 Mar 2025 17:56:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:8e07cf83beeb07b3ad93cc110919d6ac4bbfcac03b0bba4589558b07f388caee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7159133a5c3b116c8295e2fd530dffd9ef2b80618d7fb9755a8aecbd58784ff5`

```dockerfile
```

-	Layers:
	-	`sha256:3c9a26f44f5d9643748ec5fd865b27b884dfaafa4c0456cc0c4ba704a31fd163`  
		Last Modified: Thu, 20 Mar 2025 17:56:03 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json

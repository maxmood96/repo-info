## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:371962f4344295a1eb185f1c9e62064bf4503a7beb8c6e73be3405500041784b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:7e32ba65198ce220388cb6c45cfac60966e6dee5c7a7207510ce786648e1ca75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157585482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5bb5dad84091a1a6695f967bc7974bdf20759600535244123f5d8108736cdb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 26 Jun 2026 19:14:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 26 Jun 2026 19:14:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 26 Jun 2026 19:14:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 26 Jun 2026 19:14:50 GMT
ENV DOCKER_VERSION=29.6.1
# Fri, 26 Jun 2026 19:14:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 26 Jun 2026 19:14:50 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 26 Jun 2026 19:14:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 26 Jun 2026 19:14:51 GMT
ENV DOCKER_COMPOSE_VERSION=5.2.0
# Fri, 26 Jun 2026 19:14:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-x86_64'; 			sha256='018f9612ecabc5f2d7aaa53d6f5f44453a87611e2d72c8ef84d7b1eca070e719'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-armv6'; 			sha256='ce15dafabdceb12b0e136fcf71e8fdd3e7f35407da9ab2591db4097fd56327bc'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-armv7'; 			sha256='e202edcce184f5e17219e2defa8263580729c7e939133f8d703daecd461cb37e'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-aarch64'; 			sha256='739de570a0adf5eab12830db980f549fb5f44ad6b266e1e43e20f6f9df7cbcca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-ppc64le'; 			sha256='0dfd397c75da17215b8dc9382878807fdbaea0b5cf6084fb96ac656ea0940c38'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-riscv64'; 			sha256='9aa503f95e94381ffbc34a26a7dd31dca4e96ba795daa1ed26735572400a17ce'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-s390x'; 			sha256='aedc25e71397e16a2e7d3cf20929c5095909e7f75686875087c65c2279de847c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 26 Jun 2026 19:14:52 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 26 Jun 2026 19:14:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jun 2026 19:14:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 26 Jun 2026 19:14:52 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 26 Jun 2026 19:14:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Jun 2026 19:14:52 GMT
CMD ["sh"]
# Fri, 26 Jun 2026 20:09:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 26 Jun 2026 20:09:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 26 Jun 2026 20:09:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 26 Jun 2026 20:09:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 26 Jun 2026 20:09:57 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 26 Jun 2026 20:09:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 26 Jun 2026 20:09:57 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jun 2026 20:09:57 GMT
VOLUME [/var/lib/docker]
# Fri, 26 Jun 2026 20:09:57 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 26 Jun 2026 20:09:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 26 Jun 2026 20:09:57 GMT
CMD []
# Fri, 26 Jun 2026 21:10:07 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 26 Jun 2026 21:10:07 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 26 Jun 2026 21:10:07 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 26 Jun 2026 21:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.6.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.6.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Fri, 26 Jun 2026 21:10:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 26 Jun 2026 21:10:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 26 Jun 2026 21:10:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e05145bca39aab219a3a9990d94a89c42419c02fd5f40925d6bb145592eb8b`  
		Last Modified: Fri, 26 Jun 2026 19:14:59 GMT  
		Size: 8.2 MB (8170607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1daa427cd22d6c88a7f930a9fb2a2abfeb63d0e821a44851211cf9fe009a753`  
		Last Modified: Fri, 26 Jun 2026 19:14:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df37b5275370f8d84f45dd287b81d27e520c0c35b98fa117e809140073d820a`  
		Last Modified: Fri, 26 Jun 2026 19:14:59 GMT  
		Size: 19.4 MB (19439641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4cc4ef829622acfa684395b5072abf0b03ab1b1c089c87947212e7cc95671a`  
		Last Modified: Fri, 26 Jun 2026 19:14:59 GMT  
		Size: 23.0 MB (23036812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b31d5b558403aa2691bf063fe01fc988cbc83ae34c01f01f06312de0b5a2070`  
		Last Modified: Fri, 26 Jun 2026 19:15:00 GMT  
		Size: 11.3 MB (11295071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562fff92cf4d1e022ed5d3e64987d66b3dd94c5260ba0066be7f5aa9811860df`  
		Last Modified: Fri, 26 Jun 2026 19:15:00 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8632edb1fb7583e908cde08fb81f3d38eacd36685638d89f813493de7aa52a`  
		Last Modified: Fri, 26 Jun 2026 19:15:01 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1109ac0b7008cda851bdc442b18d60b59ba4a78fd5abf65b1029b7b644ed384f`  
		Last Modified: Fri, 26 Jun 2026 19:15:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f7d3688ed3253f01a35ac9ee319f7e2f8e00280b54b9fb0e8317425077cc3f`  
		Last Modified: Fri, 26 Jun 2026 20:10:07 GMT  
		Size: 7.0 MB (6965231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd57b1c0c61542f33706b9a217d7b40cf6eb469d6bbaacd592469a9f25d878d`  
		Last Modified: Fri, 26 Jun 2026 20:10:07 GMT  
		Size: 91.3 KB (91334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23011a9e0c5e9ba4ee856dbcf7c1d1926164009df6881ce03a59b65c1b9b6b0`  
		Last Modified: Fri, 26 Jun 2026 20:10:07 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34defd136645fb282a3ec960a7f5e19a39dda5397932292252eddf6e931dd56`  
		Last Modified: Fri, 26 Jun 2026 20:10:09 GMT  
		Size: 69.2 MB (69156332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d9f738aebeb26d0a87e7aa43f5e33eb6d26bcb05c5c1d726318c3c6d70b019`  
		Last Modified: Fri, 26 Jun 2026 20:10:08 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc014cc1384a4e34fd5f897abd97bf89e74dceb24ba98a1a236890061c23a4a8`  
		Last Modified: Fri, 26 Jun 2026 20:10:09 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fedeb688a134dfd96a614fb4f858bf76864d5f7a5d76fdabc5548958d7e4e4f`  
		Last Modified: Fri, 26 Jun 2026 21:10:13 GMT  
		Size: 3.5 MB (3471260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c81ea3ee5cc4fdc815bbecc7e83636c9d253555108c80a3b6b3ac4637089dc`  
		Last Modified: Fri, 26 Jun 2026 21:10:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b435a74e2da7f7cbe66f68a960273748e56884de827c9968907f52112d808d4`  
		Last Modified: Fri, 26 Jun 2026 21:10:13 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd84e92bf71e4ca3fda92193af8716b7bc7a27df2eaf1d0b2e4bd572a60880be`  
		Last Modified: Fri, 26 Jun 2026 21:10:14 GMT  
		Size: 12.1 MB (12103309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cb2266b88aba0063d5fdb6bf7d1a456e320bc4ae60522962bdee59fb7845e4`  
		Last Modified: Fri, 26 Jun 2026 21:10:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:60a04bf338a3905afe926941d1dfa69e1ee723f164f9be090c10270c9e21bbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d327b13b2f4387990a6a1be787939319382ebeced88fcc57fab642794dd96b`

```dockerfile
```

-	Layers:
	-	`sha256:8943a2760cc456fd13256361ef31a0708d98769920a4b615d7c275fcb8f94adb`  
		Last Modified: Fri, 26 Jun 2026 21:10:13 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5b12ac3fac58ba82cc21a388bbbd7c4e6ab734e0fd937b3083c166468bd310e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (146037933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1ac82d40c6358354dff44028a97431acf35e13460ff66476fab4a66d76cd04`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 26 Jun 2026 19:14:54 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 26 Jun 2026 19:14:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 26 Jun 2026 19:14:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 26 Jun 2026 19:14:57 GMT
ENV DOCKER_VERSION=29.6.1
# Fri, 26 Jun 2026 19:14:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 26 Jun 2026 19:14:57 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 26 Jun 2026 19:14:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 26 Jun 2026 19:14:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.2.0
# Fri, 26 Jun 2026 19:14:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-x86_64'; 			sha256='018f9612ecabc5f2d7aaa53d6f5f44453a87611e2d72c8ef84d7b1eca070e719'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-armv6'; 			sha256='ce15dafabdceb12b0e136fcf71e8fdd3e7f35407da9ab2591db4097fd56327bc'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-armv7'; 			sha256='e202edcce184f5e17219e2defa8263580729c7e939133f8d703daecd461cb37e'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-aarch64'; 			sha256='739de570a0adf5eab12830db980f549fb5f44ad6b266e1e43e20f6f9df7cbcca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-ppc64le'; 			sha256='0dfd397c75da17215b8dc9382878807fdbaea0b5cf6084fb96ac656ea0940c38'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-riscv64'; 			sha256='9aa503f95e94381ffbc34a26a7dd31dca4e96ba795daa1ed26735572400a17ce'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.2.0/docker-compose-linux-s390x'; 			sha256='aedc25e71397e16a2e7d3cf20929c5095909e7f75686875087c65c2279de847c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 26 Jun 2026 19:14:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 26 Jun 2026 19:14:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jun 2026 19:14:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 26 Jun 2026 19:14:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 26 Jun 2026 19:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Jun 2026 19:14:59 GMT
CMD ["sh"]
# Fri, 26 Jun 2026 20:09:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 26 Jun 2026 20:09:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 26 Jun 2026 20:09:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 26 Jun 2026 20:09:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 26 Jun 2026 20:09:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 26 Jun 2026 20:09:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 26 Jun 2026 20:09:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jun 2026 20:09:42 GMT
VOLUME [/var/lib/docker]
# Fri, 26 Jun 2026 20:09:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 26 Jun 2026 20:09:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 26 Jun 2026 20:09:42 GMT
CMD []
# Fri, 26 Jun 2026 21:10:00 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 26 Jun 2026 21:10:00 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 26 Jun 2026 21:10:00 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 26 Jun 2026 21:10:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.6.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.6.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Fri, 26 Jun 2026 21:10:01 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 26 Jun 2026 21:10:01 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 26 Jun 2026 21:10:01 GMT
USER rootless
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f574f2d77674c37cadd8c9f4bc57c1afd5ff014d7f2577d093ffdcba7723fddc`  
		Last Modified: Fri, 26 Jun 2026 19:15:05 GMT  
		Size: 8.2 MB (8231667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fa458364e4c795f7359216c331c4efda1fa3f91c672c536c3bd342961a1748`  
		Last Modified: Fri, 26 Jun 2026 19:15:05 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4d23d78ffee329b8baf1a8dbfa45aee440df6eb8a8fa7ba50cef2f6fd57ec8`  
		Last Modified: Fri, 26 Jun 2026 19:15:06 GMT  
		Size: 17.9 MB (17889549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684c8069362067b22560c772e5e5556c0da34e15d2e96f4e83fc2fa246d1c05d`  
		Last Modified: Fri, 26 Jun 2026 19:15:06 GMT  
		Size: 20.9 MB (20856356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37879908a64ad363caa4431f41417979cbecf7d292b659597d4f3025ee27c0ef`  
		Last Modified: Fri, 26 Jun 2026 19:15:07 GMT  
		Size: 10.3 MB (10267179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8027c981d0cee23366d81ff6f6e7a3561faa6cf3d96b11fa16b9518f3a1de1`  
		Last Modified: Fri, 26 Jun 2026 19:15:07 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ffa6867421af586d860ad2af33942841d0a938ce3d92318f542fa77776a096`  
		Last Modified: Fri, 26 Jun 2026 19:15:07 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eda3b5762f87b9718f7ae11079cde3e15ff1e1b6cb2d2f1d59c5d326c370d04`  
		Last Modified: Fri, 26 Jun 2026 19:15:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7b7f7c3f4d6179fee0cd18c832b93bb7d412938076e09926798c894b1e870`  
		Last Modified: Fri, 26 Jun 2026 20:09:52 GMT  
		Size: 7.2 MB (7240483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fe0a609f7f49f5ccf70c6712472dc07c629e0114d6103f5102b4edec75a966`  
		Last Modified: Fri, 26 Jun 2026 20:09:52 GMT  
		Size: 100.0 KB (99950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caa2612640a67bffdba6b2de15bee17e1f3554fab495307c2eb31c722920020`  
		Last Modified: Fri, 26 Jun 2026 20:09:52 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd80cad6104c5f657e5582ea0c09f7f8c62bcde68bb1e7964c9c21ec0d8bfeb`  
		Last Modified: Fri, 26 Jun 2026 20:09:54 GMT  
		Size: 62.6 MB (62574293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75843d6b9c9d05f0c0cd271f3c838fe43b9d98abda3603a5fdd6d567d686840`  
		Last Modified: Fri, 26 Jun 2026 20:09:53 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571f5b27af7ee8767453fb806ee10936f9c71f41b92b2fb9df9c64cfdf7e9e68`  
		Last Modified: Fri, 26 Jun 2026 20:09:53 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d78dc73bf15721c5e18393c9315ad0fd1cde93655d5dd1b22dd79c6480337c`  
		Last Modified: Fri, 26 Jun 2026 21:10:06 GMT  
		Size: 3.4 MB (3448838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac68c7e2a1412e9139e86b2cd3d47f65bb122c046cd72373b4cdde640c6bde4`  
		Last Modified: Fri, 26 Jun 2026 21:10:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940e296424552351728af90be04f9bc7331768121feb9a16968a8e5012c680ef`  
		Last Modified: Fri, 26 Jun 2026 21:10:06 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a434de8a1c5ad5bc40e0b8b54d22e2b6c5dbb2308538a24c962e0f17cfa77`  
		Last Modified: Fri, 26 Jun 2026 21:10:06 GMT  
		Size: 11.2 MB (11237083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69764499e5f4c737e1e3df06b6449dd1f094d0577a91a48156e9dabb2877ebd1`  
		Last Modified: Fri, 26 Jun 2026 21:10:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:36d245ff3b999721594d488e19b3e5980a3b910da4484947b3fe77e303ed2175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2bb59055922667754d5649c5aba19c2b29b34bd435ea8db93ff1848d8dca10`

```dockerfile
```

-	Layers:
	-	`sha256:bf33c7b8b311be23d40353d86fd6af5aaf77cefa633818a4fe82eb77c873ccae`  
		Last Modified: Fri, 26 Jun 2026 21:10:06 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

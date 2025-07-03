## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:b44749d9b6aba4f5f80bb759bb6ea83e62a1f2c8c0897ad059c5eeafb8d43c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:db4c04bc4465b0434d622bf882950ce45685a378b0ee811e9e1b1219ba6e9436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168515988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21511f843dd54e89f5b101840d8b53c72e1c5ddcd62a5f854485baaa6600fa9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eea5ac8f4a2433da8fb7f24a2320140ce3ecde3e901f4f1c87ad95056697ca`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 8.2 MB (8207455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052a5b41716ab918ba852b4c5796870ac3421207dd6f643e1b12aad154b9bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45167fa5e6b285faf8bb0e4c7f95647f39e6eedf04ed73a2782835781ae3ce68`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 20.5 MB (20460130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1113da369f53ed78c003a950ea8b8c440dbd70215cb1cceec72d83b25033bd`  
		Last Modified: Thu, 03 Jul 2025 17:22:32 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e0971b860e8aea13c584dfef29a126a6cf0c72e59f7a3e2b5b81f5eed16027`  
		Last Modified: Thu, 03 Jul 2025 17:22:31 GMT  
		Size: 21.3 MB (21277575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a12acfa4778cb7e9eef3bd175c3e4ff41c1dfebf862d9bd865721a18c75650`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b98f3328a38b6dd7ae62f1fad6b9f634d0ccf217b778a69567f3f12f8be9b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a610d0791b96d4f44016de2275f8c8d37023997dcdacfda355c1a4f6689371b`  
		Last Modified: Thu, 03 Jul 2025 17:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365751159013f2736109815bcf7ce6f16405a16442fe174c70b4de2b456ff000`  
		Last Modified: Thu, 03 Jul 2025 18:08:08 GMT  
		Size: 9.5 MB (9506705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79eda5ddd00d8f7318beb49213bca1058e91b36d987bdd0ddd6c84c32911ee`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 90.5 KB (90498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df3a8fd9c7c036d08c367ce8ce5017605d204fee4160adcdfb365d2ba3ebbf`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64a1aeb2cbe7da3322a3cb1e35be02786316351836ee864981b72887fedcf8`  
		Last Modified: Thu, 03 Jul 2025 18:08:24 GMT  
		Size: 62.5 MB (62518784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de6eae7a7783ce21dbf4bbdb7152eac13899c5ddc472b28b3d56b553d2a99a3`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bad4ccc74e83be6126960480ee79fdba8542048d94c20703c5c77117c4dc35`  
		Last Modified: Thu, 03 Jul 2025 18:08:06 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b828347c2a041335957c90cb55b04a323af16f817d2ea2aaa04c38fd9e0a915b`  
		Last Modified: Thu, 03 Jul 2025 18:11:38 GMT  
		Size: 3.4 MB (3398182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9015f88f20407c97d95eec2557adffa39da70fe898e9ef54cc056e91f839250`  
		Last Modified: Thu, 03 Jul 2025 18:11:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fe64c2be9d18d459bedfb0eaae711ac691aae9da049d2259fa61694eebd252`  
		Last Modified: Thu, 03 Jul 2025 18:11:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6974db92eb03859ebac691c35b3b8e4bda756d27667351ec08ad27e3cebb426`  
		Last Modified: Thu, 03 Jul 2025 18:11:40 GMT  
		Size: 17.6 MB (17586158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69244f3e5323c1ad99d83700a10a30cbf3c9b59bd1d6deeb518016c91586411e`  
		Last Modified: Thu, 03 Jul 2025 18:11:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a0cc335b94ca365a19094d5303c10b30b5b1662788b30690d3a98d802427f0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d20f1d9888c19a6d1afdef8729e43aec20f90f322855e9b5c650247836ff0c`

```dockerfile
```

-	Layers:
	-	`sha256:e2532b0be60f5ccad634be0410f2b01c3922c3e42bfc227d2e206c65d2636109`  
		Last Modified: Thu, 03 Jul 2025 20:07:54 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5cedcdbd876edad79f8f62fec3ae650536577aa61a559acaa654dc6f6af631b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159976175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c81ca73fc3e1d219a425a73736a34d915776a8259e79eedd00597f482971cc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD ["sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 03 Jul 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Jul 2025 05:04:15 GMT
CMD []
# Thu, 03 Jul 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 03 Jul 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Jul 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad07db5a1bbc41e58d5fde672f099fcec891ace53c8c887aee9dcfdc3c2cf13`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 8.2 MB (8228992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b0f69733af9240b4179ae03051714da71eff6464a72eaf82690a04248080`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbcd8ee831b1e8253740e284128af89bf82b609c3cbc3836edd5ee68ac2467`  
		Last Modified: Thu, 03 Jul 2025 17:28:46 GMT  
		Size: 19.3 MB (19267881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0289ff13c6e37a04d080ac18c6ef21aa6da7178815de7271e399beaa8650d`  
		Last Modified: Thu, 03 Jul 2025 17:28:47 GMT  
		Size: 19.8 MB (19819444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b84d973a05e30434f2e8034d5e4a5f45fa514c54e35fb8d9b869eddb2708471`  
		Last Modified: Thu, 03 Jul 2025 17:28:52 GMT  
		Size: 19.5 MB (19512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6abcf0c03212066096d056540a520a747ce65181b410f405615260e71f759a`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0c1bc8ed7290ffdc1fe8fcb5a607605c0be6dee8c019652f95d77571c57ec2`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a3331055b8b82e54b996a671270b0a5eb1e7c2bb43e0dacea7c4e7b90e633`  
		Last Modified: Thu, 03 Jul 2025 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952203b1c7a41a0c76f1dbea125ddaf54ce68576a4768a537dda36e1f59b55c3`  
		Last Modified: Thu, 03 Jul 2025 18:07:51 GMT  
		Size: 10.0 MB (10034350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab36c59cc6a2dbe7a12df8a0839b396c37da3b66ed9879bdb445f235671c9`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 99.6 KB (99643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bdf8ef2f3347568fdf3a63df90f459ccee3c8e2d590c2f39e6de5dd02773a`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745743961c171379ae2d21822931c1ac6c64f29c2103d0b3f08da2da68cefda0`  
		Last Modified: Thu, 03 Jul 2025 18:08:00 GMT  
		Size: 57.5 MB (57460631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29030a0bed48b13d788519c9e663ae1d99cc2fdd9f6275b8c1994a9e169c76`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b05490c912681e178d29a43ba96b6d101c051f10661a7c4f2c38ed65e463f9b`  
		Last Modified: Thu, 03 Jul 2025 18:07:49 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055439fa6d8fcc51af0c10bf7bc294b0e1f51845f1fdf975c6f2ed005a72dd7`  
		Last Modified: Thu, 03 Jul 2025 18:22:09 GMT  
		Size: 3.4 MB (3389671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5a4b35eded985f79fbbe8910bab2457acf21a3a5174dc98c50b5a52d6ae94c`  
		Last Modified: Thu, 03 Jul 2025 18:22:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a53aeca772b1453a3107bc47c8fa4c0a699b795f5bb46ce8147903629091105`  
		Last Modified: Thu, 03 Jul 2025 18:22:08 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae30160e013cd77a67fb1c70bca1161363b6d03b329bdbacdb070411f5fab194`  
		Last Modified: Thu, 03 Jul 2025 18:22:10 GMT  
		Size: 18.0 MB (18017309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156b018b4075be77289b3748988b7f34a0e22844508c688dcb3d3fbf47cba9c5`  
		Last Modified: Thu, 03 Jul 2025 18:22:08 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f92dbdaa152a7b0b5985bc9fb607ae59b1f53293d7e03ed0a763bfdb11d65c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e0049363c6bc42c7778de09c867a855ecc9d304eed6f5197c9c0be01a92207`

```dockerfile
```

-	Layers:
	-	`sha256:ddb6058b675b6f844f3eeb5728ee724318dd9b2b36a6a2ac8c90f51f2a3f80a3`  
		Last Modified: Thu, 03 Jul 2025 20:07:57 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

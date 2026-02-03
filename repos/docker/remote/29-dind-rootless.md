## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:68bb0d88ed4134f6cc41f04c62e5e49762051b16f628abf84db6f7c33994885c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:567ead5a15f1f97b9878eede0250d242c0ef27a19c0dd685d70c1c59e21d750c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164603487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e52a73bd06c9759bd4433c27b69afd58457bdb3174e0153ecf3089eea25736`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
# Tue, 03 Feb 2026 18:56:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 03 Feb 2026 18:56:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 03 Feb 2026 18:56:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 03 Feb 2026 18:56:44 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ae3e167984ddda59e327294c6376b950eea2c3ef31d27360612eac1daa1f0a`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 3.4 MB (3419941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d922f02e9320e8d0119111798e4061c241770bb012211f450efe2d517fd1a42a`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687d1e84b0ee14d3c1995e61b0e4a68d506dd136ef95f02c8e2b6faaf863a33`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfdc02c4d88b47fb1008ea5191d51a35b34fca85278d2030e245268126bf6c8`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 17.4 MB (17375862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077f22d66325a95178fd420b08832727efb00c81b7c88dd48a131ccb5b1ce2d0`  
		Last Modified: Tue, 03 Feb 2026 18:56:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0d5c44c6470979f0c582d86f55d66e742e639e3a8fdc0a404c02021d4f43d416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e137c0f7f1699722fc735873de3ba73dd4cae21481ee991407f271300a01252`

```dockerfile
```

-	Layers:
	-	`sha256:ae18371d1afbd9ae2b2e2a148ace11a55c228a20017f500977180dec98bd30d8`  
		Last Modified: Tue, 03 Feb 2026 18:56:49 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c68e67b2934792c04cb7f598418b51467087009fcb45ca095e2b0e350705d699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154359925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b76823faed7a9fec13c67806e9f797ce9b03718d27e5e068ad293efc75410c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
# Tue, 03 Feb 2026 18:55:45 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 03 Feb 2026 18:55:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 03 Feb 2026 18:55:45 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 03 Feb 2026 18:55:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3efad4ea039a0085ac85140fdaff7b0901f77d844a3ced398908bed50280d3`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 3.4 MB (3394383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad831014bf8990f5582f5d3e6722e27cfbba3529f3c04cfe9c6a949d88ac099d`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fdeaa64fd5c21fb8b772c2d90c06e6775a9a4bb2843aced9f1875939c73f16`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd2325131d24f7831871c339c38827915943cb61cb8728e71b867ad3ebd747e`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 17.7 MB (17710536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29101bcbdf9cfd2edf02a50ce900b29e142538dd886a8ce77c5a95e1b429560e`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c8832a8a4baba19861161896908a1fba0f16c66b34289e1d7587c4f6f4a2945d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3023e84e94ad559ac9f3b408469b4b362197ad68436d62ad001a7a64cb14b81c`

```dockerfile
```

-	Layers:
	-	`sha256:5b681b0886068572453781d5d67943bb963e404233a24ccd9b820c068524c523`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

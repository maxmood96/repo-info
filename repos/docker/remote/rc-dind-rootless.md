## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:d3f9de1204c59d343bde2d4dc1ce3a52dd9d94887a238971250aea84a51980a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:b8d96db3fdc57f83404b60eee8afdbf2f5f626bd20f3573d5bd235c07c08b411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163487663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfda7c0c2d6c863ed0943e4bed915c0837f83e60ab3e56349eada58c70e82a94`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_VERSION=28.3.0-rc.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Jun 2025 17:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
CMD ["sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Jun 2025 17:04:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 23 Jun 2025 17:04:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
CMD []
# Mon, 23 Jun 2025 17:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 23 Jun 2025 17:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1925cf481675fdf4d9996cf1084cfe0827645739858e6f5573f10662949466`  
		Last Modified: Tue, 24 Jun 2025 19:07:27 GMT  
		Size: 8.2 MB (8207465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a76b1bd17b956e7d8c8189988971813f561c125b669d3bd64a2ccf6f1c88dab`  
		Last Modified: Tue, 24 Jun 2025 19:07:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540deb8497e7b581c5db173a9b6be680a695d2c3a0ece738186c57d44f8a5a81`  
		Last Modified: Tue, 24 Jun 2025 19:07:28 GMT  
		Size: 20.5 MB (20460211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29413dcf2a31e94da7b3bc025bda0d48c6efa1eb3dbdb17390d1f8aaed038f16`  
		Last Modified: Tue, 24 Jun 2025 19:07:28 GMT  
		Size: 21.7 MB (21664165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a1d72ea036fbec8b6b3dd12a3e5f7e4fefd940f1612c7a91d97bc08cfc6a7`  
		Last Modified: Tue, 24 Jun 2025 19:07:27 GMT  
		Size: 21.3 MB (21256111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e846024221b092fc5bb9aeea41c448c3891cbadfb196f52898e1ac6e9168efc0`  
		Last Modified: Tue, 24 Jun 2025 19:07:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70de40294c35d205626f4205dec025466597143dc6a624e9828fccd6eaf5b3d2`  
		Last Modified: Tue, 24 Jun 2025 19:07:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19999cf4f067d0899c5c4007351ce3188bc05105da1b0d2661e25616d9b544b9`  
		Last Modified: Tue, 24 Jun 2025 19:07:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6328dc55576e090fc18da14c6b7a5567cf974ca26ec10350cae7f3c7a96f8ce0`  
		Last Modified: Tue, 24 Jun 2025 20:07:29 GMT  
		Size: 6.9 MB (6905588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9b94a3e5d62507d6275207a1b46f1e551f4d9b7bb3162fd5293ca0c781a81`  
		Last Modified: Tue, 24 Jun 2025 19:40:44 GMT  
		Size: 90.5 KB (90494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc329b9281eca3d93ef3b02cfc3587b76e0205d704f30064be34492e3058b4a8`  
		Last Modified: Tue, 24 Jun 2025 19:29:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926ae698aa43805e1a19ded4fd71ee0b7065361c0aab7c04860ed9a57c835af`  
		Last Modified: Tue, 24 Jun 2025 20:07:33 GMT  
		Size: 62.5 MB (62517855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b157036191bcad093d6fb67b2b6f7463442e0f748e78278813d55bfa03fd2817`  
		Last Modified: Tue, 24 Jun 2025 19:29:10 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09934970e22e5110606edc080594cfff9a5c1a19fae8b6f430896ca25a0585`  
		Last Modified: Tue, 24 Jun 2025 19:29:23 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003cd8bb062eeba5a2d51bd359a11618dd971ee3a4442285fd58423dd4d949c`  
		Last Modified: Tue, 24 Jun 2025 20:08:18 GMT  
		Size: 993.3 KB (993278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d513e1bc4ec3fd7bf4a3ef0a0b4fc455badbc1b52266be802cf8557b59dcd0`  
		Last Modified: Tue, 24 Jun 2025 20:08:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eff6c9eb30700326ee438503afbbae514955ec4a956227667fe51a7974bdfbd`  
		Last Modified: Tue, 24 Jun 2025 20:08:19 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14662cc8e7952426a8988d4c52f12ceb9dbeaa7629a15cdd8a43345f0c0f77c2`  
		Last Modified: Tue, 24 Jun 2025 20:08:21 GMT  
		Size: 17.6 MB (17586161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701f198b00e5ccf44db026a71b0560d05c6ae1e818f686048c307c12745a4768`  
		Last Modified: Tue, 24 Jun 2025 20:08:19 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4ee42d6e821885457ee6259418a89c444ae7dfea10e328789c78d4ac2670be45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8beb81aa4b82719a9f19eead3287aa72da002a84ff5f962400e7459438bc5b`

```dockerfile
```

-	Layers:
	-	`sha256:0bcaa1054ae94f8aed91a64eda0bb41707a44e49fde0b64b5acc3a2b64c462f7`  
		Last Modified: Tue, 24 Jun 2025 23:07:39 GMT  
		Size: 30.2 KB (30204 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d1df2f7ad9a0a2e1e233380f8805b07cef90ce0a212f8464c8512b102f1754d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154690232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f0636bb4602d0a810ea8594d2c2f932f5673da34cf06d401a557f6d1897f50`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_VERSION=28.3.0-rc.2
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 23 Jun 2025 17:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
CMD ["sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
VOLUME [/var/lib/docker]
# Mon, 23 Jun 2025 17:04:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 23 Jun 2025 17:04:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 23 Jun 2025 17:04:23 GMT
CMD []
# Mon, 23 Jun 2025 17:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.3.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.3.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 23 Jun 2025 17:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 23 Jun 2025 17:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c09c12dc876098db6faf127232f099623dbbbd3cf517f8246c8e5a8693e4f0`  
		Last Modified: Tue, 24 Jun 2025 18:27:47 GMT  
		Size: 8.2 MB (8228991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9495848de01826cc1e9f97b4397c76a8e5a50477e0ec7feb5d771d0911cc3918`  
		Last Modified: Tue, 24 Jun 2025 18:27:45 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0db23b3e04de3fbe43904b63e0c79a67ab2f241c3157cdb6dec5a3c31b841e2`  
		Last Modified: Tue, 24 Jun 2025 18:27:47 GMT  
		Size: 19.3 MB (19267887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ed01a514e1533686cb3e3cae9432f4de4bde40085931f2f77f0fb80c5a6a4f`  
		Last Modified: Tue, 24 Jun 2025 18:27:47 GMT  
		Size: 19.8 MB (19819427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548fc0669a9d4e2c9bfced6cd58fe88bc9abc3644b75060415cb0a99788a41eb`  
		Last Modified: Tue, 24 Jun 2025 18:27:48 GMT  
		Size: 19.5 MB (19486378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fa7b216979833ee9c39c6472abdae89ba9a4115918abdbc9f3f92fb24d6d87`  
		Last Modified: Tue, 24 Jun 2025 18:27:46 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6978474840d4220c46a24a5763140e9e4829f80ec717abaeef3a0928bd9bb3c`  
		Last Modified: Tue, 24 Jun 2025 18:27:46 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc95b3a140cf8e4591130d01b47ecdcd8220a9cd5474936ea2266baa7c07d9bf`  
		Last Modified: Tue, 24 Jun 2025 18:27:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a84451cba4ae979e042b5db94350d58dcfd50e658df95dffc371d4cfbff8201`  
		Last Modified: Tue, 24 Jun 2025 20:07:17 GMT  
		Size: 7.1 MB (7141619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88b861ac6445bfc322c1cf1d07e61ba443be8e0b38c821141b6012b46f10e7f`  
		Last Modified: Tue, 24 Jun 2025 20:07:15 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd902e2de33e1bdb577297cc31143cae54708e2adf3569b2fc103b4ae0966e3a`  
		Last Modified: Tue, 24 Jun 2025 20:07:16 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827721c8118c38e0ad2e829ef52345616582085009a7afff4061344f41d725d3`  
		Last Modified: Tue, 24 Jun 2025 20:07:19 GMT  
		Size: 57.5 MB (57460556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576a35b1ca55a82c992cdb9d86953bb215f7648a0c7773f0bbde2d307f44bd4b`  
		Last Modified: Tue, 24 Jun 2025 20:07:15 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a61b717c747827aec4152278f3c71cc1c46cf798e87703c332c646ef9c8fe3`  
		Last Modified: Tue, 24 Jun 2025 20:07:15 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edb1d03b2acc25ade37007b7bf7713a1645da385487fe61f1150f503e37c6f9`  
		Last Modified: Tue, 24 Jun 2025 20:08:08 GMT  
		Size: 1.0 MB (1022999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d421ee2a8a90dbb704b024162686b6479f022f7673749fbcad65141b27dbc3ba`  
		Last Modified: Tue, 24 Jun 2025 20:08:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dae7041e68e0d5258c86c58bc53e194876f40477ac0a823386e2605ee4d33c`  
		Last Modified: Tue, 24 Jun 2025 20:08:08 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb429db85be95fcbff0c6eed7a143630648ea12080801ef4e3af35fabb2bb165`  
		Last Modified: Tue, 24 Jun 2025 20:08:10 GMT  
		Size: 18.0 MB (18017309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9d80d58f1ac44bd84d89fb532130875784cb893bedb75deab00d30e35348d8`  
		Last Modified: Tue, 24 Jun 2025 20:08:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0452c25ea049c34f62ade28f80d73857c4e03c5b17c081cb4d89929945b7ba6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c8b1a920fe54cf5ac975a631566a5d397f13289343f75ccf2622124bf62ac4`

```dockerfile
```

-	Layers:
	-	`sha256:e1eb86bf961b1d336a8aab5b526d0e154bf1037543ea32f4484c11fd6ed2e5b2`  
		Last Modified: Tue, 24 Jun 2025 23:07:42 GMT  
		Size: 30.4 KB (30361 bytes)  
		MIME: application/vnd.in-toto+json

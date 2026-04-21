## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:b195ea3784d101abfe1ac68a47f95bcde74bb7ea4e4e8d277d29bc2661a6ae0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:90ee5b76cb0ac744decd66b40bf8c28137072a5c057ec0ee1929ecdbb221d36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161940861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fabb463ad72abee35979cb5448a0a39f5913b0010186d096e512ca7b033451`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:59:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:59:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:59:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:59:36 GMT
CMD []
# Tue, 21 Apr 2026 00:08:21 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 21 Apr 2026 00:08:21 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 21 Apr 2026 00:08:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 21 Apr 2026 00:08:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 21 Apr 2026 00:08:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 21 Apr 2026 00:08:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 21 Apr 2026 00:08:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53c3ea41339525629cfebd67afd71158e26f974aa002b648300d6b51b0a7f0`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 6.9 MB (6941788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042a8c82cc770b77ff12697783c5d4f58f4a1158c393d8d7bf48c66938dd0364`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e52c67d04087c8634de6b8e00bea30bbbfb9f44b910535df2fcf39d218a76e`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642357ac7fa1a3a23ac6950bf37044c34f3e2baf0302453327f0f0f9c07b625`  
		Last Modified: Mon, 20 Apr 2026 23:59:48 GMT  
		Size: 68.3 MB (68349083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b558d88b0e2089a0084bc1ecf86456f88572debf4e7c409c5b6a9e6a4f1c9`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c3644d4203c234122b18a9c209f1d9346bdf3ae77c865f94bb5d413b0e3ed`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6326f615a955ae1eaedcfd9398e20d690369774c11792fa677315a2ee4edc0eb`  
		Last Modified: Tue, 21 Apr 2026 00:08:29 GMT  
		Size: 3.4 MB (3420140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab423da3008515c1f53f14584a5eec29fd4872007b06158bf377fa09ba064a75`  
		Last Modified: Tue, 21 Apr 2026 00:08:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1226b4652a0375b13cf8982005f49f46b4ea918f3afdeb0631639fbbc3314b7d`  
		Last Modified: Tue, 21 Apr 2026 00:08:29 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7972f6fab882aea0a0a19ba34beda49c3a1fbc3fa74c8f1623babc91d75d88`  
		Last Modified: Tue, 21 Apr 2026 00:08:29 GMT  
		Size: 17.6 MB (17580715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74b8d79d9c7fe010571a301be54bec8ec1b4d7367bd0f213d1156fd0dc66b80`  
		Last Modified: Tue, 21 Apr 2026 00:08:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1df8001a7b67a92a6737daee6dd9872da616bc3739aeaa1373577cb29a570e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670d44ba2e33335446b40d2adf46f25e8eb9622108be15df50e4e534c8d509e`

```dockerfile
```

-	Layers:
	-	`sha256:a576e6e994270734040c0f9b4683c7148fce217d815f34c6ebd4513dfc2fb099`  
		Last Modified: Tue, 21 Apr 2026 00:08:28 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a8b05ad135b3c2aaf1cc2740342e7dced62e131746edba5716795edc6ab5fe0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151777543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f34433de1df012f3564979b68c8ecbea41a0994f744ffc1a0abc1ab348b4895`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:58:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:58:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:58:42 GMT
CMD []
# Tue, 21 Apr 2026 00:08:28 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 21 Apr 2026 00:08:28 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 21 Apr 2026 00:08:28 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 21 Apr 2026 00:08:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 21 Apr 2026 00:08:30 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 21 Apr 2026 00:08:30 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 21 Apr 2026 00:08:30 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b102c50bc0bd848d63594177b3551f950afb81cf23769056498c471acef763a8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 7.2 MB (7219870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffadf95cb7de624b076a0d462fa3480612216001cb1bc1977a7f7c68dd492e`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 101.2 KB (101158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c0362756805190c2877fb2ba65ac0d7335b212c601a891a40a869a2121d2a`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6689be7b2deb380b56446eca8f0ff2610db9e7a9e33ffe8e5ce8255459333b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 61.9 MB (61854105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c32c7cfcb98ead6efe658a6dede3f1c6de4b8f676102e76dbf7519fcb80cd6`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fedc2d525bb8a19fc39fdec7b591d4dd6cbcd58ecab8ef85f4a50244792ce0b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef5707b49ab3f9adf26a56a9cbf6e4e78517b050e3b2fb0364f0da00f24be43`  
		Last Modified: Tue, 21 Apr 2026 00:08:36 GMT  
		Size: 3.4 MB (3394528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93e0c3f1bc24f5a906884d4f60c44e459576b94f446616a5d85b9f99099e64d`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac4a74a9a53d69bcedb3a35d02f3cd37a6d429742ab1fdb508f31d983f54d86`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97af490d1d2239d0247cd840d1484d5d454ca169df2085b09c458aafd6fd0b4`  
		Last Modified: Tue, 21 Apr 2026 00:08:36 GMT  
		Size: 17.9 MB (17882904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89238103243275f2a60886defdafc2cc3273f86991b81361f68cb4412a1ce84`  
		Last Modified: Tue, 21 Apr 2026 00:08:36 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f2fcd0a8c8910cfe23cdc7b7f806a4a6f2a4e768fe42fff95f3b6b4bf7fa251a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77b04e174c6dfe0ab7846a82c85075337e3469d0ef0167dae8c0290864c79eb`

```dockerfile
```

-	Layers:
	-	`sha256:1e998a2dfee9b2b9098be9e582d8f43b4229d3689201c39322666ffefa251c5e`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 30.8 KB (30759 bytes)  
		MIME: application/vnd.in-toto+json

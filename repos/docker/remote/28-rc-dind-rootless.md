## `docker:28-rc-dind-rootless`

```console
$ docker pull docker@sha256:cf97d0513ef765ef7e3d1efa900cb86afe840eeeaa7b1ba3df8872bf4af71f59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:a9e36c23a7310b878a5fc0591a0482a185a1874ff7d70c7c93a9f3175d9f1de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158991376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ff64a88e3f2b9b4d951d83462655ae9f0aaf2d02d1a38ba3471a46033f70ef`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Apr 2025 22:41:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
CMD ["sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Apr 2025 22:41:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 11 Apr 2025 22:41:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
CMD []
# Fri, 11 Apr 2025 22:41:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 11 Apr 2025 22:41:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b82f98882244bb9d1481b825199ad2b76e2c9239fc45d5c541315b4011253c7`  
		Last Modified: Thu, 08 May 2025 17:07:35 GMT  
		Size: 8.1 MB (8062942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6365b308b5b9f32c39fb560ec40ce658963ea6906d5ff55e3608c5a822f48c`  
		Last Modified: Thu, 08 May 2025 17:07:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d294f5c5369f5348a56f5d9eda2cb0feaaec36c469999c191271eeb5850409d`  
		Last Modified: Thu, 08 May 2025 17:07:40 GMT  
		Size: 19.6 MB (19559040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e57ba5f1f955f8d8a91590204b831a0153f8784db500f322c41162fd4ea962c`  
		Last Modified: Thu, 08 May 2025 17:07:42 GMT  
		Size: 21.5 MB (21456663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baa0e697b5049318d66b2c2cdf30fdfe2f33d5c2f3689a91c8cfc74a149f456`  
		Last Modified: Thu, 08 May 2025 17:07:43 GMT  
		Size: 20.9 MB (20915259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3630a0390b53977ef7a5eee3302c846c61b7dfcaabd00260f25a56b7ccc9ef`  
		Last Modified: Thu, 08 May 2025 17:07:41 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53700ca860971e50ba7280e28ad32e38747f0b2065f9aa68242a139c26f57702`  
		Last Modified: Thu, 08 May 2025 17:07:43 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ca69b15bee017a3309e6ba5e902a094bb15c81a39d3d1aa55b09f60e9df4fb`  
		Last Modified: Thu, 08 May 2025 17:07:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a254bad1d61455e27fc173f9a5ddcea9ddea8b927f1deba8b5d51e7a99c851`  
		Last Modified: Thu, 08 May 2025 17:07:44 GMT  
		Size: 6.7 MB (6733011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22be4e734a83f081f10034828e21317bb44b46c01d37eab0e7aa50b38f61cbac`  
		Last Modified: Thu, 08 May 2025 17:07:44 GMT  
		Size: 90.3 KB (90322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc39ab914edae98679270bfe0aedc71896f3a20551a9ccac086aa3031bab7387`  
		Last Modified: Thu, 08 May 2025 17:07:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05303656ec0611db7afbf21ead2a1cb3907d22e1741a4df763ebbaa315b2de56`  
		Last Modified: Thu, 08 May 2025 17:07:54 GMT  
		Size: 60.4 MB (60354806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137b364139553e2e7f9ad4671a9d57de866dca1ed4aaefd3abf52f84411cf555`  
		Last Modified: Thu, 08 May 2025 17:07:46 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f40e1a4761b6c307c0f6f04deb5873d8b8ea25d1752a89d15c7d80d62bf609c`  
		Last Modified: Thu, 08 May 2025 17:07:46 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d204b1c33fe76ffedd9847936a2fa6401e7b95a31e77e9f4be9cf89fe325c49`  
		Last Modified: Fri, 09 May 2025 13:32:09 GMT  
		Size: 986.6 KB (986574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727e92bcccb2bbc51426ebd1461a3ed08edc9154e5d09cb08980b251126eca47`  
		Last Modified: Fri, 09 May 2025 13:32:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e357cea035ec3bff83c8cb960fed37c40c612069bfb4056e696f179cb30f5aa`  
		Last Modified: Fri, 09 May 2025 13:32:09 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b734111308c542e04fd2a07b5643fbec527347e1dd7bc07461a964f4b631c0b`  
		Last Modified: Fri, 09 May 2025 13:32:11 GMT  
		Size: 17.2 MB (17181067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b97e95d75773fef60c9f359af1a5709c69727a59d4a07f46901f0fd897551e`  
		Last Modified: Fri, 09 May 2025 13:32:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c3ca34fd502c71ea2d99da21a1754ce7a05c0011c992f6451d779a90200dffc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567bd52bcbf5dc1f9a18cbb729b59898aed2135d5abc4a4a0648a997bdd6a843`

```dockerfile
```

-	Layers:
	-	`sha256:efec928f47da8c8409acadebbc07d5f5775a15cfc03ee6a8079db240144212d8`  
		Last Modified: Tue, 15 Apr 2025 22:07:35 GMT  
		Size: 30.2 KB (30204 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:34b23709c41993ade68370dd88b04f3ba033fe65df5757f30cd15a0d946b05ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152493005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc639c0df2286ec24dfdd562748c675ecbf3e50a5109f358ebb3d0f0663d7c5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Apr 2025 22:41:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
CMD ["sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Apr 2025 22:41:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 11 Apr 2025 22:41:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
CMD []
# Fri, 11 Apr 2025 22:41:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 11 Apr 2025 22:41:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e41a332ac34c555abfc416477e260fbde6301802d8e137957166d7b7269e14`  
		Last Modified: Thu, 08 May 2025 17:19:10 GMT  
		Size: 8.1 MB (8077251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025b44bc2c49279b62c624fcbb004d6fb2af3e11e622deceb7b73b2d962d7213`  
		Last Modified: Thu, 08 May 2025 17:19:08 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a375c907b7effa0528387483184ba4e88fbf54b2450cf19679598de2bcf24e`  
		Last Modified: Fri, 09 May 2025 05:08:52 GMT  
		Size: 18.5 MB (18472338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e00ff2ea159a6bc4b1ee024eca5cf0db23d527f5e50393fdceca1a64615f6`  
		Last Modified: Fri, 09 May 2025 05:08:54 GMT  
		Size: 19.7 MB (19692466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb96c99dbb0b0624b1cb5125fdd1759011e1aa6916d091cbff119984a58421c4`  
		Last Modified: Fri, 09 May 2025 05:08:53 GMT  
		Size: 19.2 MB (19165688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2243b02a6893b07cd466ac580162ddf8b60b0eac492683c645456c539a8def6c`  
		Last Modified: Fri, 09 May 2025 05:08:54 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28b3b4409894df19fc82e76984f5dacf66c2ce0aaf9d02f1a4d36faad9b79a9`  
		Last Modified: Fri, 09 May 2025 05:08:55 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d84a947d698a01300252cb9ff97afef0a967e4f97eceb927d484c05ad5ba3f`  
		Last Modified: Fri, 09 May 2025 05:08:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f3be9db602c1d64f98037ffca8204dd1a74b76e42f1ea72842bf499212f4aa`  
		Last Modified: Fri, 09 May 2025 05:08:58 GMT  
		Size: 7.0 MB (6978821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2003afcb6aa08be580d2693f92fc399004a9502f4f280a31198a604533257df`  
		Last Modified: Fri, 09 May 2025 05:08:56 GMT  
		Size: 99.4 KB (99394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f764bc501ecbbafdd4d82a22a7b7d64b829c0c900a027bbe66a24deae5a2ff08`  
		Last Modified: Fri, 09 May 2025 05:08:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e788354cf9a08ff0dd7bf70f6d9739c1c7ac6efa64ad3ec1c2c4502653468f32`  
		Last Modified: Fri, 09 May 2025 05:09:05 GMT  
		Size: 55.7 MB (55714558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f73906cb951c7fb15d09806089703adb23f67e0110bf92bf05b29731fd5d14`  
		Last Modified: Fri, 09 May 2025 05:08:58 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0429fb2aeb3b26763210d8b85726290133cbf6a140bcb9ca30d9cad432492f`  
		Last Modified: Fri, 09 May 2025 05:08:59 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ee2841abeab7bd91c76f42e4f062eba290b242261800962e16f58b2497a390`  
		Last Modified: Tue, 15 Apr 2025 22:25:25 GMT  
		Size: 1.0 MB (1014203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bec6ed76c92b953a086ffe00b33043973f26d25f84d303b12e1fbebb54522db`  
		Last Modified: Tue, 15 Apr 2025 22:25:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e737aa5a8a1c2bc78befaba26800c2951e266112bd13b7d1d6328877943c8d08`  
		Last Modified: Tue, 15 Apr 2025 22:25:25 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb0bb16b3abcdc7774a398cf793a01c9c940426378aed1881f9a35938e1612`  
		Last Modified: Tue, 15 Apr 2025 22:25:26 GMT  
		Size: 19.3 MB (19275805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833459fd0bd845f5ff52278525560685e43d21f5e87c92e9fc320a5a77316e0`  
		Last Modified: Tue, 15 Apr 2025 22:25:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:954b8d184091b30251f5bcaf499a0768bb59d98d65258f62fef92beb6ad989ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1b64bba6f7f1516d00537e4dd87314a733427a171c0cfe9311567cae2fddc1`

```dockerfile
```

-	Layers:
	-	`sha256:f1710145e58895814fac8a92b9da22083171b96675624ba8d888306fb636f704`  
		Last Modified: Tue, 15 Apr 2025 22:25:25 GMT  
		Size: 30.4 KB (30361 bytes)  
		MIME: application/vnd.in-toto+json

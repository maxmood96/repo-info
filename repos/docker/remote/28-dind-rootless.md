## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:b48c7d1e7e4a202a4ac0c4fa55935b42b81b87d3110e3e267839ae52214c9e16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:b1a0efebeccb1aa0698d2947c7c0e4f9a99ff048a09e639d0088d0cbb7d3bf81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159035388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2939d9461edc15d77aa003d12c3f7c5e48ef11e1ce52a247c8f0e3e0cc90e251`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.1.0
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-x86_64'; 			sha256='7bdb2ce2916e5dd0354e5d129892bf96fdcdb1a9ab8eed69b9173e131db4c230'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv6'; 			sha256='dc555cf80a1c5849853a71083f4930790e6515d14c31060de77e6d83bbc996c3'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv7'; 			sha256='50aba1c8fe1eb8efefede3dab9e6c2226ba756a5ffa5cf4f4f5baadaee9a7455'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-aarch64'; 			sha256='a91e930a076b91e6c69f11d1dbe3c06729ae765fb9dbb3f97cb808e784647399'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-ppc64le'; 			sha256='fa6b67a69916a99d14191df5dee1e8399d5eb07f1d322f04caa2078045cb0140'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-riscv64'; 			sha256='c582635c0c4fb1e692dd8a7de206373866f2aa3fcfd9cf03d2358585e602e15d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-s390x'; 			sha256='8cb63254106ceded2373a86355f48ea410564e748521a4b097e3d43b93c05e24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 17 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:04:16 GMT
CMD ["sh"]
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 17 Apr 2025 17:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 17 Apr 2025 17:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 17 Apr 2025 17:04:16 GMT
CMD []
# Thu, 17 Apr 2025 17:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 17 Apr 2025 17:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 17 Apr 2025 17:04:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98ba9902857ddbb8552004010cb7e9d38ec727cb6023b99c5c8eb3fd4ce6081`  
		Last Modified: Thu, 17 Apr 2025 18:27:38 GMT  
		Size: 8.1 MB (8062893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c58f351bf97fd28e58cd8060cef8a6f34d9c092e35a3a429552862a9b80da1`  
		Last Modified: Thu, 17 Apr 2025 18:27:37 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fbe10d2a92f2d8205b7fe7a61aa3f5de4275dfff73384f00e215cadef52f23`  
		Last Modified: Thu, 17 Apr 2025 18:27:38 GMT  
		Size: 19.6 MB (19565542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09cf47617ff6abf5514035959688907e7f54de6ac3061a82a07a38d339675a9`  
		Last Modified: Thu, 17 Apr 2025 18:27:38 GMT  
		Size: 21.5 MB (21456647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9167b1a9e2a49008626c0da4079fb7fc4185f701466445fabf46d4fcadf1c4`  
		Last Modified: Thu, 17 Apr 2025 18:27:38 GMT  
		Size: 20.9 MB (20923468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d66e70b322ddce654027aef73f3f8a95a24d341fe1fea3f755072f42e16a70e`  
		Last Modified: Thu, 17 Apr 2025 18:27:39 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6ad03f16d499462ef3e149f7d35f2171dd287cd29105b97831a8da33583e86`  
		Last Modified: Thu, 17 Apr 2025 18:27:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4658f721145adb14dde848bcf6c0620cb4c1b9ef27025ca588e6cc77ddf48e`  
		Last Modified: Thu, 17 Apr 2025 18:27:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23b559c98d4d75ed86ca6a293a1f906179cb97a02692accc05bc412a5aecb0b`  
		Last Modified: Thu, 17 Apr 2025 18:29:28 GMT  
		Size: 6.7 MB (6732960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812d0ded7cfbee230218c9d274ca7e3e84b1810f1d77d669183defd0500acd66`  
		Last Modified: Thu, 17 Apr 2025 18:29:27 GMT  
		Size: 90.3 KB (90333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f04fc4be82606d17d6d368adc9dd33ed55cd9f86b73a24fe04a885a7673136`  
		Last Modified: Thu, 17 Apr 2025 18:29:27 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edbdc891cb1c1be629802ab8083b773631194d62fd0941dc56d47a284aac729`  
		Last Modified: Thu, 17 Apr 2025 18:29:29 GMT  
		Size: 60.4 MB (60384203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4366cca22097f47c1d5c28b5b5ceec9580334d8d038adcfc4ad1fe54eacd1dfb`  
		Last Modified: Thu, 17 Apr 2025 18:29:28 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f666af814df31313dc622f12ca4ad0db8a59aacbc6c6b678be5cd149d25a738`  
		Last Modified: Thu, 17 Apr 2025 18:29:28 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c8588fc770380c19c56d29e421aa46c456c98abc50802c74ceef62ffb33a57`  
		Last Modified: Thu, 17 Apr 2025 18:52:02 GMT  
		Size: 986.6 KB (986581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c35e938ac01c61bc30d50047dfd9296b949a36d428b94ae7efb3d77f4322be2`  
		Last Modified: Thu, 17 Apr 2025 18:52:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789627391791a59f2670a5d1699b9ba506c54920f229b250d859e4db88603f94`  
		Last Modified: Thu, 17 Apr 2025 18:52:02 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b274c02562a092225d0c7bcfdd5decc73340668a7aa6afe15b70c72e31990654`  
		Last Modified: Thu, 17 Apr 2025 18:52:02 GMT  
		Size: 17.2 MB (17181070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d0a63455012dba6a549be337396f94feff33542bd6b38b366c31325e695565`  
		Last Modified: Thu, 17 Apr 2025 18:52:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bb9cfee1437abc57391e785bd4526aa0f0b298bab0a7809d7b565f0d00cbcb19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff27ae637af216d919b763d41d6ad4ccd49ed14bbae05132811cf7892c4d7d0`

```dockerfile
```

-	Layers:
	-	`sha256:0b36355f51bc903b73f6c6e969469be08102f3d7a9e95c87294e133b462eea54`  
		Last Modified: Thu, 17 Apr 2025 18:52:02 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1ff1b98f479dc58cfed04fb991acff688f27a33361568286d93f4b2bf7c43acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152480473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83441b3def8697388a05af1983ee55c6a63d6b2d35756fd153f06c58041d6aec`
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
ENV DOCKER_BUILDX_VERSION=0.23.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
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
	-	`sha256:55e41a332ac34c555abfc416477e260fbde6301802d8e137957166d7b7269e14`  
		Last Modified: Tue, 15 Apr 2025 22:05:00 GMT  
		Size: 8.1 MB (8077251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025b44bc2c49279b62c624fcbb004d6fb2af3e11e622deceb7b73b2d962d7213`  
		Last Modified: Tue, 15 Apr 2025 22:04:59 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548b10c496662caab533c3d131758d622285b3f373756838531f1a168224831`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 18.5 MB (18457152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a45d6fe346d03b0272285dd9725e00aefad8b06d1f295635b39c9630cc6a6`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 19.7 MB (19692478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510dd6065899f34e92a17b88db1cb1ce4b9130bcd36f87ff97a9cfc7cd2430b8`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 19.2 MB (19165660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803567d33d1c34c1f24b0f2ca1c14b4b236cc528d23d4b4e2cd31a71d2d95cf9`  
		Last Modified: Tue, 15 Apr 2025 22:14:27 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640dbcafae79da65d205c76809ffb4d36184629f730bbfe5390d61bdbb9bb592`  
		Last Modified: Tue, 15 Apr 2025 22:14:28 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac5cd38945045e3390b31fbbf1b98016e77d70bfc1c8e4943c8a511454f46be`  
		Last Modified: Tue, 15 Apr 2025 22:14:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dc6d9cc98ef412cebe1089c79a0b32ddfed7b3321d6fa49c3b1d7dbe4b3c70`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a9f3b4322221600837bd19350617e9fbdf944b0f97ea579f4969f6e5d6049e`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 99.4 KB (99378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60eb0dce1bf078d608f862da78405ed0a6787825fbd8f9584b22f503dab449c`  
		Last Modified: Tue, 15 Apr 2025 22:26:01 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ed7a6d0e2d072bf5c0d02797956e1062a2c902e2aab07367bdfe977c466161`  
		Last Modified: Tue, 15 Apr 2025 22:26:03 GMT  
		Size: 55.7 MB (55710879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb1e30286ee5a0c6035e171d60a2b4e64cceaf5e8d3b4b7744f47a2c3affcc0`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f180e29b0ef2ab0fe57327b9d65d69b7d92b6245d338b4a9eaf59353772f325e`  
		Last Modified: Tue, 15 Apr 2025 22:26:02 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593538725234e7f5471d5edcd1545b428c2be3e765746760f8fbaea46b2965a9`  
		Last Modified: Tue, 15 Apr 2025 23:07:21 GMT  
		Size: 1.0 MB (1014211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f87db4b1a10e689b727a320ef2869a263d4e8c3dc046cd0976435e2d34d983`  
		Last Modified: Tue, 15 Apr 2025 23:07:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48c5275d28148d3c58af76a48d45befc03d686c8647f4569a07da472d3fb932`  
		Last Modified: Tue, 15 Apr 2025 23:07:21 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f1b4eeca171dd968721ebed2f30758cc913ca1fc968d32aaec90b0e4501fc0`  
		Last Modified: Tue, 15 Apr 2025 23:07:22 GMT  
		Size: 19.3 MB (19282132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19c98b4578bd75541d368745c684355023aeed914370664c16ce434016cefa6`  
		Last Modified: Tue, 15 Apr 2025 23:07:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:de3d621c088272cc86d5c7777395aceab3af8e685ee6605b4f4011e6b8f02f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724e2934dbdc120f6444a7c1e06fb77a2ebb3194079761af1ea85196deb8f8c6`

```dockerfile
```

-	Layers:
	-	`sha256:6afe9376f42157faae689cdd015195db7c251375305753dc292b96e889342beb`  
		Last Modified: Tue, 15 Apr 2025 23:07:20 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json

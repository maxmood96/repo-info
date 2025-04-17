## `docker:latest`

```console
$ docker pull docker@sha256:dbd0882bf05e6225bc64c35308f5234a33c511dd38d333ff422a9cd8aa3840dc
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

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:225345ea1006e618abb6f4fb8bd4bd48465061ecddc243cf2d595a6b955284a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140866400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06c0b0b4d26d3761a1104657e134e434267f2f4ba2ac30e68e2f2c253b176bc`
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

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:254cf1befc2af2acb7313e7eb6612a71a6beff0b21f03d0c6ae95db9052619cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd02ee6a581985d63add5b687b854d9648348328a42b55643f2f9f7fa3538e8`

```dockerfile
```

-	Layers:
	-	`sha256:c1d8c152f5ff1197e8d1d78b00b40360e3ce285ca264995da2d7b2105b358e64`  
		Last Modified: Thu, 17 Apr 2025 18:29:27 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:51212062ddb8b55cb878a979db965bfd39ab9767a3f1f7fff60a5206239ecffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131521451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216ecd7e2619a0dadd8eaa7a9a1627f5618d860b0cbb86a9d7215a6ce3721645`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:8adf473a27e29a258983cb420fbb9e1b8eb738c8df934e10bd9cf65f8e3b3818`  
		Last Modified: Thu, 17 Apr 2025 18:37:41 GMT  
		Size: 17.5 MB (17512375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9a06738d784bf4e963932fa09b019d5070323c9534324cdd5b6534de7d9bdb`  
		Last Modified: Thu, 17 Apr 2025 18:37:41 GMT  
		Size: 20.1 MB (20075420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd128f280e440fd59f8125420e2ee27393cbd8a4f624ecb6150418b8d5e09c6`  
		Last Modified: Thu, 17 Apr 2025 18:37:41 GMT  
		Size: 19.7 MB (19678196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948f18c9fc1eb05aa1ad4c59270c2b97935ef90ce42f7294717700b08b8a6a1a`  
		Last Modified: Thu, 17 Apr 2025 18:37:40 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965e6b27a4811e4b67ff12dd913227fd58ec2b50097afa4fbf034adffdf2391`  
		Last Modified: Thu, 17 Apr 2025 18:37:41 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6359ce0f810633f17052402705d1547ea3c8af51eff1a9a0ca7df3c7c37239`  
		Last Modified: Thu, 17 Apr 2025 18:37:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6f001b64c6ec16d38ec37de066be2b448de7e37c97da083fe6d534ff83b5e1`  
		Last Modified: Thu, 17 Apr 2025 18:51:41 GMT  
		Size: 7.0 MB (7036878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d04d3a8c6ffb04f6f19fa70cc72e02caa6d14dc4f2fe8373ae5107e62a9db0`  
		Last Modified: Thu, 17 Apr 2025 18:51:41 GMT  
		Size: 89.9 KB (89863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601438b7e614564a9152822cfdc974f026b29623fd093068b8597e15c93d1af2`  
		Last Modified: Thu, 17 Apr 2025 18:51:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dca6396893b164971e5007da7eb351b23a4d2c9f58b8ebe5a05c4a6ecee2b1`  
		Last Modified: Thu, 17 Apr 2025 18:51:43 GMT  
		Size: 55.8 MB (55777719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73abad49efef5c6ef9e9b523bd714dda01992e1adce23c601ca052f54abf5e4b`  
		Last Modified: Thu, 17 Apr 2025 18:51:42 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f53ad53d1bdf3385249575f3938da0ada7d0c7419243b1fd94f7132a01b45d7`  
		Last Modified: Thu, 17 Apr 2025 18:51:42 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:785ade079392fdb55b56b6a359a325473e6938392fa91c145543d5077e354105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f295acf55d454bd5dd11741379e374c55567176a6f77d94e5321d1f75e677`

```dockerfile
```

-	Layers:
	-	`sha256:a0136f9c978a74c3fbde19d496f5b4c7a103393532df57889ee46361f26720a5`  
		Last Modified: Thu, 17 Apr 2025 18:51:41 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:cd010b16467edf2a69e84f2a83b8a788d1260f7a7f792a26f1c7e4a0057533cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129850661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df986bfa6b9ad5582f5485960f9cbb28ef0eb2a73c51b1fc23cb4258da7289b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a864060af87a5048c5c602ac87964067948691631141ffc3818333edb16ed6`  
		Last Modified: Tue, 15 Apr 2025 22:13:41 GMT  
		Size: 7.3 MB (7301755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c418fb5b9eb8648b75bfdc32d3b64717b14e09489dfedf7e46fc76341ad53`  
		Last Modified: Tue, 15 Apr 2025 22:13:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c02a9075e72ac575ac987686b524566b5f2b30af5e1b60e0c5547721e21b2a`  
		Last Modified: Thu, 17 Apr 2025 18:47:51 GMT  
		Size: 17.5 MB (17499394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9b808cc99ebc19e3353f54a0387e28e34c83321d3ab3e2d4ecccef5948bbc7`  
		Last Modified: Thu, 17 Apr 2025 18:47:51 GMT  
		Size: 20.1 MB (20055853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb98544edcd3c20cfc258994aed0930a970ca38bcb51299e8ef913cf8c16d4c`  
		Last Modified: Thu, 17 Apr 2025 18:47:51 GMT  
		Size: 19.7 MB (19657168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06763d10183a86dd09b104d5ad2b23d1690346d0c33dacc59a12d108ae524faf`  
		Last Modified: Thu, 17 Apr 2025 18:47:50 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c62ac809958758f2c08a74c22018ef77d4d7fb57611bba964b0d7be94ae26ae`  
		Last Modified: Thu, 17 Apr 2025 18:47:51 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e9723ac14fe6cee302b4cb5f7690a28a211d0dfb16d4871a92c564e8dbb80d`  
		Last Modified: Thu, 17 Apr 2025 18:47:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c588a4fd622af880ec0e026856ae5730d34f82a0a4d5fbeaafba3de88d649581`  
		Last Modified: Thu, 17 Apr 2025 18:52:28 GMT  
		Size: 6.4 MB (6366158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3ea1ad0294fdbfd009a23130320783fb5efa530f8237aebc7518a9e7e690f`  
		Last Modified: Thu, 17 Apr 2025 18:52:27 GMT  
		Size: 86.4 KB (86358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4be754769bb6039a34569e77713fb2fb10634ecbeacfeffc414ff4759ad65d`  
		Last Modified: Thu, 17 Apr 2025 18:52:27 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3490c40d6bf92c46ac04aff29696f2f3245e08524198993ae08ffcfb22dde13b`  
		Last Modified: Thu, 17 Apr 2025 18:52:30 GMT  
		Size: 55.8 MB (55777719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86df9f5210d7e52525f30a08893d21db27c6257b73be6ded22019192ae7262ba`  
		Last Modified: Thu, 17 Apr 2025 18:52:28 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0d7588bf5e54c0ee5a8a0ad088967a2a2174dde5683dd739d36022c90ec7b8`  
		Last Modified: Thu, 17 Apr 2025 18:52:28 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a8ed15bce1724be4895880596e9fc964f1cb37bea6b5ee30725e41e53d67159b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949b0cf6b50ece5a38653de904c3686ae9a34eafc35e30104142d2c7dc2aeea7`

```dockerfile
```

-	Layers:
	-	`sha256:f85ded834c252ebc3bf6e261bbb4f978179b9a718b078c6250c426ad68d621fa`  
		Last Modified: Thu, 17 Apr 2025 18:52:27 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d01c9690143c1fef82eedfa8e81c1bef3f3f6111a3e5204ddfe705e7d0366930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132260957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59559f55ce42edf9fb7d877e656eabe9caaa20ffc4450108c761ca012747eaf8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0757cec9b8247b57760f8b7130dddfcd875393c0b6fe5b8594e1436bda11e0`  
		Last Modified: Thu, 17 Apr 2025 18:50:46 GMT  
		Size: 8.1 MB (8077204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdc4631afb83d6365951521e4c046c2514791d363972aa8113ff0005204a4ca`  
		Last Modified: Thu, 17 Apr 2025 18:50:45 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a78f3d251baf12455053c55dc15e95b86aee510a7100848d03aacd66714760`  
		Last Modified: Thu, 17 Apr 2025 18:50:46 GMT  
		Size: 18.5 MB (18485728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72baf470aa0e1470980f0235fdf31e788c64a43253424be724d7c2e2110aee0d`  
		Last Modified: Thu, 17 Apr 2025 18:50:47 GMT  
		Size: 19.7 MB (19692490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2f9cad1a5086226688db1f3525de29b7fe714033dd8a68897dadd9917eada`  
		Last Modified: Thu, 17 Apr 2025 18:50:47 GMT  
		Size: 19.2 MB (19183018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d2fecf01b5569a6912eb88aef721d7af007ca0f636af39f65bc32fe26368a2`  
		Last Modified: Thu, 17 Apr 2025 18:50:47 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d6874a88f7d04bdcbf76e8214df85bf4c88c14f5b7ff0ad9a9b420db1ae81`  
		Last Modified: Thu, 17 Apr 2025 18:50:48 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afad8ac09d3c53cc6eef808746d7bc9fc4ed8150e82472e70b689990e157d5fc`  
		Last Modified: Thu, 17 Apr 2025 18:50:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158563ba6888deb70f2b1340c029779ad2bff78380d47a5bcb808ba492a11919`  
		Last Modified: Thu, 17 Apr 2025 19:07:26 GMT  
		Size: 7.0 MB (6978950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10aef32a036494d4494d609141dfbf9deceb362ce035d7d648391c239799a7da`  
		Last Modified: Thu, 17 Apr 2025 19:07:26 GMT  
		Size: 99.4 KB (99398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35c6f419490af39eb87a9e7cf05542a9b3c8cb526b967ae41eaa194ccf2fbed`  
		Last Modified: Thu, 17 Apr 2025 19:07:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3112d31e58543629646b098fc6fa868b2b5f8bbb63d8cc7854ab2e636512696e`  
		Last Modified: Thu, 17 Apr 2025 19:07:28 GMT  
		Size: 55.7 MB (55743028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7135a381160411989a3d878811229804aecba1c677e30aa811c62bb795b3c91d`  
		Last Modified: Thu, 17 Apr 2025 19:07:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d625c8ccbefa20514d5c2b0f208b96359ab9922ae1a01cb4b26da69f5eef0c`  
		Last Modified: Thu, 17 Apr 2025 19:07:27 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:ae8661da163ade85e71ec4d39164ca743b3f2d9abc8913b1b61a92dbb0c54dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8947f05b07b26bd9e25a7c3f73aea46bc0ea5b8e0289a068d013790b260e7eb`

```dockerfile
```

-	Layers:
	-	`sha256:af7c0cd469bab298177aadf1e2289b7eaa2de66345b36547aaebe96158a28a38`  
		Last Modified: Thu, 17 Apr 2025 19:07:25 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

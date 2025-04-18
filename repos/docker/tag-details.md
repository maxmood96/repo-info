<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-1809`](#docker28-windowsservercore-1809)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.1`](#docker281)
-	[`docker:28.1-cli`](#docker281-cli)
-	[`docker:28.1-dind`](#docker281-dind)
-	[`docker:28.1-dind-rootless`](#docker281-dind-rootless)
-	[`docker:28.1-windowsservercore`](#docker281-windowsservercore)
-	[`docker:28.1-windowsservercore-1809`](#docker281-windowsservercore-1809)
-	[`docker:28.1-windowsservercore-ltsc2022`](#docker281-windowsservercore-ltsc2022)
-	[`docker:28.1-windowsservercore-ltsc2025`](#docker281-windowsservercore-ltsc2025)
-	[`docker:28.1.0`](#docker2810)
-	[`docker:28.1.0-alpine3.21`](#docker2810-alpine321)
-	[`docker:28.1.0-cli`](#docker2810-cli)
-	[`docker:28.1.0-cli-alpine3.21`](#docker2810-cli-alpine321)
-	[`docker:28.1.0-dind`](#docker2810-dind)
-	[`docker:28.1.0-dind-alpine3.21`](#docker2810-dind-alpine321)
-	[`docker:28.1.0-dind-rootless`](#docker2810-dind-rootless)
-	[`docker:28.1.0-windowsservercore`](#docker2810-windowsservercore)
-	[`docker:28.1.0-windowsservercore-1809`](#docker2810-windowsservercore-1809)
-	[`docker:28.1.0-windowsservercore-ltsc2022`](#docker2810-windowsservercore-ltsc2022)
-	[`docker:28.1.0-windowsservercore-ltsc2025`](#docker2810-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

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

### `docker:28` - linux; amd64

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

### `docker:28` - unknown; unknown

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

### `docker:28` - linux; arm variant v6

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

### `docker:28` - unknown; unknown

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

### `docker:28` - linux; arm variant v7

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

### `docker:28` - unknown; unknown

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

### `docker:28` - linux; arm64 variant v8

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

### `docker:28` - unknown; unknown

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

## `docker:28-cli`

```console
$ docker pull docker@sha256:23cfbeefc3f4aa9d521bb97e07aff63b9c19eb9f9ba9c32bc8239fbc2b77775b
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

### `docker:28-cli` - linux; amd64

```console
$ docker pull docker@sha256:52d88de2357048962588f26d27598908cd1be13d5e0cfa1523793ecb8f32803f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73652948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deb61ad03625c2200c09cad15db296babe3c4062b62bcd8dea55e309e6dacab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bed48dffce491e86191ef39ace19f81a2e044e5401a8d6e8113c30dd908057d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aea4a8d4ac8b8867270838ac3bd213d1c9d134128501dd403ec934bfe16a36e`

```dockerfile
```

-	Layers:
	-	`sha256:f61c57a32213435eba0c6b56580018ac6cfbe388950fbea0037bcc1f54aec289`  
		Last Modified: Thu, 17 Apr 2025 18:27:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:976b17c9d79aadcf387020b276b1620f5578cd5ad57011b1fe492c700cecdb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68611022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf5eb5389a8724919b6ccd89b41c8136d76061e1ea37a46a737e431f20b44c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:03f4c260d41dd0e996485037f1b9ffef9f444f1ca91a61445ba81756e795e8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c20cab2d97bf3bc5fb66556065c08457a53ddb5a5a9968554786cf4a1d00dc`

```dockerfile
```

-	Layers:
	-	`sha256:5d4618616647f7f5308a2b25569464bbbacc5520ceea1774cc737aae46e2edea`  
		Last Modified: Thu, 17 Apr 2025 18:37:40 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:f6b490990228b32d94ae1278f88635fc2e1d93142499ceb34c1fbb85c8380589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67614456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c294c0838b5dd0f46960db67103d333f672db373138f1b3bca47fb8a7dafd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0074b191fefcd2671ee2ef868b889e1c37900ec53186fbd05d3859d701b0194f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0179e3cecec651439cd64ff00de3dd60cb8beb8d33868f2a09806ea1db0f8`

```dockerfile
```

-	Layers:
	-	`sha256:e0b21c112521c52dda1e986c3f5a6db7d546098fe5db90c8fbc5cfe35109abff`  
		Last Modified: Thu, 17 Apr 2025 18:47:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:68303eb35ec3a17a21c305d5abafa4cf56cfb4e0c55995505fbdb04edfe57c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69433624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348b53b676688ea63e108cececef7c952a275896e39c37122f36892a0868391f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:10193cd16309c1c701e67561f2d98cacaeb1901ed358fd016e613384a52eff8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045be3683929bf108fcbd2bf97b6eadad5bac7f3168464e62009e63aa7568182`

```dockerfile
```

-	Layers:
	-	`sha256:bd4fad60791b68af4c6c575d9a4db26bc6009d708c47251c8bd049b8b827b678`  
		Last Modified: Thu, 17 Apr 2025 18:50:48 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

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

### `docker:28-dind` - linux; amd64

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

### `docker:28-dind` - unknown; unknown

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

### `docker:28-dind` - linux; arm variant v6

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

### `docker:28-dind` - unknown; unknown

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

### `docker:28-dind` - linux; arm variant v7

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

### `docker:28-dind` - unknown; unknown

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

### `docker:28-dind` - linux; arm64 variant v8

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

### `docker:28-dind` - unknown; unknown

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

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:cfae1360488abdc3ee0dba4fe89420793f34e218e3e1d969f90881eb60f94af1
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
$ docker pull docker@sha256:082a0182ac140cfc2d1b3de83637d675af1895a5c0f1844c1dabcae22ea12d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152552323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6899d44cbd6b5d6f55e7bec6805176b66565c9254ccb6fb6dc880be0477d5f`
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
	-	`sha256:ce10ed87a566d0375a64ba19c179459aeae36eede6c6fcc5ecb92628cd8ffdb9`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 1.0 MB (1014220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58c7ebb5111b8ae78ffff6d7b250c03079262ba4a3f4d4b28aa56a133973968`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0d50a20adc69d9af9a41bd1100c27472aa6cbf6f2a160088cab1964906c015`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bd366ce6af6776aae3c1950bb0e9a794d7f48bd180242e76c42efa8c6d3edb`  
		Last Modified: Thu, 17 Apr 2025 20:07:18 GMT  
		Size: 19.3 MB (19275808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ff5a38300abcf02c0d3894bc80f20837030fe834a406bfa591f5f77c28475`  
		Last Modified: Thu, 17 Apr 2025 20:07:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b634773f6d82167e92b3d1179f6bbe6db843825690ede3a80eb2f4e93404bca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a11aff44f1f49258f5942f0dae84df86fbd3e3943ca0e2b6b73aa1a9fb91fe`

```dockerfile
```

-	Layers:
	-	`sha256:54cc39183a3e3de25f55ee17bbc754f7a1e525409795fd4899f4169864704d8d`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:429c6cc329d558cde0f693432c7025e2ebd2997e97851488850d34cafdc3d804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull docker@sha256:1688b4283d6333dc6b062b9725f33e581febe882f118bdaca25c16a43952408c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459681963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a67f4377ec1505bc64fdd5fba308d67690797d25ae8fae2c2abe3a8220b470`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:14:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:14:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:14:12 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:14:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:14:26 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:14:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:14:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:14:38 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:14:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260c6bd48bf9b7bcd23a74ce27f83b531faea9e315ff6737ef884b00bd81da70`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d26d0fae6a860033208ee05de1b45fff21172f23e6c08fcb6c8ddd89a4cf120`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 370.8 KB (370783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e04ee05f729c840466ec7fdbddf08441974dd64583ae57b0c2e1e82888dc02`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a31d3ae72d44e6ac1ba7d34ae1f04a19832141dd6bce84fcc466087f8b56eb`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f75320aa722434dac44791dfa0fc684d4a9118fa6391061b2a6f8101d52a7`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 19.9 MB (19906717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3437ffb66e6fb89a8e52416a38c4e07715674914477817e827340751d33df40`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8902215ab64b3c66d798e6283552def1adaaa91ec7060d2b701324013ff287a5`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a4f89a37a7fcddfc7bba6da9b4f189b05df2f60d049e0deb935afa332f2bd`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e20d43751d763b52f2c66c50dac0f795edac26bd54f2fceebbd844ac18b0`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 22.4 MB (22368711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded394e9a68dc176a9ac6ae87bae98371ce9575ebf52a380abe1c57025a67662`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11948f5717802bd1eaac711e6cdb65cbcaac908f474150dbbd248d948802859`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29097adaffd2b10496a62fdf22ccd89530230ca2141515caec61c5e4cff7d9e`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af02f07dd826ea269773bc614ae42f76d01eec6273637e02431652a26045646`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 21.9 MB (21862437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull docker@sha256:995ca0bf38de1f8a0245f2caa155396da4f06cbc594336fb9c76897128890d91
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338010035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe100f55f377339e6d5f4224211c47c2fbb6b253a25fa282fcc1576ced9f558`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:16:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:16:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:16:57 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:16:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:17:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:09 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:17:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:17:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22ed7df539503b8409fa12a12fac0de1ecc8657bd576c4dcad98a9a93f6c3f6`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96fabcddd098deceb4965e2923d655850837faf9387775bb7a3f7347379f68`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 348.4 KB (348428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af955c30c344b96d47b273fc240431ecb647b6d5e6b5a6db506fd0a46eeda828`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e779905e67487e73a71ba4407c8ecfdf2b013b20d213efb032bd04ad16cca2c1`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4805881421d38e32a8c7790733335e6261d0766591620a2b2ff692b5b1b0a0`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 19.9 MB (19886290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a8cfa1b6a752dcfa395a1f04be70be82b8e3b567e5e5068788dbb471737e3c`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60819df3ae15cadcce13014b660c523cb6b6de908488d5b054f4b3a9847a592b`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4d3e5a621f70aa48fd9ba3cfa11d545e447fb079315c602e625b6f4ceeccb`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4da2eae8290184aea1d6de343a3bd28a09a8797b29e585a267a77fe14ee5df`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 22.3 MB (22346645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9a652976a5b14d3f822b16d23e045465bbe41007f536e9adffe54db8f0687`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d342975a32de3069ec71a8b68ac01b3c48ed4667b43bdfb1184c425c513c7e7c`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864f4aa6948b12f6e4eaebbd858bced5d111337ee7ffc5944059dddbf7145b92`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001844b2a9a1d6bbb6fd855f7437999f2cb31fb9f22815db8a4a9579731e813`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 21.8 MB (21834550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull docker@sha256:76e33dc88f985d1beab4d78f43dd885d456de128945b4a6dd03981c5bb2f35bf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229913583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f586db89c826ee7b52a5ebb6e4f0f9b89a87d4eb2eda2cd54dc67e02c90f1cdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:11:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:11:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:11:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:11:59 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:12:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:12:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:12:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:12:13 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:12:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390143f98317407a20ac29c08b9ec3b59ab9a7cd865888e898464db9e33c4b1e`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230494274935a2d45131a3ae53d73013b524f80b5f1c5c346f361572546c443d`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 337.0 KB (336986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae671c2fb897de70375a2ffd366a9df2ca182b54ee1c98fc04054eed585c852`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b60498a9f6b4d861a2fb43e6765f711d9fc862decf8f6669268f935e417efca`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e96b8a20b826e815d7b12e8b80a6870a6d57fda4040e07e958ecbca9250a7`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 19.9 MB (19878251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a665a369422bcdc54e164d7d15190b072e05a725bd7bb0b71b6e8122238bae0`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ec24a0da078daf54e38f2804f68f22646c0635fd9c07e9666160b6a75e8f3`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841757b89b0ec185e9e9c24a2bbaa990da0810e57f369e5c6e275cade454cd90`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71a487c601cdf1b95461f1d743ce1bc4d360fa55fb753d2c1f87c58987ea79`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 22.3 MB (22339705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd42e2c5ce5fadf18e468bfa810ec1a0a31db7526079ae284b593296a82e09`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f848fd528a82281bfcf00e5773ccdfe2c8f7cd77cab21abcefca9df3a3618626`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfefefef3315a12a85b7a2692ec7f43bd6cf67a23e3f69fdce2f31aa05c339`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b76f6dddb987140c5bd123843c626ccb3c54d67ec2c959df7fc666b6dbc8d`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 21.8 MB (21821032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:326ac27545ba0438a8e7108c0385c6d32985cf8b0949d07389e38b03eed5bc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull docker@sha256:76e33dc88f985d1beab4d78f43dd885d456de128945b4a6dd03981c5bb2f35bf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229913583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f586db89c826ee7b52a5ebb6e4f0f9b89a87d4eb2eda2cd54dc67e02c90f1cdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:11:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:11:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:11:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:11:59 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:12:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:12:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:12:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:12:13 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:12:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390143f98317407a20ac29c08b9ec3b59ab9a7cd865888e898464db9e33c4b1e`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230494274935a2d45131a3ae53d73013b524f80b5f1c5c346f361572546c443d`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 337.0 KB (336986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae671c2fb897de70375a2ffd366a9df2ca182b54ee1c98fc04054eed585c852`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b60498a9f6b4d861a2fb43e6765f711d9fc862decf8f6669268f935e417efca`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e96b8a20b826e815d7b12e8b80a6870a6d57fda4040e07e958ecbca9250a7`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 19.9 MB (19878251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a665a369422bcdc54e164d7d15190b072e05a725bd7bb0b71b6e8122238bae0`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ec24a0da078daf54e38f2804f68f22646c0635fd9c07e9666160b6a75e8f3`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841757b89b0ec185e9e9c24a2bbaa990da0810e57f369e5c6e275cade454cd90`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71a487c601cdf1b95461f1d743ce1bc4d360fa55fb753d2c1f87c58987ea79`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 22.3 MB (22339705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd42e2c5ce5fadf18e468bfa810ec1a0a31db7526079ae284b593296a82e09`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f848fd528a82281bfcf00e5773ccdfe2c8f7cd77cab21abcefca9df3a3618626`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfefefef3315a12a85b7a2692ec7f43bd6cf67a23e3f69fdce2f31aa05c339`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b76f6dddb987140c5bd123843c626ccb3c54d67ec2c959df7fc666b6dbc8d`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 21.8 MB (21821032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:e3e1628d403cdb4880246d886cad700aca6626c1c8e17ddd53df1f649aa4bd85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull docker@sha256:995ca0bf38de1f8a0245f2caa155396da4f06cbc594336fb9c76897128890d91
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338010035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe100f55f377339e6d5f4224211c47c2fbb6b253a25fa282fcc1576ced9f558`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:16:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:16:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:16:57 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:16:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:17:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:09 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:17:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:17:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22ed7df539503b8409fa12a12fac0de1ecc8657bd576c4dcad98a9a93f6c3f6`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96fabcddd098deceb4965e2923d655850837faf9387775bb7a3f7347379f68`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 348.4 KB (348428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af955c30c344b96d47b273fc240431ecb647b6d5e6b5a6db506fd0a46eeda828`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e779905e67487e73a71ba4407c8ecfdf2b013b20d213efb032bd04ad16cca2c1`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4805881421d38e32a8c7790733335e6261d0766591620a2b2ff692b5b1b0a0`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 19.9 MB (19886290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a8cfa1b6a752dcfa395a1f04be70be82b8e3b567e5e5068788dbb471737e3c`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60819df3ae15cadcce13014b660c523cb6b6de908488d5b054f4b3a9847a592b`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4d3e5a621f70aa48fd9ba3cfa11d545e447fb079315c602e625b6f4ceeccb`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4da2eae8290184aea1d6de343a3bd28a09a8797b29e585a267a77fe14ee5df`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 22.3 MB (22346645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9a652976a5b14d3f822b16d23e045465bbe41007f536e9adffe54db8f0687`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d342975a32de3069ec71a8b68ac01b3c48ed4667b43bdfb1184c425c513c7e7c`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864f4aa6948b12f6e4eaebbd858bced5d111337ee7ffc5944059dddbf7145b92`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001844b2a9a1d6bbb6fd855f7437999f2cb31fb9f22815db8a4a9579731e813`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 21.8 MB (21834550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:29a51c17510341c58aee951a685b0a97a446dcafb3f8d94cbd2db3e59a640525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull docker@sha256:1688b4283d6333dc6b062b9725f33e581febe882f118bdaca25c16a43952408c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459681963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a67f4377ec1505bc64fdd5fba308d67690797d25ae8fae2c2abe3a8220b470`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:14:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:14:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:14:12 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:14:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:14:26 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:14:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:14:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:14:38 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:14:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260c6bd48bf9b7bcd23a74ce27f83b531faea9e315ff6737ef884b00bd81da70`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d26d0fae6a860033208ee05de1b45fff21172f23e6c08fcb6c8ddd89a4cf120`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 370.8 KB (370783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e04ee05f729c840466ec7fdbddf08441974dd64583ae57b0c2e1e82888dc02`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a31d3ae72d44e6ac1ba7d34ae1f04a19832141dd6bce84fcc466087f8b56eb`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f75320aa722434dac44791dfa0fc684d4a9118fa6391061b2a6f8101d52a7`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 19.9 MB (19906717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3437ffb66e6fb89a8e52416a38c4e07715674914477817e827340751d33df40`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8902215ab64b3c66d798e6283552def1adaaa91ec7060d2b701324013ff287a5`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a4f89a37a7fcddfc7bba6da9b4f189b05df2f60d049e0deb935afa332f2bd`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e20d43751d763b52f2c66c50dac0f795edac26bd54f2fceebbd844ac18b0`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 22.4 MB (22368711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded394e9a68dc176a9ac6ae87bae98371ce9575ebf52a380abe1c57025a67662`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11948f5717802bd1eaac711e6cdb65cbcaac908f474150dbbd248d948802859`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29097adaffd2b10496a62fdf22ccd89530230ca2141515caec61c5e4cff7d9e`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af02f07dd826ea269773bc614ae42f76d01eec6273637e02431652a26045646`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 21.9 MB (21862437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.1`

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

### `docker:28.1` - linux; amd64

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

### `docker:28.1` - unknown; unknown

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

### `docker:28.1` - linux; arm variant v6

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

### `docker:28.1` - unknown; unknown

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

### `docker:28.1` - linux; arm variant v7

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

### `docker:28.1` - unknown; unknown

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

### `docker:28.1` - linux; arm64 variant v8

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

### `docker:28.1` - unknown; unknown

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

## `docker:28.1-cli`

```console
$ docker pull docker@sha256:23cfbeefc3f4aa9d521bb97e07aff63b9c19eb9f9ba9c32bc8239fbc2b77775b
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

### `docker:28.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:52d88de2357048962588f26d27598908cd1be13d5e0cfa1523793ecb8f32803f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73652948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deb61ad03625c2200c09cad15db296babe3c4062b62bcd8dea55e309e6dacab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bed48dffce491e86191ef39ace19f81a2e044e5401a8d6e8113c30dd908057d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aea4a8d4ac8b8867270838ac3bd213d1c9d134128501dd403ec934bfe16a36e`

```dockerfile
```

-	Layers:
	-	`sha256:f61c57a32213435eba0c6b56580018ac6cfbe388950fbea0037bcc1f54aec289`  
		Last Modified: Thu, 17 Apr 2025 18:27:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:976b17c9d79aadcf387020b276b1620f5578cd5ad57011b1fe492c700cecdb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68611022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf5eb5389a8724919b6ccd89b41c8136d76061e1ea37a46a737e431f20b44c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:03f4c260d41dd0e996485037f1b9ffef9f444f1ca91a61445ba81756e795e8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c20cab2d97bf3bc5fb66556065c08457a53ddb5a5a9968554786cf4a1d00dc`

```dockerfile
```

-	Layers:
	-	`sha256:5d4618616647f7f5308a2b25569464bbbacc5520ceea1774cc737aae46e2edea`  
		Last Modified: Thu, 17 Apr 2025 18:37:40 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:f6b490990228b32d94ae1278f88635fc2e1d93142499ceb34c1fbb85c8380589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67614456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c294c0838b5dd0f46960db67103d333f672db373138f1b3bca47fb8a7dafd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0074b191fefcd2671ee2ef868b889e1c37900ec53186fbd05d3859d701b0194f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0179e3cecec651439cd64ff00de3dd60cb8beb8d33868f2a09806ea1db0f8`

```dockerfile
```

-	Layers:
	-	`sha256:e0b21c112521c52dda1e986c3f5a6db7d546098fe5db90c8fbc5cfe35109abff`  
		Last Modified: Thu, 17 Apr 2025 18:47:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:68303eb35ec3a17a21c305d5abafa4cf56cfb4e0c55995505fbdb04edfe57c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69433624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348b53b676688ea63e108cececef7c952a275896e39c37122f36892a0868391f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:10193cd16309c1c701e67561f2d98cacaeb1901ed358fd016e613384a52eff8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045be3683929bf108fcbd2bf97b6eadad5bac7f3168464e62009e63aa7568182`

```dockerfile
```

-	Layers:
	-	`sha256:bd4fad60791b68af4c6c575d9a4db26bc6009d708c47251c8bd049b8b827b678`  
		Last Modified: Thu, 17 Apr 2025 18:50:48 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.1-dind`

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

### `docker:28.1-dind` - linux; amd64

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

### `docker:28.1-dind` - unknown; unknown

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

### `docker:28.1-dind` - linux; arm variant v6

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

### `docker:28.1-dind` - unknown; unknown

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

### `docker:28.1-dind` - linux; arm variant v7

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

### `docker:28.1-dind` - unknown; unknown

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

### `docker:28.1-dind` - linux; arm64 variant v8

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

### `docker:28.1-dind` - unknown; unknown

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

## `docker:28.1-dind-rootless`

```console
$ docker pull docker@sha256:cfae1360488abdc3ee0dba4fe89420793f34e218e3e1d969f90881eb60f94af1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.1-dind-rootless` - linux; amd64

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

### `docker:28.1-dind-rootless` - unknown; unknown

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

### `docker:28.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:082a0182ac140cfc2d1b3de83637d675af1895a5c0f1844c1dabcae22ea12d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152552323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6899d44cbd6b5d6f55e7bec6805176b66565c9254ccb6fb6dc880be0477d5f`
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
	-	`sha256:ce10ed87a566d0375a64ba19c179459aeae36eede6c6fcc5ecb92628cd8ffdb9`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 1.0 MB (1014220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58c7ebb5111b8ae78ffff6d7b250c03079262ba4a3f4d4b28aa56a133973968`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0d50a20adc69d9af9a41bd1100c27472aa6cbf6f2a160088cab1964906c015`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bd366ce6af6776aae3c1950bb0e9a794d7f48bd180242e76c42efa8c6d3edb`  
		Last Modified: Thu, 17 Apr 2025 20:07:18 GMT  
		Size: 19.3 MB (19275808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ff5a38300abcf02c0d3894bc80f20837030fe834a406bfa591f5f77c28475`  
		Last Modified: Thu, 17 Apr 2025 20:07:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b634773f6d82167e92b3d1179f6bbe6db843825690ede3a80eb2f4e93404bca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a11aff44f1f49258f5942f0dae84df86fbd3e3943ca0e2b6b73aa1a9fb91fe`

```dockerfile
```

-	Layers:
	-	`sha256:54cc39183a3e3de25f55ee17bbc754f7a1e525409795fd4899f4169864704d8d`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.1-windowsservercore`

```console
$ docker pull docker@sha256:429c6cc329d558cde0f693432c7025e2ebd2997e97851488850d34cafdc3d804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `docker:28.1-windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull docker@sha256:1688b4283d6333dc6b062b9725f33e581febe882f118bdaca25c16a43952408c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459681963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a67f4377ec1505bc64fdd5fba308d67690797d25ae8fae2c2abe3a8220b470`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:14:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:14:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:14:12 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:14:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:14:26 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:14:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:14:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:14:38 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:14:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260c6bd48bf9b7bcd23a74ce27f83b531faea9e315ff6737ef884b00bd81da70`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d26d0fae6a860033208ee05de1b45fff21172f23e6c08fcb6c8ddd89a4cf120`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 370.8 KB (370783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e04ee05f729c840466ec7fdbddf08441974dd64583ae57b0c2e1e82888dc02`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a31d3ae72d44e6ac1ba7d34ae1f04a19832141dd6bce84fcc466087f8b56eb`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f75320aa722434dac44791dfa0fc684d4a9118fa6391061b2a6f8101d52a7`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 19.9 MB (19906717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3437ffb66e6fb89a8e52416a38c4e07715674914477817e827340751d33df40`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8902215ab64b3c66d798e6283552def1adaaa91ec7060d2b701324013ff287a5`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a4f89a37a7fcddfc7bba6da9b4f189b05df2f60d049e0deb935afa332f2bd`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e20d43751d763b52f2c66c50dac0f795edac26bd54f2fceebbd844ac18b0`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 22.4 MB (22368711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded394e9a68dc176a9ac6ae87bae98371ce9575ebf52a380abe1c57025a67662`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11948f5717802bd1eaac711e6cdb65cbcaac908f474150dbbd248d948802859`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29097adaffd2b10496a62fdf22ccd89530230ca2141515caec61c5e4cff7d9e`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af02f07dd826ea269773bc614ae42f76d01eec6273637e02431652a26045646`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 21.9 MB (21862437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.1-windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull docker@sha256:995ca0bf38de1f8a0245f2caa155396da4f06cbc594336fb9c76897128890d91
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338010035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe100f55f377339e6d5f4224211c47c2fbb6b253a25fa282fcc1576ced9f558`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:16:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:16:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:16:57 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:16:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:17:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:09 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:17:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:17:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22ed7df539503b8409fa12a12fac0de1ecc8657bd576c4dcad98a9a93f6c3f6`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96fabcddd098deceb4965e2923d655850837faf9387775bb7a3f7347379f68`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 348.4 KB (348428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af955c30c344b96d47b273fc240431ecb647b6d5e6b5a6db506fd0a46eeda828`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e779905e67487e73a71ba4407c8ecfdf2b013b20d213efb032bd04ad16cca2c1`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4805881421d38e32a8c7790733335e6261d0766591620a2b2ff692b5b1b0a0`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 19.9 MB (19886290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a8cfa1b6a752dcfa395a1f04be70be82b8e3b567e5e5068788dbb471737e3c`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60819df3ae15cadcce13014b660c523cb6b6de908488d5b054f4b3a9847a592b`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4d3e5a621f70aa48fd9ba3cfa11d545e447fb079315c602e625b6f4ceeccb`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4da2eae8290184aea1d6de343a3bd28a09a8797b29e585a267a77fe14ee5df`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 22.3 MB (22346645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9a652976a5b14d3f822b16d23e045465bbe41007f536e9adffe54db8f0687`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d342975a32de3069ec71a8b68ac01b3c48ed4667b43bdfb1184c425c513c7e7c`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864f4aa6948b12f6e4eaebbd858bced5d111337ee7ffc5944059dddbf7145b92`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001844b2a9a1d6bbb6fd855f7437999f2cb31fb9f22815db8a4a9579731e813`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 21.8 MB (21834550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.1-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull docker@sha256:76e33dc88f985d1beab4d78f43dd885d456de128945b4a6dd03981c5bb2f35bf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229913583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f586db89c826ee7b52a5ebb6e4f0f9b89a87d4eb2eda2cd54dc67e02c90f1cdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:11:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:11:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:11:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:11:59 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:12:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:12:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:12:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:12:13 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:12:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390143f98317407a20ac29c08b9ec3b59ab9a7cd865888e898464db9e33c4b1e`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230494274935a2d45131a3ae53d73013b524f80b5f1c5c346f361572546c443d`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 337.0 KB (336986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae671c2fb897de70375a2ffd366a9df2ca182b54ee1c98fc04054eed585c852`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b60498a9f6b4d861a2fb43e6765f711d9fc862decf8f6669268f935e417efca`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e96b8a20b826e815d7b12e8b80a6870a6d57fda4040e07e958ecbca9250a7`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 19.9 MB (19878251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a665a369422bcdc54e164d7d15190b072e05a725bd7bb0b71b6e8122238bae0`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ec24a0da078daf54e38f2804f68f22646c0635fd9c07e9666160b6a75e8f3`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841757b89b0ec185e9e9c24a2bbaa990da0810e57f369e5c6e275cade454cd90`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71a487c601cdf1b95461f1d743ce1bc4d360fa55fb753d2c1f87c58987ea79`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 22.3 MB (22339705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd42e2c5ce5fadf18e468bfa810ec1a0a31db7526079ae284b593296a82e09`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f848fd528a82281bfcf00e5773ccdfe2c8f7cd77cab21abcefca9df3a3618626`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfefefef3315a12a85b7a2692ec7f43bd6cf67a23e3f69fdce2f31aa05c339`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b76f6dddb987140c5bd123843c626ccb3c54d67ec2c959df7fc666b6dbc8d`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 21.8 MB (21821032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:326ac27545ba0438a8e7108c0385c6d32985cf8b0949d07389e38b03eed5bc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `docker:28.1-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull docker@sha256:76e33dc88f985d1beab4d78f43dd885d456de128945b4a6dd03981c5bb2f35bf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229913583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f586db89c826ee7b52a5ebb6e4f0f9b89a87d4eb2eda2cd54dc67e02c90f1cdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:11:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:11:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:11:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:11:59 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:12:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:12:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:12:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:12:13 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:12:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390143f98317407a20ac29c08b9ec3b59ab9a7cd865888e898464db9e33c4b1e`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230494274935a2d45131a3ae53d73013b524f80b5f1c5c346f361572546c443d`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 337.0 KB (336986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae671c2fb897de70375a2ffd366a9df2ca182b54ee1c98fc04054eed585c852`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b60498a9f6b4d861a2fb43e6765f711d9fc862decf8f6669268f935e417efca`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e96b8a20b826e815d7b12e8b80a6870a6d57fda4040e07e958ecbca9250a7`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 19.9 MB (19878251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a665a369422bcdc54e164d7d15190b072e05a725bd7bb0b71b6e8122238bae0`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ec24a0da078daf54e38f2804f68f22646c0635fd9c07e9666160b6a75e8f3`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841757b89b0ec185e9e9c24a2bbaa990da0810e57f369e5c6e275cade454cd90`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71a487c601cdf1b95461f1d743ce1bc4d360fa55fb753d2c1f87c58987ea79`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 22.3 MB (22339705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd42e2c5ce5fadf18e468bfa810ec1a0a31db7526079ae284b593296a82e09`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f848fd528a82281bfcf00e5773ccdfe2c8f7cd77cab21abcefca9df3a3618626`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfefefef3315a12a85b7a2692ec7f43bd6cf67a23e3f69fdce2f31aa05c339`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b76f6dddb987140c5bd123843c626ccb3c54d67ec2c959df7fc666b6dbc8d`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 21.8 MB (21821032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:e3e1628d403cdb4880246d886cad700aca6626c1c8e17ddd53df1f649aa4bd85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `docker:28.1-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull docker@sha256:995ca0bf38de1f8a0245f2caa155396da4f06cbc594336fb9c76897128890d91
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338010035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe100f55f377339e6d5f4224211c47c2fbb6b253a25fa282fcc1576ced9f558`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:16:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:16:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:16:57 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:16:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:17:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:09 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:17:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:17:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22ed7df539503b8409fa12a12fac0de1ecc8657bd576c4dcad98a9a93f6c3f6`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96fabcddd098deceb4965e2923d655850837faf9387775bb7a3f7347379f68`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 348.4 KB (348428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af955c30c344b96d47b273fc240431ecb647b6d5e6b5a6db506fd0a46eeda828`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e779905e67487e73a71ba4407c8ecfdf2b013b20d213efb032bd04ad16cca2c1`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4805881421d38e32a8c7790733335e6261d0766591620a2b2ff692b5b1b0a0`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 19.9 MB (19886290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a8cfa1b6a752dcfa395a1f04be70be82b8e3b567e5e5068788dbb471737e3c`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60819df3ae15cadcce13014b660c523cb6b6de908488d5b054f4b3a9847a592b`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4d3e5a621f70aa48fd9ba3cfa11d545e447fb079315c602e625b6f4ceeccb`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4da2eae8290184aea1d6de343a3bd28a09a8797b29e585a267a77fe14ee5df`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 22.3 MB (22346645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9a652976a5b14d3f822b16d23e045465bbe41007f536e9adffe54db8f0687`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d342975a32de3069ec71a8b68ac01b3c48ed4667b43bdfb1184c425c513c7e7c`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864f4aa6948b12f6e4eaebbd858bced5d111337ee7ffc5944059dddbf7145b92`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001844b2a9a1d6bbb6fd855f7437999f2cb31fb9f22815db8a4a9579731e813`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 21.8 MB (21834550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:29a51c17510341c58aee951a685b0a97a446dcafb3f8d94cbd2db3e59a640525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `docker:28.1-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull docker@sha256:1688b4283d6333dc6b062b9725f33e581febe882f118bdaca25c16a43952408c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459681963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a67f4377ec1505bc64fdd5fba308d67690797d25ae8fae2c2abe3a8220b470`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:14:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:14:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:14:12 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:14:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:14:26 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:14:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:14:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:14:38 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:14:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260c6bd48bf9b7bcd23a74ce27f83b531faea9e315ff6737ef884b00bd81da70`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d26d0fae6a860033208ee05de1b45fff21172f23e6c08fcb6c8ddd89a4cf120`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 370.8 KB (370783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e04ee05f729c840466ec7fdbddf08441974dd64583ae57b0c2e1e82888dc02`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a31d3ae72d44e6ac1ba7d34ae1f04a19832141dd6bce84fcc466087f8b56eb`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f75320aa722434dac44791dfa0fc684d4a9118fa6391061b2a6f8101d52a7`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 19.9 MB (19906717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3437ffb66e6fb89a8e52416a38c4e07715674914477817e827340751d33df40`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8902215ab64b3c66d798e6283552def1adaaa91ec7060d2b701324013ff287a5`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a4f89a37a7fcddfc7bba6da9b4f189b05df2f60d049e0deb935afa332f2bd`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e20d43751d763b52f2c66c50dac0f795edac26bd54f2fceebbd844ac18b0`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 22.4 MB (22368711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded394e9a68dc176a9ac6ae87bae98371ce9575ebf52a380abe1c57025a67662`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11948f5717802bd1eaac711e6cdb65cbcaac908f474150dbbd248d948802859`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29097adaffd2b10496a62fdf22ccd89530230ca2141515caec61c5e4cff7d9e`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af02f07dd826ea269773bc614ae42f76d01eec6273637e02431652a26045646`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 21.9 MB (21862437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.1.0`

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

### `docker:28.1.0` - linux; amd64

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

### `docker:28.1.0` - unknown; unknown

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

### `docker:28.1.0` - linux; arm variant v6

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

### `docker:28.1.0` - unknown; unknown

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

### `docker:28.1.0` - linux; arm variant v7

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

### `docker:28.1.0` - unknown; unknown

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

### `docker:28.1.0` - linux; arm64 variant v8

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

### `docker:28.1.0` - unknown; unknown

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

## `docker:28.1.0-alpine3.21`

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

### `docker:28.1.0-alpine3.21` - linux; amd64

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

### `docker:28.1.0-alpine3.21` - unknown; unknown

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

### `docker:28.1.0-alpine3.21` - linux; arm variant v6

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

### `docker:28.1.0-alpine3.21` - unknown; unknown

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

### `docker:28.1.0-alpine3.21` - linux; arm variant v7

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

### `docker:28.1.0-alpine3.21` - unknown; unknown

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

### `docker:28.1.0-alpine3.21` - linux; arm64 variant v8

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

### `docker:28.1.0-alpine3.21` - unknown; unknown

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

## `docker:28.1.0-cli`

```console
$ docker pull docker@sha256:23cfbeefc3f4aa9d521bb97e07aff63b9c19eb9f9ba9c32bc8239fbc2b77775b
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

### `docker:28.1.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:52d88de2357048962588f26d27598908cd1be13d5e0cfa1523793ecb8f32803f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73652948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deb61ad03625c2200c09cad15db296babe3c4062b62bcd8dea55e309e6dacab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.1.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:bed48dffce491e86191ef39ace19f81a2e044e5401a8d6e8113c30dd908057d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aea4a8d4ac8b8867270838ac3bd213d1c9d134128501dd403ec934bfe16a36e`

```dockerfile
```

-	Layers:
	-	`sha256:f61c57a32213435eba0c6b56580018ac6cfbe388950fbea0037bcc1f54aec289`  
		Last Modified: Thu, 17 Apr 2025 18:27:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.1.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:976b17c9d79aadcf387020b276b1620f5578cd5ad57011b1fe492c700cecdb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68611022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf5eb5389a8724919b6ccd89b41c8136d76061e1ea37a46a737e431f20b44c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.1.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:03f4c260d41dd0e996485037f1b9ffef9f444f1ca91a61445ba81756e795e8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c20cab2d97bf3bc5fb66556065c08457a53ddb5a5a9968554786cf4a1d00dc`

```dockerfile
```

-	Layers:
	-	`sha256:5d4618616647f7f5308a2b25569464bbbacc5520ceea1774cc737aae46e2edea`  
		Last Modified: Thu, 17 Apr 2025 18:37:40 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.1.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:f6b490990228b32d94ae1278f88635fc2e1d93142499ceb34c1fbb85c8380589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67614456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c294c0838b5dd0f46960db67103d333f672db373138f1b3bca47fb8a7dafd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.1.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0074b191fefcd2671ee2ef868b889e1c37900ec53186fbd05d3859d701b0194f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0179e3cecec651439cd64ff00de3dd60cb8beb8d33868f2a09806ea1db0f8`

```dockerfile
```

-	Layers:
	-	`sha256:e0b21c112521c52dda1e986c3f5a6db7d546098fe5db90c8fbc5cfe35109abff`  
		Last Modified: Thu, 17 Apr 2025 18:47:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.1.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:68303eb35ec3a17a21c305d5abafa4cf56cfb4e0c55995505fbdb04edfe57c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69433624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348b53b676688ea63e108cececef7c952a275896e39c37122f36892a0868391f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.1.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:10193cd16309c1c701e67561f2d98cacaeb1901ed358fd016e613384a52eff8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045be3683929bf108fcbd2bf97b6eadad5bac7f3168464e62009e63aa7568182`

```dockerfile
```

-	Layers:
	-	`sha256:bd4fad60791b68af4c6c575d9a4db26bc6009d708c47251c8bd049b8b827b678`  
		Last Modified: Thu, 17 Apr 2025 18:50:48 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.1.0-cli-alpine3.21`

```console
$ docker pull docker@sha256:23cfbeefc3f4aa9d521bb97e07aff63b9c19eb9f9ba9c32bc8239fbc2b77775b
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

### `docker:28.1.0-cli-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:52d88de2357048962588f26d27598908cd1be13d5e0cfa1523793ecb8f32803f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73652948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deb61ad03625c2200c09cad15db296babe3c4062b62bcd8dea55e309e6dacab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.1.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:bed48dffce491e86191ef39ace19f81a2e044e5401a8d6e8113c30dd908057d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aea4a8d4ac8b8867270838ac3bd213d1c9d134128501dd403ec934bfe16a36e`

```dockerfile
```

-	Layers:
	-	`sha256:f61c57a32213435eba0c6b56580018ac6cfbe388950fbea0037bcc1f54aec289`  
		Last Modified: Thu, 17 Apr 2025 18:27:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.1.0-cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:976b17c9d79aadcf387020b276b1620f5578cd5ad57011b1fe492c700cecdb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68611022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf5eb5389a8724919b6ccd89b41c8136d76061e1ea37a46a737e431f20b44c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.1.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:03f4c260d41dd0e996485037f1b9ffef9f444f1ca91a61445ba81756e795e8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c20cab2d97bf3bc5fb66556065c08457a53ddb5a5a9968554786cf4a1d00dc`

```dockerfile
```

-	Layers:
	-	`sha256:5d4618616647f7f5308a2b25569464bbbacc5520ceea1774cc737aae46e2edea`  
		Last Modified: Thu, 17 Apr 2025 18:37:40 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.1.0-cli-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:f6b490990228b32d94ae1278f88635fc2e1d93142499ceb34c1fbb85c8380589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67614456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c294c0838b5dd0f46960db67103d333f672db373138f1b3bca47fb8a7dafd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.1.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:0074b191fefcd2671ee2ef868b889e1c37900ec53186fbd05d3859d701b0194f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0179e3cecec651439cd64ff00de3dd60cb8beb8d33868f2a09806ea1db0f8`

```dockerfile
```

-	Layers:
	-	`sha256:e0b21c112521c52dda1e986c3f5a6db7d546098fe5db90c8fbc5cfe35109abff`  
		Last Modified: Thu, 17 Apr 2025 18:47:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.1.0-cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:68303eb35ec3a17a21c305d5abafa4cf56cfb4e0c55995505fbdb04edfe57c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69433624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348b53b676688ea63e108cececef7c952a275896e39c37122f36892a0868391f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:28.1.0-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:10193cd16309c1c701e67561f2d98cacaeb1901ed358fd016e613384a52eff8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045be3683929bf108fcbd2bf97b6eadad5bac7f3168464e62009e63aa7568182`

```dockerfile
```

-	Layers:
	-	`sha256:bd4fad60791b68af4c6c575d9a4db26bc6009d708c47251c8bd049b8b827b678`  
		Last Modified: Thu, 17 Apr 2025 18:50:48 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.1.0-dind`

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

### `docker:28.1.0-dind` - linux; amd64

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

### `docker:28.1.0-dind` - unknown; unknown

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

### `docker:28.1.0-dind` - linux; arm variant v6

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

### `docker:28.1.0-dind` - unknown; unknown

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

### `docker:28.1.0-dind` - linux; arm variant v7

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

### `docker:28.1.0-dind` - unknown; unknown

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

### `docker:28.1.0-dind` - linux; arm64 variant v8

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

### `docker:28.1.0-dind` - unknown; unknown

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

## `docker:28.1.0-dind-alpine3.21`

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

### `docker:28.1.0-dind-alpine3.21` - linux; amd64

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

### `docker:28.1.0-dind-alpine3.21` - unknown; unknown

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

### `docker:28.1.0-dind-alpine3.21` - linux; arm variant v6

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

### `docker:28.1.0-dind-alpine3.21` - unknown; unknown

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

### `docker:28.1.0-dind-alpine3.21` - linux; arm variant v7

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

### `docker:28.1.0-dind-alpine3.21` - unknown; unknown

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

### `docker:28.1.0-dind-alpine3.21` - linux; arm64 variant v8

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

### `docker:28.1.0-dind-alpine3.21` - unknown; unknown

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

## `docker:28.1.0-dind-rootless`

```console
$ docker pull docker@sha256:cfae1360488abdc3ee0dba4fe89420793f34e218e3e1d969f90881eb60f94af1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.1.0-dind-rootless` - linux; amd64

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

### `docker:28.1.0-dind-rootless` - unknown; unknown

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

### `docker:28.1.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:082a0182ac140cfc2d1b3de83637d675af1895a5c0f1844c1dabcae22ea12d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152552323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6899d44cbd6b5d6f55e7bec6805176b66565c9254ccb6fb6dc880be0477d5f`
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
	-	`sha256:ce10ed87a566d0375a64ba19c179459aeae36eede6c6fcc5ecb92628cd8ffdb9`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 1.0 MB (1014220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58c7ebb5111b8ae78ffff6d7b250c03079262ba4a3f4d4b28aa56a133973968`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0d50a20adc69d9af9a41bd1100c27472aa6cbf6f2a160088cab1964906c015`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bd366ce6af6776aae3c1950bb0e9a794d7f48bd180242e76c42efa8c6d3edb`  
		Last Modified: Thu, 17 Apr 2025 20:07:18 GMT  
		Size: 19.3 MB (19275808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ff5a38300abcf02c0d3894bc80f20837030fe834a406bfa591f5f77c28475`  
		Last Modified: Thu, 17 Apr 2025 20:07:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.1.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b634773f6d82167e92b3d1179f6bbe6db843825690ede3a80eb2f4e93404bca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a11aff44f1f49258f5942f0dae84df86fbd3e3943ca0e2b6b73aa1a9fb91fe`

```dockerfile
```

-	Layers:
	-	`sha256:54cc39183a3e3de25f55ee17bbc754f7a1e525409795fd4899f4169864704d8d`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.1.0-windowsservercore`

```console
$ docker pull docker@sha256:429c6cc329d558cde0f693432c7025e2ebd2997e97851488850d34cafdc3d804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `docker:28.1.0-windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull docker@sha256:1688b4283d6333dc6b062b9725f33e581febe882f118bdaca25c16a43952408c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459681963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a67f4377ec1505bc64fdd5fba308d67690797d25ae8fae2c2abe3a8220b470`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:14:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:14:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:14:12 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:14:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:14:26 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:14:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:14:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:14:38 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:14:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260c6bd48bf9b7bcd23a74ce27f83b531faea9e315ff6737ef884b00bd81da70`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d26d0fae6a860033208ee05de1b45fff21172f23e6c08fcb6c8ddd89a4cf120`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 370.8 KB (370783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e04ee05f729c840466ec7fdbddf08441974dd64583ae57b0c2e1e82888dc02`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a31d3ae72d44e6ac1ba7d34ae1f04a19832141dd6bce84fcc466087f8b56eb`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f75320aa722434dac44791dfa0fc684d4a9118fa6391061b2a6f8101d52a7`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 19.9 MB (19906717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3437ffb66e6fb89a8e52416a38c4e07715674914477817e827340751d33df40`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8902215ab64b3c66d798e6283552def1adaaa91ec7060d2b701324013ff287a5`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a4f89a37a7fcddfc7bba6da9b4f189b05df2f60d049e0deb935afa332f2bd`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e20d43751d763b52f2c66c50dac0f795edac26bd54f2fceebbd844ac18b0`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 22.4 MB (22368711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded394e9a68dc176a9ac6ae87bae98371ce9575ebf52a380abe1c57025a67662`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11948f5717802bd1eaac711e6cdb65cbcaac908f474150dbbd248d948802859`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29097adaffd2b10496a62fdf22ccd89530230ca2141515caec61c5e4cff7d9e`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af02f07dd826ea269773bc614ae42f76d01eec6273637e02431652a26045646`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 21.9 MB (21862437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.1.0-windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull docker@sha256:995ca0bf38de1f8a0245f2caa155396da4f06cbc594336fb9c76897128890d91
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338010035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe100f55f377339e6d5f4224211c47c2fbb6b253a25fa282fcc1576ced9f558`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:16:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:16:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:16:57 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:16:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:17:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:09 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:17:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:17:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22ed7df539503b8409fa12a12fac0de1ecc8657bd576c4dcad98a9a93f6c3f6`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96fabcddd098deceb4965e2923d655850837faf9387775bb7a3f7347379f68`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 348.4 KB (348428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af955c30c344b96d47b273fc240431ecb647b6d5e6b5a6db506fd0a46eeda828`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e779905e67487e73a71ba4407c8ecfdf2b013b20d213efb032bd04ad16cca2c1`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4805881421d38e32a8c7790733335e6261d0766591620a2b2ff692b5b1b0a0`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 19.9 MB (19886290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a8cfa1b6a752dcfa395a1f04be70be82b8e3b567e5e5068788dbb471737e3c`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60819df3ae15cadcce13014b660c523cb6b6de908488d5b054f4b3a9847a592b`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4d3e5a621f70aa48fd9ba3cfa11d545e447fb079315c602e625b6f4ceeccb`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4da2eae8290184aea1d6de343a3bd28a09a8797b29e585a267a77fe14ee5df`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 22.3 MB (22346645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9a652976a5b14d3f822b16d23e045465bbe41007f536e9adffe54db8f0687`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d342975a32de3069ec71a8b68ac01b3c48ed4667b43bdfb1184c425c513c7e7c`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864f4aa6948b12f6e4eaebbd858bced5d111337ee7ffc5944059dddbf7145b92`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001844b2a9a1d6bbb6fd855f7437999f2cb31fb9f22815db8a4a9579731e813`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 21.8 MB (21834550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.1.0-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull docker@sha256:76e33dc88f985d1beab4d78f43dd885d456de128945b4a6dd03981c5bb2f35bf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229913583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f586db89c826ee7b52a5ebb6e4f0f9b89a87d4eb2eda2cd54dc67e02c90f1cdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:11:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:11:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:11:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:11:59 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:12:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:12:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:12:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:12:13 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:12:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390143f98317407a20ac29c08b9ec3b59ab9a7cd865888e898464db9e33c4b1e`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230494274935a2d45131a3ae53d73013b524f80b5f1c5c346f361572546c443d`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 337.0 KB (336986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae671c2fb897de70375a2ffd366a9df2ca182b54ee1c98fc04054eed585c852`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b60498a9f6b4d861a2fb43e6765f711d9fc862decf8f6669268f935e417efca`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e96b8a20b826e815d7b12e8b80a6870a6d57fda4040e07e958ecbca9250a7`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 19.9 MB (19878251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a665a369422bcdc54e164d7d15190b072e05a725bd7bb0b71b6e8122238bae0`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ec24a0da078daf54e38f2804f68f22646c0635fd9c07e9666160b6a75e8f3`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841757b89b0ec185e9e9c24a2bbaa990da0810e57f369e5c6e275cade454cd90`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71a487c601cdf1b95461f1d743ce1bc4d360fa55fb753d2c1f87c58987ea79`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 22.3 MB (22339705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd42e2c5ce5fadf18e468bfa810ec1a0a31db7526079ae284b593296a82e09`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f848fd528a82281bfcf00e5773ccdfe2c8f7cd77cab21abcefca9df3a3618626`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfefefef3315a12a85b7a2692ec7f43bd6cf67a23e3f69fdce2f31aa05c339`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b76f6dddb987140c5bd123843c626ccb3c54d67ec2c959df7fc666b6dbc8d`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 21.8 MB (21821032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.1.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:326ac27545ba0438a8e7108c0385c6d32985cf8b0949d07389e38b03eed5bc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `docker:28.1.0-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull docker@sha256:76e33dc88f985d1beab4d78f43dd885d456de128945b4a6dd03981c5bb2f35bf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229913583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f586db89c826ee7b52a5ebb6e4f0f9b89a87d4eb2eda2cd54dc67e02c90f1cdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:11:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:11:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:11:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:11:59 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:12:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:12:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:12:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:12:13 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:12:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390143f98317407a20ac29c08b9ec3b59ab9a7cd865888e898464db9e33c4b1e`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230494274935a2d45131a3ae53d73013b524f80b5f1c5c346f361572546c443d`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 337.0 KB (336986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae671c2fb897de70375a2ffd366a9df2ca182b54ee1c98fc04054eed585c852`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b60498a9f6b4d861a2fb43e6765f711d9fc862decf8f6669268f935e417efca`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e96b8a20b826e815d7b12e8b80a6870a6d57fda4040e07e958ecbca9250a7`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 19.9 MB (19878251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a665a369422bcdc54e164d7d15190b072e05a725bd7bb0b71b6e8122238bae0`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ec24a0da078daf54e38f2804f68f22646c0635fd9c07e9666160b6a75e8f3`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841757b89b0ec185e9e9c24a2bbaa990da0810e57f369e5c6e275cade454cd90`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71a487c601cdf1b95461f1d743ce1bc4d360fa55fb753d2c1f87c58987ea79`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 22.3 MB (22339705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd42e2c5ce5fadf18e468bfa810ec1a0a31db7526079ae284b593296a82e09`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f848fd528a82281bfcf00e5773ccdfe2c8f7cd77cab21abcefca9df3a3618626`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfefefef3315a12a85b7a2692ec7f43bd6cf67a23e3f69fdce2f31aa05c339`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b76f6dddb987140c5bd123843c626ccb3c54d67ec2c959df7fc666b6dbc8d`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 21.8 MB (21821032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.1.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:e3e1628d403cdb4880246d886cad700aca6626c1c8e17ddd53df1f649aa4bd85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `docker:28.1.0-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull docker@sha256:995ca0bf38de1f8a0245f2caa155396da4f06cbc594336fb9c76897128890d91
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338010035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe100f55f377339e6d5f4224211c47c2fbb6b253a25fa282fcc1576ced9f558`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:16:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:16:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:16:57 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:16:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:17:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:09 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:17:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:17:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22ed7df539503b8409fa12a12fac0de1ecc8657bd576c4dcad98a9a93f6c3f6`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96fabcddd098deceb4965e2923d655850837faf9387775bb7a3f7347379f68`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 348.4 KB (348428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af955c30c344b96d47b273fc240431ecb647b6d5e6b5a6db506fd0a46eeda828`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e779905e67487e73a71ba4407c8ecfdf2b013b20d213efb032bd04ad16cca2c1`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4805881421d38e32a8c7790733335e6261d0766591620a2b2ff692b5b1b0a0`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 19.9 MB (19886290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a8cfa1b6a752dcfa395a1f04be70be82b8e3b567e5e5068788dbb471737e3c`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60819df3ae15cadcce13014b660c523cb6b6de908488d5b054f4b3a9847a592b`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4d3e5a621f70aa48fd9ba3cfa11d545e447fb079315c602e625b6f4ceeccb`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4da2eae8290184aea1d6de343a3bd28a09a8797b29e585a267a77fe14ee5df`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 22.3 MB (22346645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9a652976a5b14d3f822b16d23e045465bbe41007f536e9adffe54db8f0687`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d342975a32de3069ec71a8b68ac01b3c48ed4667b43bdfb1184c425c513c7e7c`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864f4aa6948b12f6e4eaebbd858bced5d111337ee7ffc5944059dddbf7145b92`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001844b2a9a1d6bbb6fd855f7437999f2cb31fb9f22815db8a4a9579731e813`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 21.8 MB (21834550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.1.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:29a51c17510341c58aee951a685b0a97a446dcafb3f8d94cbd2db3e59a640525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `docker:28.1.0-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull docker@sha256:1688b4283d6333dc6b062b9725f33e581febe882f118bdaca25c16a43952408c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459681963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a67f4377ec1505bc64fdd5fba308d67690797d25ae8fae2c2abe3a8220b470`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:14:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:14:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:14:12 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:14:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:14:26 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:14:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:14:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:14:38 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:14:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260c6bd48bf9b7bcd23a74ce27f83b531faea9e315ff6737ef884b00bd81da70`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d26d0fae6a860033208ee05de1b45fff21172f23e6c08fcb6c8ddd89a4cf120`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 370.8 KB (370783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e04ee05f729c840466ec7fdbddf08441974dd64583ae57b0c2e1e82888dc02`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a31d3ae72d44e6ac1ba7d34ae1f04a19832141dd6bce84fcc466087f8b56eb`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f75320aa722434dac44791dfa0fc684d4a9118fa6391061b2a6f8101d52a7`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 19.9 MB (19906717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3437ffb66e6fb89a8e52416a38c4e07715674914477817e827340751d33df40`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8902215ab64b3c66d798e6283552def1adaaa91ec7060d2b701324013ff287a5`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a4f89a37a7fcddfc7bba6da9b4f189b05df2f60d049e0deb935afa332f2bd`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e20d43751d763b52f2c66c50dac0f795edac26bd54f2fceebbd844ac18b0`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 22.4 MB (22368711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded394e9a68dc176a9ac6ae87bae98371ce9575ebf52a380abe1c57025a67662`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11948f5717802bd1eaac711e6cdb65cbcaac908f474150dbbd248d948802859`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29097adaffd2b10496a62fdf22ccd89530230ca2141515caec61c5e4cff7d9e`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af02f07dd826ea269773bc614ae42f76d01eec6273637e02431652a26045646`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 21.9 MB (21862437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:23cfbeefc3f4aa9d521bb97e07aff63b9c19eb9f9ba9c32bc8239fbc2b77775b
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

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:52d88de2357048962588f26d27598908cd1be13d5e0cfa1523793ecb8f32803f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73652948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deb61ad03625c2200c09cad15db296babe3c4062b62bcd8dea55e309e6dacab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:bed48dffce491e86191ef39ace19f81a2e044e5401a8d6e8113c30dd908057d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aea4a8d4ac8b8867270838ac3bd213d1c9d134128501dd403ec934bfe16a36e`

```dockerfile
```

-	Layers:
	-	`sha256:f61c57a32213435eba0c6b56580018ac6cfbe388950fbea0037bcc1f54aec289`  
		Last Modified: Thu, 17 Apr 2025 18:27:37 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:976b17c9d79aadcf387020b276b1620f5578cd5ad57011b1fe492c700cecdb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68611022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf5eb5389a8724919b6ccd89b41c8136d76061e1ea37a46a737e431f20b44c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:03f4c260d41dd0e996485037f1b9ffef9f444f1ca91a61445ba81756e795e8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c20cab2d97bf3bc5fb66556065c08457a53ddb5a5a9968554786cf4a1d00dc`

```dockerfile
```

-	Layers:
	-	`sha256:5d4618616647f7f5308a2b25569464bbbacc5520ceea1774cc737aae46e2edea`  
		Last Modified: Thu, 17 Apr 2025 18:37:40 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:f6b490990228b32d94ae1278f88635fc2e1d93142499ceb34c1fbb85c8380589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67614456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c294c0838b5dd0f46960db67103d333f672db373138f1b3bca47fb8a7dafd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:0074b191fefcd2671ee2ef868b889e1c37900ec53186fbd05d3859d701b0194f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0179e3cecec651439cd64ff00de3dd60cb8beb8d33868f2a09806ea1db0f8`

```dockerfile
```

-	Layers:
	-	`sha256:e0b21c112521c52dda1e986c3f5a6db7d546098fe5db90c8fbc5cfe35109abff`  
		Last Modified: Thu, 17 Apr 2025 18:47:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:68303eb35ec3a17a21c305d5abafa4cf56cfb4e0c55995505fbdb04edfe57c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69433624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348b53b676688ea63e108cececef7c952a275896e39c37122f36892a0868391f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:10193cd16309c1c701e67561f2d98cacaeb1901ed358fd016e613384a52eff8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045be3683929bf108fcbd2bf97b6eadad5bac7f3168464e62009e63aa7568182`

```dockerfile
```

-	Layers:
	-	`sha256:bd4fad60791b68af4c6c575d9a4db26bc6009d708c47251c8bd049b8b827b678`  
		Last Modified: Thu, 17 Apr 2025 18:50:48 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

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

### `docker:dind` - linux; amd64

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

### `docker:dind` - unknown; unknown

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

### `docker:dind` - linux; arm variant v6

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

### `docker:dind` - unknown; unknown

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

### `docker:dind` - linux; arm variant v7

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

### `docker:dind` - unknown; unknown

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

### `docker:dind` - linux; arm64 variant v8

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

### `docker:dind` - unknown; unknown

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

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:cfae1360488abdc3ee0dba4fe89420793f34e218e3e1d969f90881eb60f94af1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

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

### `docker:dind-rootless` - unknown; unknown

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

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:082a0182ac140cfc2d1b3de83637d675af1895a5c0f1844c1dabcae22ea12d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152552323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6899d44cbd6b5d6f55e7bec6805176b66565c9254ccb6fb6dc880be0477d5f`
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
	-	`sha256:ce10ed87a566d0375a64ba19c179459aeae36eede6c6fcc5ecb92628cd8ffdb9`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 1.0 MB (1014220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58c7ebb5111b8ae78ffff6d7b250c03079262ba4a3f4d4b28aa56a133973968`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0d50a20adc69d9af9a41bd1100c27472aa6cbf6f2a160088cab1964906c015`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bd366ce6af6776aae3c1950bb0e9a794d7f48bd180242e76c42efa8c6d3edb`  
		Last Modified: Thu, 17 Apr 2025 20:07:18 GMT  
		Size: 19.3 MB (19275808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ff5a38300abcf02c0d3894bc80f20837030fe834a406bfa591f5f77c28475`  
		Last Modified: Thu, 17 Apr 2025 20:07:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b634773f6d82167e92b3d1179f6bbe6db843825690ede3a80eb2f4e93404bca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a11aff44f1f49258f5942f0dae84df86fbd3e3943ca0e2b6b73aa1a9fb91fe`

```dockerfile
```

-	Layers:
	-	`sha256:54cc39183a3e3de25f55ee17bbc754f7a1e525409795fd4899f4169864704d8d`  
		Last Modified: Thu, 17 Apr 2025 20:07:17 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json

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

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:429c6cc329d558cde0f693432c7025e2ebd2997e97851488850d34cafdc3d804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull docker@sha256:1688b4283d6333dc6b062b9725f33e581febe882f118bdaca25c16a43952408c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459681963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a67f4377ec1505bc64fdd5fba308d67690797d25ae8fae2c2abe3a8220b470`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:14:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:14:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:14:12 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:14:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:14:26 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:14:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:14:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:14:38 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:14:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260c6bd48bf9b7bcd23a74ce27f83b531faea9e315ff6737ef884b00bd81da70`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d26d0fae6a860033208ee05de1b45fff21172f23e6c08fcb6c8ddd89a4cf120`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 370.8 KB (370783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e04ee05f729c840466ec7fdbddf08441974dd64583ae57b0c2e1e82888dc02`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a31d3ae72d44e6ac1ba7d34ae1f04a19832141dd6bce84fcc466087f8b56eb`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f75320aa722434dac44791dfa0fc684d4a9118fa6391061b2a6f8101d52a7`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 19.9 MB (19906717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3437ffb66e6fb89a8e52416a38c4e07715674914477817e827340751d33df40`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8902215ab64b3c66d798e6283552def1adaaa91ec7060d2b701324013ff287a5`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a4f89a37a7fcddfc7bba6da9b4f189b05df2f60d049e0deb935afa332f2bd`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e20d43751d763b52f2c66c50dac0f795edac26bd54f2fceebbd844ac18b0`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 22.4 MB (22368711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded394e9a68dc176a9ac6ae87bae98371ce9575ebf52a380abe1c57025a67662`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11948f5717802bd1eaac711e6cdb65cbcaac908f474150dbbd248d948802859`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29097adaffd2b10496a62fdf22ccd89530230ca2141515caec61c5e4cff7d9e`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af02f07dd826ea269773bc614ae42f76d01eec6273637e02431652a26045646`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 21.9 MB (21862437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull docker@sha256:995ca0bf38de1f8a0245f2caa155396da4f06cbc594336fb9c76897128890d91
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338010035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe100f55f377339e6d5f4224211c47c2fbb6b253a25fa282fcc1576ced9f558`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:16:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:16:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:16:57 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:16:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:17:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:09 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:17:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:17:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22ed7df539503b8409fa12a12fac0de1ecc8657bd576c4dcad98a9a93f6c3f6`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96fabcddd098deceb4965e2923d655850837faf9387775bb7a3f7347379f68`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 348.4 KB (348428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af955c30c344b96d47b273fc240431ecb647b6d5e6b5a6db506fd0a46eeda828`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e779905e67487e73a71ba4407c8ecfdf2b013b20d213efb032bd04ad16cca2c1`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4805881421d38e32a8c7790733335e6261d0766591620a2b2ff692b5b1b0a0`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 19.9 MB (19886290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a8cfa1b6a752dcfa395a1f04be70be82b8e3b567e5e5068788dbb471737e3c`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60819df3ae15cadcce13014b660c523cb6b6de908488d5b054f4b3a9847a592b`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4d3e5a621f70aa48fd9ba3cfa11d545e447fb079315c602e625b6f4ceeccb`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4da2eae8290184aea1d6de343a3bd28a09a8797b29e585a267a77fe14ee5df`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 22.3 MB (22346645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9a652976a5b14d3f822b16d23e045465bbe41007f536e9adffe54db8f0687`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d342975a32de3069ec71a8b68ac01b3c48ed4667b43bdfb1184c425c513c7e7c`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864f4aa6948b12f6e4eaebbd858bced5d111337ee7ffc5944059dddbf7145b92`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001844b2a9a1d6bbb6fd855f7437999f2cb31fb9f22815db8a4a9579731e813`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 21.8 MB (21834550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull docker@sha256:76e33dc88f985d1beab4d78f43dd885d456de128945b4a6dd03981c5bb2f35bf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229913583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f586db89c826ee7b52a5ebb6e4f0f9b89a87d4eb2eda2cd54dc67e02c90f1cdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:11:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:11:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:11:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:11:59 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:12:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:12:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:12:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:12:13 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:12:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390143f98317407a20ac29c08b9ec3b59ab9a7cd865888e898464db9e33c4b1e`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230494274935a2d45131a3ae53d73013b524f80b5f1c5c346f361572546c443d`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 337.0 KB (336986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae671c2fb897de70375a2ffd366a9df2ca182b54ee1c98fc04054eed585c852`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b60498a9f6b4d861a2fb43e6765f711d9fc862decf8f6669268f935e417efca`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e96b8a20b826e815d7b12e8b80a6870a6d57fda4040e07e958ecbca9250a7`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 19.9 MB (19878251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a665a369422bcdc54e164d7d15190b072e05a725bd7bb0b71b6e8122238bae0`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ec24a0da078daf54e38f2804f68f22646c0635fd9c07e9666160b6a75e8f3`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841757b89b0ec185e9e9c24a2bbaa990da0810e57f369e5c6e275cade454cd90`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71a487c601cdf1b95461f1d743ce1bc4d360fa55fb753d2c1f87c58987ea79`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 22.3 MB (22339705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd42e2c5ce5fadf18e468bfa810ec1a0a31db7526079ae284b593296a82e09`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f848fd528a82281bfcf00e5773ccdfe2c8f7cd77cab21abcefca9df3a3618626`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfefefef3315a12a85b7a2692ec7f43bd6cf67a23e3f69fdce2f31aa05c339`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b76f6dddb987140c5bd123843c626ccb3c54d67ec2c959df7fc666b6dbc8d`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 21.8 MB (21821032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:326ac27545ba0438a8e7108c0385c6d32985cf8b0949d07389e38b03eed5bc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull docker@sha256:76e33dc88f985d1beab4d78f43dd885d456de128945b4a6dd03981c5bb2f35bf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229913583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f586db89c826ee7b52a5ebb6e4f0f9b89a87d4eb2eda2cd54dc67e02c90f1cdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:11:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:11:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:11:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:11:59 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:12:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:12:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:12:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:12:13 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:12:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390143f98317407a20ac29c08b9ec3b59ab9a7cd865888e898464db9e33c4b1e`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230494274935a2d45131a3ae53d73013b524f80b5f1c5c346f361572546c443d`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 337.0 KB (336986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae671c2fb897de70375a2ffd366a9df2ca182b54ee1c98fc04054eed585c852`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b60498a9f6b4d861a2fb43e6765f711d9fc862decf8f6669268f935e417efca`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e96b8a20b826e815d7b12e8b80a6870a6d57fda4040e07e958ecbca9250a7`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 19.9 MB (19878251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a665a369422bcdc54e164d7d15190b072e05a725bd7bb0b71b6e8122238bae0`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ec24a0da078daf54e38f2804f68f22646c0635fd9c07e9666160b6a75e8f3`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841757b89b0ec185e9e9c24a2bbaa990da0810e57f369e5c6e275cade454cd90`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71a487c601cdf1b95461f1d743ce1bc4d360fa55fb753d2c1f87c58987ea79`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 22.3 MB (22339705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd42e2c5ce5fadf18e468bfa810ec1a0a31db7526079ae284b593296a82e09`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f848fd528a82281bfcf00e5773ccdfe2c8f7cd77cab21abcefca9df3a3618626`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfefefef3315a12a85b7a2692ec7f43bd6cf67a23e3f69fdce2f31aa05c339`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b76f6dddb987140c5bd123843c626ccb3c54d67ec2c959df7fc666b6dbc8d`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 21.8 MB (21821032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:e3e1628d403cdb4880246d886cad700aca6626c1c8e17ddd53df1f649aa4bd85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull docker@sha256:995ca0bf38de1f8a0245f2caa155396da4f06cbc594336fb9c76897128890d91
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338010035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe100f55f377339e6d5f4224211c47c2fbb6b253a25fa282fcc1576ced9f558`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:16:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:16:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:16:57 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:16:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:17:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:09 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:17:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:17:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22ed7df539503b8409fa12a12fac0de1ecc8657bd576c4dcad98a9a93f6c3f6`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96fabcddd098deceb4965e2923d655850837faf9387775bb7a3f7347379f68`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 348.4 KB (348428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af955c30c344b96d47b273fc240431ecb647b6d5e6b5a6db506fd0a46eeda828`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e779905e67487e73a71ba4407c8ecfdf2b013b20d213efb032bd04ad16cca2c1`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4805881421d38e32a8c7790733335e6261d0766591620a2b2ff692b5b1b0a0`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 19.9 MB (19886290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a8cfa1b6a752dcfa395a1f04be70be82b8e3b567e5e5068788dbb471737e3c`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60819df3ae15cadcce13014b660c523cb6b6de908488d5b054f4b3a9847a592b`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4d3e5a621f70aa48fd9ba3cfa11d545e447fb079315c602e625b6f4ceeccb`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4da2eae8290184aea1d6de343a3bd28a09a8797b29e585a267a77fe14ee5df`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 22.3 MB (22346645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9a652976a5b14d3f822b16d23e045465bbe41007f536e9adffe54db8f0687`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d342975a32de3069ec71a8b68ac01b3c48ed4667b43bdfb1184c425c513c7e7c`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864f4aa6948b12f6e4eaebbd858bced5d111337ee7ffc5944059dddbf7145b92`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001844b2a9a1d6bbb6fd855f7437999f2cb31fb9f22815db8a4a9579731e813`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 21.8 MB (21834550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:29a51c17510341c58aee951a685b0a97a446dcafb3f8d94cbd2db3e59a640525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull docker@sha256:1688b4283d6333dc6b062b9725f33e581febe882f118bdaca25c16a43952408c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459681963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a67f4377ec1505bc64fdd5fba308d67690797d25ae8fae2c2abe3a8220b470`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:14:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:14:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:14:12 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:14:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:14:26 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:14:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:14:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:14:38 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:14:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260c6bd48bf9b7bcd23a74ce27f83b531faea9e315ff6737ef884b00bd81da70`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d26d0fae6a860033208ee05de1b45fff21172f23e6c08fcb6c8ddd89a4cf120`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 370.8 KB (370783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e04ee05f729c840466ec7fdbddf08441974dd64583ae57b0c2e1e82888dc02`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a31d3ae72d44e6ac1ba7d34ae1f04a19832141dd6bce84fcc466087f8b56eb`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f75320aa722434dac44791dfa0fc684d4a9118fa6391061b2a6f8101d52a7`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 19.9 MB (19906717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3437ffb66e6fb89a8e52416a38c4e07715674914477817e827340751d33df40`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8902215ab64b3c66d798e6283552def1adaaa91ec7060d2b701324013ff287a5`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a4f89a37a7fcddfc7bba6da9b4f189b05df2f60d049e0deb935afa332f2bd`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e20d43751d763b52f2c66c50dac0f795edac26bd54f2fceebbd844ac18b0`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 22.4 MB (22368711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded394e9a68dc176a9ac6ae87bae98371ce9575ebf52a380abe1c57025a67662`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11948f5717802bd1eaac711e6cdb65cbcaac908f474150dbbd248d948802859`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29097adaffd2b10496a62fdf22ccd89530230ca2141515caec61c5e4cff7d9e`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af02f07dd826ea269773bc614ae42f76d01eec6273637e02431652a26045646`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 21.9 MB (21862437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

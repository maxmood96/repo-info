<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.1`](#docker291)
-	[`docker:29.1-cli`](#docker291-cli)
-	[`docker:29.1-dind`](#docker291-dind)
-	[`docker:29.1-dind-rootless`](#docker291-dind-rootless)
-	[`docker:29.1-windowsservercore`](#docker291-windowsservercore)
-	[`docker:29.1-windowsservercore-ltsc2022`](#docker291-windowsservercore-ltsc2022)
-	[`docker:29.1-windowsservercore-ltsc2025`](#docker291-windowsservercore-ltsc2025)
-	[`docker:29.1.2`](#docker2912)
-	[`docker:29.1.2-alpine3.22`](#docker2912-alpine322)
-	[`docker:29.1.2-cli`](#docker2912-cli)
-	[`docker:29.1.2-cli-alpine3.22`](#docker2912-cli-alpine322)
-	[`docker:29.1.2-dind`](#docker2912-dind)
-	[`docker:29.1.2-dind-alpine3.22`](#docker2912-dind-alpine322)
-	[`docker:29.1.2-dind-rootless`](#docker2912-dind-rootless)
-	[`docker:29.1.2-windowsservercore`](#docker2912-windowsservercore)
-	[`docker:29.1.2-windowsservercore-ltsc2022`](#docker2912-windowsservercore-ltsc2022)
-	[`docker:29.1.2-windowsservercore-ltsc2025`](#docker2912-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:9b20eb23e1f0443655673efb9db76c4b18cc1b45de1fcf82b3c1b749b9647bdf
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

### `docker:29` - linux; amd64

```console
$ docker pull docker@sha256:e7722a3fdf461a91095cc11b6751da7e69a1bdd583df23b5837cd03bc3dcbf11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146834840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3d6683ede5a5e31409999791e15e1785c65344da6483593dd3af23c29bd562`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:08:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:07 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:35:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:35:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:35:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:35:13 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bca2c07d80098fe1c61e0aa26eac435752d6dca6a2d3837735a2f68eedd27f`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 8.2 MB (8232306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c13c6aae9df8eeb1b8fe904cbdc67165e49d9f6ca682577bdee0ff1fddb0e`  
		Last Modified: Tue, 02 Dec 2025 00:08:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbba1101f59cdf058694512346b7fb8aeda578243290fc893ba55d81ac314cd`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 18.8 MB (18762388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc6a25ab2f1cc6386ed9595b9c99245b984bddba79a401ede272b40c8a1d34`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3786f9aa3c17d408a9f2162d158dcac195becac82c72ee0a4b29c43f52649`  
		Last Modified: Tue, 02 Dec 2025 00:08:43 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de8d894975036d476ad31205669d2600d672441a0b78b3d35650f89daf8774`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8318820339c402ec6f7161ee23642657be448d0298de2ca2a4946643e99bf`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fca41ae3f7f0a9e8364572b85d6e7862b0a01a49813320a77b7cca46a3dc67`  
		Last Modified: Tue, 02 Dec 2025 00:08:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eaeb7e3ff54863b596ddf45aa1f53fe06b5bac153cd3057038bca861e20c27`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 6.9 MB (6905410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568debdaab006707818488bd30ccbe9d028b275d05c6ce65dd3b1aec6ecdd841`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6f1c21ebbe286ed54f5e70396d9124048a5aab0e142aa1b81824ff82ace94`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b638749a1ad920d398a23428bd3e49a14bdf1b01a65776444264fa6afec6effd`  
		Last Modified: Tue, 02 Dec 2025 00:36:12 GMT  
		Size: 64.4 MB (64383976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4c76068297a0e5e2b8b3f4b582b62ec0bd167377a14e5e849d084838dd7d65`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831f7baf80344c1ea02c8259ab473f8c112481bf3ba30f27311a27ae615a6ba9`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:b3ffbc635daa4785c6e8540daa89e290342d9ce7574d182f603904c844e2ae55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cddfa71d427c6ffde929b85b3ac597a723b864fa7b755fb7e2b38bffcec4abf`

```dockerfile
```

-	Layers:
	-	`sha256:c293678f6e88a59d70f255b8b2d4d5370350c49c9cac522deee7e1ca928a771f`  
		Last Modified: Tue, 02 Dec 2025 03:08:05 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:f4264dc6f53bf84c143abcd79f054061e949f91297519b16342df3b0fcf515d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138377571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5525feeb0b6b1996748694f01b24cce0d9825880fcc090ceaec227482995adb8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:00:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:01:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:01:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:01:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:01:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:03 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:08:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:08:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:08:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:08:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:08:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:08:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:47 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd90142670bbaed6f585f4970fd1d53633e0869fd5272c8e3df77120bace0e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 8.1 MB (8140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642374c76164440ef8b823ab6bba0dd1bee0e2a2376c47bb5f4073a585413e04`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed115a71dbefda1db4593399cccc8dad9b72d92954e97811cb17ea6cbd16029`  
		Last Modified: Tue, 02 Dec 2025 00:01:24 GMT  
		Size: 17.6 MB (17559034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5443b6b267bcc407b81aa1fc56c89a28780986fdb8a6a0e262dc6cb167368cb`  
		Last Modified: Tue, 02 Dec 2025 00:01:23 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1408d4a896b763e6cf9b6eb5321ee325d093c04ddb275e901a85d57735dd87d`  
		Last Modified: Tue, 02 Dec 2025 00:01:21 GMT  
		Size: 20.5 MB (20480374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc905b6a443c6c8096533c447544d946dedb7a2450e9d8815424d25a2b70b5b8`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79661a927ae816f329cd8e6d5aebc5775b45d598f860218a7fa0bf34259fedae`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc8f4aa5c2b729f00263aa5f33b190bedfd7d94a05ac9ccb26f4f1995d10a1e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f114e86733f934e05b8cc095e26ac7d23df0400c164367a5d0960c90ffbb7e7`  
		Last Modified: Tue, 02 Dec 2025 00:09:22 GMT  
		Size: 7.2 MB (7230316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52de536e5339daea653f15c27e78b4cf16e12a10d82ef4f286872bc4f4aafd9`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 90.0 KB (89961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae860099f824f4d5c845c472dccead8faa86f1afc2773e064de55ac8317fa514`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99458a7fe0e1036a55a30274f0e06e8baa5da805dac7a2d7f788bf02c9531c18`  
		Last Modified: Tue, 02 Dec 2025 00:09:30 GMT  
		Size: 59.9 MB (59888589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bba7682b037f71b8aea88b0676d075b4bcd35fa3390b95b1bd864d4999afb7d`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed47c75bfd062f331a396b716966fb250ee7485fee132a7b2942e732842fbf3`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:ec56f63d4804233c364f31addc653c748a9b7e58cc1b72a68562b7cfd4f5869d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3125bbdfa07949727984336157b0367e420ed260fb1153f6a4ac86374835df20`

```dockerfile
```

-	Layers:
	-	`sha256:e35660952afa463bcd149750757d217195b0afeb78547aeae6aecaf7697b4b82`  
		Last Modified: Tue, 02 Dec 2025 03:08:08 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:4c9e1d32783f3091ec573930696e1a02680c8b2e0a96588960e8cfb4785f0987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136499855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a132a67d9b1e15c2a6b6b5072baf4669d91a4c94c59594cde5e134a3f13f7e0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:03:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:03:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:03:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:03:35 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:08:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:08:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:08:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:08:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:08:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:08:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:52 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec0784ecb867af52b79e3f383d52e39182464803fd28c22d49d1ff019df6e4`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 7.5 MB (7461368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491247472d55430402882837b71580b20d49d688f85f713917e74b9c4dcfa29`  
		Last Modified: Tue, 02 Dec 2025 00:03:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681ac3424d8a722d9e60118306e4292f0558f8234066431fcf35fe24394a1bb8`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 17.6 MB (17550851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4ccba3516b05ed1ea12fcc5ff93f84c20331f6098765bc58aa14342452b044`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01cc08290b32581069106ced2f3f3eb8ee944803bea261cb440c95a59f3e88`  
		Last Modified: Tue, 02 Dec 2025 00:03:52 GMT  
		Size: 20.5 MB (20462776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3320b40de969faa831b8c731ba2d0e1b46c0099f07df033d271e79b3ae90cfa`  
		Last Modified: Tue, 02 Dec 2025 00:03:49 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6f871522091994e48824cf572b17680f5f65920875e93a33820ca79643cb83`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccd637b5bd3f36088e619e2cd9af1073d6cf18b4daae90c18da0bebaac04039`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fedb293900f104824c5bf607d49531816ebb696de67d2349e25c3b7235c7d4`  
		Last Modified: Tue, 02 Dec 2025 03:08:37 GMT  
		Size: 6.5 MB (6538170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f3efb3e0b8e692ee930467452c2b90850e32de6e81f525c8b5ecb809596cb1`  
		Last Modified: Tue, 02 Dec 2025 01:10:44 GMT  
		Size: 86.4 KB (86397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6a05cebb7258e8cc03a59c4ddbfab058b79a4254d47f5f7339c3cbb66e0f91`  
		Last Modified: Tue, 02 Dec 2025 01:10:45 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2700c9375899dc20256cee56347f7a94685712635d0a083c74baf5a4d0ac5809`  
		Last Modified: Tue, 02 Dec 2025 03:08:48 GMT  
		Size: 59.7 MB (59715683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f83379703e2b0dd6765daef6f82dba3e582ae979b57dfd62b9101c915e244`  
		Last Modified: Tue, 02 Dec 2025 01:10:48 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fb0afbbc9ea4bc8903a6671f34110ef481952a81c388cc585e9b21cd7f4e21`  
		Last Modified: Tue, 02 Dec 2025 01:10:44 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:81b93d08f8b08b14411acfcfd4683554ff94f1553aa1c42bb33bb2e43d453ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db32ac5181c3e6cf95fea47b5846cd4a761768ec6dc895055994af29bcb7718b`

```dockerfile
```

-	Layers:
	-	`sha256:9f6b2982982b5b6659faac06d4632eb9f834c5522239d5ab3c1c0c340c2664f7`  
		Last Modified: Tue, 02 Dec 2025 03:08:11 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:37269ed2d81f5f6d65910acc46f07807e7027efa4560c03b5c2c427c57b5b99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135915031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cb9c89488e9663f2162c6982870ff63ce946066edbedbf787cccfcb650d4a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:02:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:02:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:02:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:02:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:02:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:02:56 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:10:29 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:10:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:10:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:10:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:10:33 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8d6f5f280f3c754fdf75be610b9eaad7ee272876c0223bf2f3bd9a69fa411`  
		Last Modified: Tue, 02 Dec 2025 00:03:11 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e82d4d488e2618905f471024c5fe4d2e766267d8f3348b3dd7b6191630216`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f10b7b7acafc5f4d720b74cd91450008c1662de4a06650c39d1fb60537c2a6`  
		Last Modified: Tue, 02 Dec 2025 00:03:14 GMT  
		Size: 17.3 MB (17331274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53231739b67e10b4afa5aed2ecd60407f25e184a679cdbb1b5be2acafe29cc00`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c895eab34015734e14c5a975b34482844ee37ed6cae5b06a56089d9240b3`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 19.9 MB (19869837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549587bc62ff6067012fffc4124531c681e33704d75b4332e354e8e8c7ac9e94`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015487da6372d9bb9ef8a815c66c71f3c29cdd4a5dcaee2f5e87280d9717f00`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25860a630a1731a13c772ef03361714d3807678f3549f006ebe44c22140700b`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ac678ddec83e4354555da6ef9579f4ef2f9988789f66f9a5ca00e87db6b54`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 7.1 MB (7140876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8cd171770863e9348d4ee8c70d82ad8f289d2f4c1d388c224940feff19e47a`  
		Last Modified: Tue, 02 Dec 2025 00:11:01 GMT  
		Size: 99.5 KB (99516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5c60c1c2283f8e5a61f9ffda4011e80b738fd729f6732471650d647f62cb9`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c4891a520b352f266fdd87afc53d295cf90939a3cf3161134eee0a9f36e1d`  
		Last Modified: Tue, 02 Dec 2025 00:11:17 GMT  
		Size: 58.4 MB (58424894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d5d9da598fa4548678e746eb3de0f80e0197dc4482495dd269b371f4ab250`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ddcdacde67a928d9cfcb6dafce29f04eeb8bff016e6cd2756fea0f8a499d79`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:69a58a45b2f2152765e4d687b8e3006251f085c64eb9a725cd9562931e90989d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba11b7f0671e0843042aae85daa5eec651de997c5be2739f8d372d98a5fe0674`

```dockerfile
```

-	Layers:
	-	`sha256:70f851367f687fd4db17c04dc02a75b417cdb7a18c3bf70b7a00292fa8e33939`  
		Last Modified: Tue, 02 Dec 2025 03:08:14 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:b6b6bfc4ba4c55a1e921d6d37e4d6e11dd3d6c73e9e7e4a712371ace91e6c106
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

### `docker:29-cli` - linux; amd64

```console
$ docker pull docker@sha256:06d66076bb85261b052f4b1fdf594cb94a90666282d19d1c8950e40f58a856d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75449058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807a85c29587d39053f60ea09e02d190f569f0becaf9cd592f2b77afa92b4d69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:08:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bca2c07d80098fe1c61e0aa26eac435752d6dca6a2d3837735a2f68eedd27f`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 8.2 MB (8232306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c13c6aae9df8eeb1b8fe904cbdc67165e49d9f6ca682577bdee0ff1fddb0e`  
		Last Modified: Tue, 02 Dec 2025 00:08:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbba1101f59cdf058694512346b7fb8aeda578243290fc893ba55d81ac314cd`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 18.8 MB (18762388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc6a25ab2f1cc6386ed9595b9c99245b984bddba79a401ede272b40c8a1d34`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3786f9aa3c17d408a9f2162d158dcac195becac82c72ee0a4b29c43f52649`  
		Last Modified: Tue, 02 Dec 2025 00:08:43 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de8d894975036d476ad31205669d2600d672441a0b78b3d35650f89daf8774`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8318820339c402ec6f7161ee23642657be448d0298de2ca2a4946643e99bf`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fca41ae3f7f0a9e8364572b85d6e7862b0a01a49813320a77b7cca46a3dc67`  
		Last Modified: Tue, 02 Dec 2025 00:08:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:26274226c8c0faadd21be8696f3a311564ad7a4ab1ef384c048553a24d3f0ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916e002882958960262548cbc5346e72669f994ab582698cb9f97c5a25a565e9`

```dockerfile
```

-	Layers:
	-	`sha256:a46ae34aa73068e39fe087bf2583406667a30359eb3f75440314f7c1acb9296a`  
		Last Modified: Tue, 02 Dec 2025 03:08:20 GMT  
		Size: 38.1 KB (38072 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:7dec30a9bddbb6a8022449d724ec7ccb8d72831f641c9318256e13621b115f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71162709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe592527df6e45624d69acd1f08345d80166ac1b721283466fa69b5e70d1fce4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:00:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:01:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:01:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:01:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:01:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:03 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd90142670bbaed6f585f4970fd1d53633e0869fd5272c8e3df77120bace0e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 8.1 MB (8140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642374c76164440ef8b823ab6bba0dd1bee0e2a2376c47bb5f4073a585413e04`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed115a71dbefda1db4593399cccc8dad9b72d92954e97811cb17ea6cbd16029`  
		Last Modified: Tue, 02 Dec 2025 00:01:24 GMT  
		Size: 17.6 MB (17559034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5443b6b267bcc407b81aa1fc56c89a28780986fdb8a6a0e262dc6cb167368cb`  
		Last Modified: Tue, 02 Dec 2025 00:01:23 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1408d4a896b763e6cf9b6eb5321ee325d093c04ddb275e901a85d57735dd87d`  
		Last Modified: Tue, 02 Dec 2025 00:01:21 GMT  
		Size: 20.5 MB (20480374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc905b6a443c6c8096533c447544d946dedb7a2450e9d8815424d25a2b70b5b8`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79661a927ae816f329cd8e6d5aebc5775b45d598f860218a7fa0bf34259fedae`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc8f4aa5c2b729f00263aa5f33b190bedfd7d94a05ac9ccb26f4f1995d10a1e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:59f483c5d14576f6604d8761286ec411d1e4cea808c56c6517fa68aa86482f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7eb9816e4263309859c9fa2544254d266fce016841a6dd9ebb252dfb60b369`

```dockerfile
```

-	Layers:
	-	`sha256:2b4874b8d5341ca253e2d4e4c06cb6938a34fde4eb798103ab4ba8f879527028`  
		Last Modified: Tue, 02 Dec 2025 03:08:23 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:e29562e7b2b07035db21a39fc060357a494d7cfb2aa8e6d1b34cdd2c28492ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70153607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682acbc8a7f3934bc163828bdbf4f86937e5f744b33fe889d224a4e560b25d5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:03:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:03:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:03:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:03:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec0784ecb867af52b79e3f383d52e39182464803fd28c22d49d1ff019df6e4`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 7.5 MB (7461368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491247472d55430402882837b71580b20d49d688f85f713917e74b9c4dcfa29`  
		Last Modified: Tue, 02 Dec 2025 00:03:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681ac3424d8a722d9e60118306e4292f0558f8234066431fcf35fe24394a1bb8`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 17.6 MB (17550851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4ccba3516b05ed1ea12fcc5ff93f84c20331f6098765bc58aa14342452b044`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01cc08290b32581069106ced2f3f3eb8ee944803bea261cb440c95a59f3e88`  
		Last Modified: Tue, 02 Dec 2025 00:03:52 GMT  
		Size: 20.5 MB (20462776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3320b40de969faa831b8c731ba2d0e1b46c0099f07df033d271e79b3ae90cfa`  
		Last Modified: Tue, 02 Dec 2025 00:03:49 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6f871522091994e48824cf572b17680f5f65920875e93a33820ca79643cb83`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccd637b5bd3f36088e619e2cd9af1073d6cf18b4daae90c18da0bebaac04039`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2a42b7168acc8dd7465a298f656d13b5ef3da6a4e4a802e7c2f758b3b87528fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d110713e939ebab1bfb3791674c56ccdb6a71e216860021350b985431c1398`

```dockerfile
```

-	Layers:
	-	`sha256:e3979750bdc58314c6ed89fe981aa70da96caf2931e7efe401364b9464cc2e37`  
		Last Modified: Tue, 02 Dec 2025 03:08:26 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:056f1c5ae751413a3801dc2a11917de4e3278964a995f552292e55b588a32db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70243742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b329681fa645f06008f07c64da4c89ed70718d7a45714e322d215dedb1ace80a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:02:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:02:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:02:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:02:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:02:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:02:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8d6f5f280f3c754fdf75be610b9eaad7ee272876c0223bf2f3bd9a69fa411`  
		Last Modified: Tue, 02 Dec 2025 00:03:11 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e82d4d488e2618905f471024c5fe4d2e766267d8f3348b3dd7b6191630216`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f10b7b7acafc5f4d720b74cd91450008c1662de4a06650c39d1fb60537c2a6`  
		Last Modified: Tue, 02 Dec 2025 00:03:14 GMT  
		Size: 17.3 MB (17331274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53231739b67e10b4afa5aed2ecd60407f25e184a679cdbb1b5be2acafe29cc00`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c895eab34015734e14c5a975b34482844ee37ed6cae5b06a56089d9240b3`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 19.9 MB (19869837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549587bc62ff6067012fffc4124531c681e33704d75b4332e354e8e8c7ac9e94`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015487da6372d9bb9ef8a815c66c71f3c29cdd4a5dcaee2f5e87280d9717f00`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25860a630a1731a13c772ef03361714d3807678f3549f006ebe44c22140700b`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7da5ae430420c1356c0bd6c28cbcbaad830ffe49f10f32553ae5a481daa8b7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2bc66f36721e245c614fa122147d157eb29e4a89b1d28c8819d7d789616898`

```dockerfile
```

-	Layers:
	-	`sha256:377912c6134d900c01b748697784d6625f52f655404bcc8267902a5e62ab31c7`  
		Last Modified: Tue, 02 Dec 2025 03:08:29 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:9b20eb23e1f0443655673efb9db76c4b18cc1b45de1fcf82b3c1b749b9647bdf
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

### `docker:29-dind` - linux; amd64

```console
$ docker pull docker@sha256:e7722a3fdf461a91095cc11b6751da7e69a1bdd583df23b5837cd03bc3dcbf11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146834840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3d6683ede5a5e31409999791e15e1785c65344da6483593dd3af23c29bd562`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:08:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:07 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:35:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:35:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:35:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:35:13 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bca2c07d80098fe1c61e0aa26eac435752d6dca6a2d3837735a2f68eedd27f`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 8.2 MB (8232306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c13c6aae9df8eeb1b8fe904cbdc67165e49d9f6ca682577bdee0ff1fddb0e`  
		Last Modified: Tue, 02 Dec 2025 00:08:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbba1101f59cdf058694512346b7fb8aeda578243290fc893ba55d81ac314cd`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 18.8 MB (18762388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc6a25ab2f1cc6386ed9595b9c99245b984bddba79a401ede272b40c8a1d34`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3786f9aa3c17d408a9f2162d158dcac195becac82c72ee0a4b29c43f52649`  
		Last Modified: Tue, 02 Dec 2025 00:08:43 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de8d894975036d476ad31205669d2600d672441a0b78b3d35650f89daf8774`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8318820339c402ec6f7161ee23642657be448d0298de2ca2a4946643e99bf`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fca41ae3f7f0a9e8364572b85d6e7862b0a01a49813320a77b7cca46a3dc67`  
		Last Modified: Tue, 02 Dec 2025 00:08:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eaeb7e3ff54863b596ddf45aa1f53fe06b5bac153cd3057038bca861e20c27`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 6.9 MB (6905410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568debdaab006707818488bd30ccbe9d028b275d05c6ce65dd3b1aec6ecdd841`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6f1c21ebbe286ed54f5e70396d9124048a5aab0e142aa1b81824ff82ace94`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b638749a1ad920d398a23428bd3e49a14bdf1b01a65776444264fa6afec6effd`  
		Last Modified: Tue, 02 Dec 2025 00:36:12 GMT  
		Size: 64.4 MB (64383976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4c76068297a0e5e2b8b3f4b582b62ec0bd167377a14e5e849d084838dd7d65`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831f7baf80344c1ea02c8259ab473f8c112481bf3ba30f27311a27ae615a6ba9`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b3ffbc635daa4785c6e8540daa89e290342d9ce7574d182f603904c844e2ae55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cddfa71d427c6ffde929b85b3ac597a723b864fa7b755fb7e2b38bffcec4abf`

```dockerfile
```

-	Layers:
	-	`sha256:c293678f6e88a59d70f255b8b2d4d5370350c49c9cac522deee7e1ca928a771f`  
		Last Modified: Tue, 02 Dec 2025 03:08:05 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f4264dc6f53bf84c143abcd79f054061e949f91297519b16342df3b0fcf515d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138377571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5525feeb0b6b1996748694f01b24cce0d9825880fcc090ceaec227482995adb8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:00:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:01:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:01:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:01:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:01:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:03 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:08:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:08:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:08:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:08:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:08:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:08:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:47 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd90142670bbaed6f585f4970fd1d53633e0869fd5272c8e3df77120bace0e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 8.1 MB (8140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642374c76164440ef8b823ab6bba0dd1bee0e2a2376c47bb5f4073a585413e04`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed115a71dbefda1db4593399cccc8dad9b72d92954e97811cb17ea6cbd16029`  
		Last Modified: Tue, 02 Dec 2025 00:01:24 GMT  
		Size: 17.6 MB (17559034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5443b6b267bcc407b81aa1fc56c89a28780986fdb8a6a0e262dc6cb167368cb`  
		Last Modified: Tue, 02 Dec 2025 00:01:23 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1408d4a896b763e6cf9b6eb5321ee325d093c04ddb275e901a85d57735dd87d`  
		Last Modified: Tue, 02 Dec 2025 00:01:21 GMT  
		Size: 20.5 MB (20480374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc905b6a443c6c8096533c447544d946dedb7a2450e9d8815424d25a2b70b5b8`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79661a927ae816f329cd8e6d5aebc5775b45d598f860218a7fa0bf34259fedae`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc8f4aa5c2b729f00263aa5f33b190bedfd7d94a05ac9ccb26f4f1995d10a1e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f114e86733f934e05b8cc095e26ac7d23df0400c164367a5d0960c90ffbb7e7`  
		Last Modified: Tue, 02 Dec 2025 00:09:22 GMT  
		Size: 7.2 MB (7230316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52de536e5339daea653f15c27e78b4cf16e12a10d82ef4f286872bc4f4aafd9`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 90.0 KB (89961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae860099f824f4d5c845c472dccead8faa86f1afc2773e064de55ac8317fa514`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99458a7fe0e1036a55a30274f0e06e8baa5da805dac7a2d7f788bf02c9531c18`  
		Last Modified: Tue, 02 Dec 2025 00:09:30 GMT  
		Size: 59.9 MB (59888589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bba7682b037f71b8aea88b0676d075b4bcd35fa3390b95b1bd864d4999afb7d`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed47c75bfd062f331a396b716966fb250ee7485fee132a7b2942e732842fbf3`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ec56f63d4804233c364f31addc653c748a9b7e58cc1b72a68562b7cfd4f5869d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3125bbdfa07949727984336157b0367e420ed260fb1153f6a4ac86374835df20`

```dockerfile
```

-	Layers:
	-	`sha256:e35660952afa463bcd149750757d217195b0afeb78547aeae6aecaf7697b4b82`  
		Last Modified: Tue, 02 Dec 2025 03:08:08 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:4c9e1d32783f3091ec573930696e1a02680c8b2e0a96588960e8cfb4785f0987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136499855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a132a67d9b1e15c2a6b6b5072baf4669d91a4c94c59594cde5e134a3f13f7e0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:03:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:03:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:03:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:03:35 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:08:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:08:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:08:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:08:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:08:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:08:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:52 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec0784ecb867af52b79e3f383d52e39182464803fd28c22d49d1ff019df6e4`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 7.5 MB (7461368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491247472d55430402882837b71580b20d49d688f85f713917e74b9c4dcfa29`  
		Last Modified: Tue, 02 Dec 2025 00:03:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681ac3424d8a722d9e60118306e4292f0558f8234066431fcf35fe24394a1bb8`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 17.6 MB (17550851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4ccba3516b05ed1ea12fcc5ff93f84c20331f6098765bc58aa14342452b044`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01cc08290b32581069106ced2f3f3eb8ee944803bea261cb440c95a59f3e88`  
		Last Modified: Tue, 02 Dec 2025 00:03:52 GMT  
		Size: 20.5 MB (20462776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3320b40de969faa831b8c731ba2d0e1b46c0099f07df033d271e79b3ae90cfa`  
		Last Modified: Tue, 02 Dec 2025 00:03:49 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6f871522091994e48824cf572b17680f5f65920875e93a33820ca79643cb83`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccd637b5bd3f36088e619e2cd9af1073d6cf18b4daae90c18da0bebaac04039`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fedb293900f104824c5bf607d49531816ebb696de67d2349e25c3b7235c7d4`  
		Last Modified: Tue, 02 Dec 2025 03:08:37 GMT  
		Size: 6.5 MB (6538170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f3efb3e0b8e692ee930467452c2b90850e32de6e81f525c8b5ecb809596cb1`  
		Last Modified: Tue, 02 Dec 2025 01:10:44 GMT  
		Size: 86.4 KB (86397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6a05cebb7258e8cc03a59c4ddbfab058b79a4254d47f5f7339c3cbb66e0f91`  
		Last Modified: Tue, 02 Dec 2025 01:10:45 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2700c9375899dc20256cee56347f7a94685712635d0a083c74baf5a4d0ac5809`  
		Last Modified: Tue, 02 Dec 2025 03:08:48 GMT  
		Size: 59.7 MB (59715683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f83379703e2b0dd6765daef6f82dba3e582ae979b57dfd62b9101c915e244`  
		Last Modified: Tue, 02 Dec 2025 01:10:48 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fb0afbbc9ea4bc8903a6671f34110ef481952a81c388cc585e9b21cd7f4e21`  
		Last Modified: Tue, 02 Dec 2025 01:10:44 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:81b93d08f8b08b14411acfcfd4683554ff94f1553aa1c42bb33bb2e43d453ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db32ac5181c3e6cf95fea47b5846cd4a761768ec6dc895055994af29bcb7718b`

```dockerfile
```

-	Layers:
	-	`sha256:9f6b2982982b5b6659faac06d4632eb9f834c5522239d5ab3c1c0c340c2664f7`  
		Last Modified: Tue, 02 Dec 2025 03:08:11 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:37269ed2d81f5f6d65910acc46f07807e7027efa4560c03b5c2c427c57b5b99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135915031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cb9c89488e9663f2162c6982870ff63ce946066edbedbf787cccfcb650d4a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:02:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:02:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:02:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:02:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:02:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:02:56 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:10:29 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:10:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:10:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:10:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:10:33 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8d6f5f280f3c754fdf75be610b9eaad7ee272876c0223bf2f3bd9a69fa411`  
		Last Modified: Tue, 02 Dec 2025 00:03:11 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e82d4d488e2618905f471024c5fe4d2e766267d8f3348b3dd7b6191630216`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f10b7b7acafc5f4d720b74cd91450008c1662de4a06650c39d1fb60537c2a6`  
		Last Modified: Tue, 02 Dec 2025 00:03:14 GMT  
		Size: 17.3 MB (17331274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53231739b67e10b4afa5aed2ecd60407f25e184a679cdbb1b5be2acafe29cc00`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c895eab34015734e14c5a975b34482844ee37ed6cae5b06a56089d9240b3`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 19.9 MB (19869837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549587bc62ff6067012fffc4124531c681e33704d75b4332e354e8e8c7ac9e94`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015487da6372d9bb9ef8a815c66c71f3c29cdd4a5dcaee2f5e87280d9717f00`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25860a630a1731a13c772ef03361714d3807678f3549f006ebe44c22140700b`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ac678ddec83e4354555da6ef9579f4ef2f9988789f66f9a5ca00e87db6b54`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 7.1 MB (7140876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8cd171770863e9348d4ee8c70d82ad8f289d2f4c1d388c224940feff19e47a`  
		Last Modified: Tue, 02 Dec 2025 00:11:01 GMT  
		Size: 99.5 KB (99516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5c60c1c2283f8e5a61f9ffda4011e80b738fd729f6732471650d647f62cb9`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c4891a520b352f266fdd87afc53d295cf90939a3cf3161134eee0a9f36e1d`  
		Last Modified: Tue, 02 Dec 2025 00:11:17 GMT  
		Size: 58.4 MB (58424894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d5d9da598fa4548678e746eb3de0f80e0197dc4482495dd269b371f4ab250`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ddcdacde67a928d9cfcb6dafce29f04eeb8bff016e6cd2756fea0f8a499d79`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:69a58a45b2f2152765e4d687b8e3006251f085c64eb9a725cd9562931e90989d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba11b7f0671e0843042aae85daa5eec651de997c5be2739f8d372d98a5fe0674`

```dockerfile
```

-	Layers:
	-	`sha256:70f851367f687fd4db17c04dc02a75b417cdb7a18c3bf70b7a00292fa8e33939`  
		Last Modified: Tue, 02 Dec 2025 03:08:14 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:26d283e4272e65c34bec8b7703698f75583b470b7fa5d6ac7b0544632dcdc74d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:4d55728f99b9642731991198ac30737ae9269d10e0d4721f798d1a6c7b6b6646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167604793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f500029a797b09b09f16482f6fd1be288c57d9355fc7176acea27545f24040aa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:08:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:07 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:35:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:35:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:35:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:35:13 GMT
CMD []
# Tue, 02 Dec 2025 01:04:33 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 02 Dec 2025 01:04:33 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 02 Dec 2025 01:04:33 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 01:04:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 02 Dec 2025 01:04:34 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 02 Dec 2025 01:04:34 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 02 Dec 2025 01:04:34 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bca2c07d80098fe1c61e0aa26eac435752d6dca6a2d3837735a2f68eedd27f`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 8.2 MB (8232306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c13c6aae9df8eeb1b8fe904cbdc67165e49d9f6ca682577bdee0ff1fddb0e`  
		Last Modified: Tue, 02 Dec 2025 00:08:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbba1101f59cdf058694512346b7fb8aeda578243290fc893ba55d81ac314cd`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 18.8 MB (18762388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc6a25ab2f1cc6386ed9595b9c99245b984bddba79a401ede272b40c8a1d34`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3786f9aa3c17d408a9f2162d158dcac195becac82c72ee0a4b29c43f52649`  
		Last Modified: Tue, 02 Dec 2025 00:08:43 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de8d894975036d476ad31205669d2600d672441a0b78b3d35650f89daf8774`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8318820339c402ec6f7161ee23642657be448d0298de2ca2a4946643e99bf`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fca41ae3f7f0a9e8364572b85d6e7862b0a01a49813320a77b7cca46a3dc67`  
		Last Modified: Tue, 02 Dec 2025 00:08:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eaeb7e3ff54863b596ddf45aa1f53fe06b5bac153cd3057038bca861e20c27`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 6.9 MB (6905410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568debdaab006707818488bd30ccbe9d028b275d05c6ce65dd3b1aec6ecdd841`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6f1c21ebbe286ed54f5e70396d9124048a5aab0e142aa1b81824ff82ace94`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b638749a1ad920d398a23428bd3e49a14bdf1b01a65776444264fa6afec6effd`  
		Last Modified: Tue, 02 Dec 2025 00:36:12 GMT  
		Size: 64.4 MB (64383976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4c76068297a0e5e2b8b3f4b582b62ec0bd167377a14e5e849d084838dd7d65`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831f7baf80344c1ea02c8259ab473f8c112481bf3ba30f27311a27ae615a6ba9`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6ab179a37092cfe7a4ed7e56cfaa4245be172a64fa8983225d912989c5fcc5`  
		Last Modified: Tue, 02 Dec 2025 01:04:49 GMT  
		Size: 3.4 MB (3398376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff83acf3702948a722e974d3dfc0a3282ac4ea70c4b2338b9a522e2544f1ade5`  
		Last Modified: Tue, 02 Dec 2025 01:04:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef24dccdc8e52bba4677dc83acf458b27fc0ee05e8023ff60cd3092c847448a`  
		Last Modified: Tue, 02 Dec 2025 01:04:49 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675547768fa484d1c34426e57586edd545c80c258f8ee3b1daad209973a18e39`  
		Last Modified: Tue, 02 Dec 2025 01:04:52 GMT  
		Size: 17.4 MB (17370238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6970303a67916649ea0e564b703347d9b6d63a5499fd2317d7bc25825bac820e`  
		Last Modified: Tue, 02 Dec 2025 01:04:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:eb319559cabdac9b6d6e61682add0ddd92bc4a1f016e42cb5cb54cb4406e18fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8a901677136393b67572d4d6f9bc5a7138099f768ffa584d6a047f88e97c1f`

```dockerfile
```

-	Layers:
	-	`sha256:a3186791ef27178f63f3334dcbdf3618a5894a1a04a580d19d58df0aad0c51f6`  
		Last Modified: Tue, 02 Dec 2025 03:08:36 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:500d9983f84e3c1918053364b152d6c8678606181d1b47f39e6e56325f88a4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157013358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259bf946645a41d2af38ec03e3dbc71a98181d2ae1e3f4953a1d790b71712216`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:02:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:02:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:02:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:02:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:02:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:02:56 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:10:29 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:10:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:10:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:10:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:10:33 GMT
CMD []
# Tue, 02 Dec 2025 00:16:44 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 02 Dec 2025 00:16:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 02 Dec 2025 00:16:44 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:16:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 02 Dec 2025 00:16:45 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 02 Dec 2025 00:16:45 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 02 Dec 2025 00:16:45 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8d6f5f280f3c754fdf75be610b9eaad7ee272876c0223bf2f3bd9a69fa411`  
		Last Modified: Tue, 02 Dec 2025 00:03:11 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e82d4d488e2618905f471024c5fe4d2e766267d8f3348b3dd7b6191630216`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f10b7b7acafc5f4d720b74cd91450008c1662de4a06650c39d1fb60537c2a6`  
		Last Modified: Tue, 02 Dec 2025 00:03:14 GMT  
		Size: 17.3 MB (17331274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53231739b67e10b4afa5aed2ecd60407f25e184a679cdbb1b5be2acafe29cc00`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c895eab34015734e14c5a975b34482844ee37ed6cae5b06a56089d9240b3`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 19.9 MB (19869837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549587bc62ff6067012fffc4124531c681e33704d75b4332e354e8e8c7ac9e94`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015487da6372d9bb9ef8a815c66c71f3c29cdd4a5dcaee2f5e87280d9717f00`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25860a630a1731a13c772ef03361714d3807678f3549f006ebe44c22140700b`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ac678ddec83e4354555da6ef9579f4ef2f9988789f66f9a5ca00e87db6b54`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 7.1 MB (7140876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8cd171770863e9348d4ee8c70d82ad8f289d2f4c1d388c224940feff19e47a`  
		Last Modified: Tue, 02 Dec 2025 00:11:01 GMT  
		Size: 99.5 KB (99516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5c60c1c2283f8e5a61f9ffda4011e80b738fd729f6732471650d647f62cb9`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c4891a520b352f266fdd87afc53d295cf90939a3cf3161134eee0a9f36e1d`  
		Last Modified: Tue, 02 Dec 2025 00:11:17 GMT  
		Size: 58.4 MB (58424894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d5d9da598fa4548678e746eb3de0f80e0197dc4482495dd269b371f4ab250`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ddcdacde67a928d9cfcb6dafce29f04eeb8bff016e6cd2756fea0f8a499d79`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763091d1251eb3f132c7b256f6b764c4d0955511bb4d4cfa11a52a3748b983b4`  
		Last Modified: Tue, 02 Dec 2025 00:17:05 GMT  
		Size: 3.4 MB (3389942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7986a5219667182dcb2d7497f51bcaf7b8358e271f41f0423f8f6665e6e8e27`  
		Last Modified: Tue, 02 Dec 2025 00:17:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2c564976ca2ad686546fe1e57597bd2623c76c3d660e852e930f32acfb7ffc`  
		Last Modified: Tue, 02 Dec 2025 00:17:05 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f8d39c0e9195885f73df58fb87203a86f5600e9372dc7af6c6ced416c50de3`  
		Last Modified: Tue, 02 Dec 2025 00:17:10 GMT  
		Size: 17.7 MB (17707046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b4c481f84d857b2b25d71535d076ec14fe51bf97a7693bb84958d2cc97bc79`  
		Last Modified: Tue, 02 Dec 2025 00:17:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:293f1f699032f6d51172da18bfd76ae3d5160bae1b22229359b445b35e2f27e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8a0d27bc916671f250df0b710a855e84e8aa12c157c41c5e1ac989214fcadd`

```dockerfile
```

-	Layers:
	-	`sha256:43e535d7855d564532284ba0cc7bd59b7a8ba7a0be76ae888afdda1ac9c29482`  
		Last Modified: Tue, 02 Dec 2025 03:08:39 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:1c43c735429614f250536aac0dd2c328e6d0b893b299c60a260849bf484844e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:edb55a55a9709f716094eff0d619f5cccfbe7ab9c820d4cd94316a3dc80f85b0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301942510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd431f71a41f9ca0d66fa3490028ce3378094dc608e876e5a5e01d5f1c00a85`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 02 Dec 2025 00:02:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:03:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:03:18 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:03:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:03:38 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:03:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:03:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1274f6d3b6ceaa195acd16a17546b93878ef3c76e6b0c0ea475532ae81138829`  
		Last Modified: Tue, 02 Dec 2025 00:29:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18719cadfdf416a79dc2e3958aaaa04ba5f00625ff6e93ab3dec72cf2f51da`  
		Last Modified: Tue, 02 Dec 2025 00:29:25 GMT  
		Size: 394.4 KB (394389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacb90f7314fdc946208b5f3ff65f6c72d6649551c978d26418bda8d9e5a6890`  
		Last Modified: Tue, 02 Dec 2025 00:29:30 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad66afc50aa529e50d970dea5d3e8f437aab69ad9cb3882a256d4319b5b42d15`  
		Last Modified: Tue, 02 Dec 2025 00:29:33 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b85b05963e8f44359d0370018251cb0af969ffdbeeb8b5a7d16e32fa4e6e0`  
		Last Modified: Tue, 02 Dec 2025 01:01:49 GMT  
		Size: 19.4 MB (19445634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4369b8ed94ba65d95a6942b0a54d8302024faae5688bd932577bcc256abefee3`  
		Last Modified: Tue, 02 Dec 2025 00:29:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a49cd2f3d1017e97f6ed405d89cd3d09949977cd4e8b5b34fdb146b8da04a3`  
		Last Modified: Tue, 02 Dec 2025 00:29:41 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f583f8eec952d8c1f2b32d817e3b14c51c57780bc726d9eb1c393555075ba3c7`  
		Last Modified: Tue, 02 Dec 2025 00:29:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9def44a99f4bab2dcc70f25abcf502cbafd84b76181171949b51aa186814cce8`  
		Last Modified: Tue, 02 Dec 2025 01:01:52 GMT  
		Size: 23.9 MB (23942612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46335ebb4377421068829028c4feca1ce21bb336ddc77ffaff4cf2fdd07669d`  
		Last Modified: Tue, 02 Dec 2025 00:29:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6700c7401706484942b62f39837e732625ea2eae796316fd97da557c97d9a2bd`  
		Last Modified: Tue, 02 Dec 2025 00:29:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fcde18a4abb110b9720f6357dc8098af919dc2247e1fcb902d2dbce1dc2bbb`  
		Last Modified: Tue, 02 Dec 2025 00:29:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a06df7c12fbd246e254cc1c5ccda1ea8a3064c55627e865f6c813204a155a`  
		Last Modified: Tue, 02 Dec 2025 01:01:55 GMT  
		Size: 22.7 MB (22692302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:59fd73de957de338aebfa44cbc56e9e613995025b25e51d83b83c144f5f15828
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836458539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb88b8d8055f99a033e38f88e5335522379ea547e8004051da7417b42321791`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 02 Dec 2025 00:09:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:10:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:10:58 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:11:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:11:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:11:29 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:11:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:11:32 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:11:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:11:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:11:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:12:00 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:12:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca80c7273175042e00fe42b9acc4273bb878eee0a0c4c5fa397b7397b8841b60`  
		Last Modified: Tue, 02 Dec 2025 00:27:05 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de920d113346f7751e223cc4f56c9ac711e693c7bbad0a62661edd7a13e3cb18`  
		Last Modified: Tue, 02 Dec 2025 00:27:06 GMT  
		Size: 518.9 KB (518913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4006e793c124c40f2cd2b04d3620d9d0701f4a8b6b235a461ac6bf489cfee31`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b20b11149feeb6be69bcded688660b34c2ff915411a4a073b5a67b8511a88e`  
		Last Modified: Tue, 02 Dec 2025 00:27:07 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f920b83c504a555c3b5c26902e6a1ec22ef2c88c9afba067de16269b6f0429`  
		Last Modified: Tue, 02 Dec 2025 00:27:10 GMT  
		Size: 19.4 MB (19406772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf9e2e8b9aa98bf5c8b54f2bc38c78ea68496c411e4620b1762bd486b251406`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e633a60820512a97163b768f578d2ed4c4d4e6a403d9a260fc3625581aee37d6`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c418e2d05c842f6856d59f8030e8c3b42bc6d2060d9185961466724fb8ebb259`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cefba9d08372f4b315b8a9b066b2e795c2a6f31473405639443e63a3a13cb4e`  
		Last Modified: Tue, 02 Dec 2025 00:27:12 GMT  
		Size: 23.9 MB (23905567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9c528564d3c90f5342ffbe261f0e02cc558cd11bb1c2cda3901acce07c071e`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac38da0772c85387d94e42b5ac044035676912ba7b05c906b2b267f10c2c0e10`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90916836d70bec2b5e65b639f5ebfb46be73741a370798dee04edb8ee868a44b`  
		Last Modified: Tue, 02 Dec 2025 00:27:12 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42bcb722bb6159035d26e8273c1451882c9adf5073c21bba4efbc06e42c5f68`  
		Last Modified: Tue, 02 Dec 2025 00:27:14 GMT  
		Size: 22.7 MB (22653934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:da10f7e9be92554d35616813bc89c43489e9d0568b3682aa5dd4c573ce5e9a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:59fd73de957de338aebfa44cbc56e9e613995025b25e51d83b83c144f5f15828
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836458539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb88b8d8055f99a033e38f88e5335522379ea547e8004051da7417b42321791`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 02 Dec 2025 00:09:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:10:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:10:58 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:11:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:11:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:11:29 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:11:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:11:32 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:11:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:11:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:11:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:12:00 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:12:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca80c7273175042e00fe42b9acc4273bb878eee0a0c4c5fa397b7397b8841b60`  
		Last Modified: Tue, 02 Dec 2025 00:27:05 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de920d113346f7751e223cc4f56c9ac711e693c7bbad0a62661edd7a13e3cb18`  
		Last Modified: Tue, 02 Dec 2025 00:27:06 GMT  
		Size: 518.9 KB (518913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4006e793c124c40f2cd2b04d3620d9d0701f4a8b6b235a461ac6bf489cfee31`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b20b11149feeb6be69bcded688660b34c2ff915411a4a073b5a67b8511a88e`  
		Last Modified: Tue, 02 Dec 2025 00:27:07 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f920b83c504a555c3b5c26902e6a1ec22ef2c88c9afba067de16269b6f0429`  
		Last Modified: Tue, 02 Dec 2025 00:27:10 GMT  
		Size: 19.4 MB (19406772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf9e2e8b9aa98bf5c8b54f2bc38c78ea68496c411e4620b1762bd486b251406`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e633a60820512a97163b768f578d2ed4c4d4e6a403d9a260fc3625581aee37d6`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c418e2d05c842f6856d59f8030e8c3b42bc6d2060d9185961466724fb8ebb259`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cefba9d08372f4b315b8a9b066b2e795c2a6f31473405639443e63a3a13cb4e`  
		Last Modified: Tue, 02 Dec 2025 00:27:12 GMT  
		Size: 23.9 MB (23905567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9c528564d3c90f5342ffbe261f0e02cc558cd11bb1c2cda3901acce07c071e`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac38da0772c85387d94e42b5ac044035676912ba7b05c906b2b267f10c2c0e10`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90916836d70bec2b5e65b639f5ebfb46be73741a370798dee04edb8ee868a44b`  
		Last Modified: Tue, 02 Dec 2025 00:27:12 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42bcb722bb6159035d26e8273c1451882c9adf5073c21bba4efbc06e42c5f68`  
		Last Modified: Tue, 02 Dec 2025 00:27:14 GMT  
		Size: 22.7 MB (22653934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:5e399dd5dd0dfe81579a2bca9462ce91fd0af47c6c1f7a6b73ffbc942907f790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:edb55a55a9709f716094eff0d619f5cccfbe7ab9c820d4cd94316a3dc80f85b0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301942510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd431f71a41f9ca0d66fa3490028ce3378094dc608e876e5a5e01d5f1c00a85`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 02 Dec 2025 00:02:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:03:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:03:18 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:03:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:03:38 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:03:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:03:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1274f6d3b6ceaa195acd16a17546b93878ef3c76e6b0c0ea475532ae81138829`  
		Last Modified: Tue, 02 Dec 2025 00:29:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18719cadfdf416a79dc2e3958aaaa04ba5f00625ff6e93ab3dec72cf2f51da`  
		Last Modified: Tue, 02 Dec 2025 00:29:25 GMT  
		Size: 394.4 KB (394389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacb90f7314fdc946208b5f3ff65f6c72d6649551c978d26418bda8d9e5a6890`  
		Last Modified: Tue, 02 Dec 2025 00:29:30 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad66afc50aa529e50d970dea5d3e8f437aab69ad9cb3882a256d4319b5b42d15`  
		Last Modified: Tue, 02 Dec 2025 00:29:33 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b85b05963e8f44359d0370018251cb0af969ffdbeeb8b5a7d16e32fa4e6e0`  
		Last Modified: Tue, 02 Dec 2025 01:01:49 GMT  
		Size: 19.4 MB (19445634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4369b8ed94ba65d95a6942b0a54d8302024faae5688bd932577bcc256abefee3`  
		Last Modified: Tue, 02 Dec 2025 00:29:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a49cd2f3d1017e97f6ed405d89cd3d09949977cd4e8b5b34fdb146b8da04a3`  
		Last Modified: Tue, 02 Dec 2025 00:29:41 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f583f8eec952d8c1f2b32d817e3b14c51c57780bc726d9eb1c393555075ba3c7`  
		Last Modified: Tue, 02 Dec 2025 00:29:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9def44a99f4bab2dcc70f25abcf502cbafd84b76181171949b51aa186814cce8`  
		Last Modified: Tue, 02 Dec 2025 01:01:52 GMT  
		Size: 23.9 MB (23942612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46335ebb4377421068829028c4feca1ce21bb336ddc77ffaff4cf2fdd07669d`  
		Last Modified: Tue, 02 Dec 2025 00:29:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6700c7401706484942b62f39837e732625ea2eae796316fd97da557c97d9a2bd`  
		Last Modified: Tue, 02 Dec 2025 00:29:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fcde18a4abb110b9720f6357dc8098af919dc2247e1fcb902d2dbce1dc2bbb`  
		Last Modified: Tue, 02 Dec 2025 00:29:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a06df7c12fbd246e254cc1c5ccda1ea8a3064c55627e865f6c813204a155a`  
		Last Modified: Tue, 02 Dec 2025 01:01:55 GMT  
		Size: 22.7 MB (22692302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1`

```console
$ docker pull docker@sha256:9b20eb23e1f0443655673efb9db76c4b18cc1b45de1fcf82b3c1b749b9647bdf
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

### `docker:29.1` - linux; amd64

```console
$ docker pull docker@sha256:e7722a3fdf461a91095cc11b6751da7e69a1bdd583df23b5837cd03bc3dcbf11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146834840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3d6683ede5a5e31409999791e15e1785c65344da6483593dd3af23c29bd562`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:08:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:07 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:35:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:35:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:35:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:35:13 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bca2c07d80098fe1c61e0aa26eac435752d6dca6a2d3837735a2f68eedd27f`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 8.2 MB (8232306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c13c6aae9df8eeb1b8fe904cbdc67165e49d9f6ca682577bdee0ff1fddb0e`  
		Last Modified: Tue, 02 Dec 2025 00:08:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbba1101f59cdf058694512346b7fb8aeda578243290fc893ba55d81ac314cd`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 18.8 MB (18762388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc6a25ab2f1cc6386ed9595b9c99245b984bddba79a401ede272b40c8a1d34`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3786f9aa3c17d408a9f2162d158dcac195becac82c72ee0a4b29c43f52649`  
		Last Modified: Tue, 02 Dec 2025 00:08:43 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de8d894975036d476ad31205669d2600d672441a0b78b3d35650f89daf8774`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8318820339c402ec6f7161ee23642657be448d0298de2ca2a4946643e99bf`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fca41ae3f7f0a9e8364572b85d6e7862b0a01a49813320a77b7cca46a3dc67`  
		Last Modified: Tue, 02 Dec 2025 00:08:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eaeb7e3ff54863b596ddf45aa1f53fe06b5bac153cd3057038bca861e20c27`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 6.9 MB (6905410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568debdaab006707818488bd30ccbe9d028b275d05c6ce65dd3b1aec6ecdd841`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6f1c21ebbe286ed54f5e70396d9124048a5aab0e142aa1b81824ff82ace94`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b638749a1ad920d398a23428bd3e49a14bdf1b01a65776444264fa6afec6effd`  
		Last Modified: Tue, 02 Dec 2025 00:36:12 GMT  
		Size: 64.4 MB (64383976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4c76068297a0e5e2b8b3f4b582b62ec0bd167377a14e5e849d084838dd7d65`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831f7baf80344c1ea02c8259ab473f8c112481bf3ba30f27311a27ae615a6ba9`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:b3ffbc635daa4785c6e8540daa89e290342d9ce7574d182f603904c844e2ae55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cddfa71d427c6ffde929b85b3ac597a723b864fa7b755fb7e2b38bffcec4abf`

```dockerfile
```

-	Layers:
	-	`sha256:c293678f6e88a59d70f255b8b2d4d5370350c49c9cac522deee7e1ca928a771f`  
		Last Modified: Tue, 02 Dec 2025 03:08:05 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:f4264dc6f53bf84c143abcd79f054061e949f91297519b16342df3b0fcf515d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138377571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5525feeb0b6b1996748694f01b24cce0d9825880fcc090ceaec227482995adb8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:00:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:01:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:01:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:01:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:01:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:03 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:08:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:08:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:08:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:08:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:08:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:08:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:47 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd90142670bbaed6f585f4970fd1d53633e0869fd5272c8e3df77120bace0e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 8.1 MB (8140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642374c76164440ef8b823ab6bba0dd1bee0e2a2376c47bb5f4073a585413e04`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed115a71dbefda1db4593399cccc8dad9b72d92954e97811cb17ea6cbd16029`  
		Last Modified: Tue, 02 Dec 2025 00:01:24 GMT  
		Size: 17.6 MB (17559034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5443b6b267bcc407b81aa1fc56c89a28780986fdb8a6a0e262dc6cb167368cb`  
		Last Modified: Tue, 02 Dec 2025 00:01:23 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1408d4a896b763e6cf9b6eb5321ee325d093c04ddb275e901a85d57735dd87d`  
		Last Modified: Tue, 02 Dec 2025 00:01:21 GMT  
		Size: 20.5 MB (20480374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc905b6a443c6c8096533c447544d946dedb7a2450e9d8815424d25a2b70b5b8`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79661a927ae816f329cd8e6d5aebc5775b45d598f860218a7fa0bf34259fedae`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc8f4aa5c2b729f00263aa5f33b190bedfd7d94a05ac9ccb26f4f1995d10a1e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f114e86733f934e05b8cc095e26ac7d23df0400c164367a5d0960c90ffbb7e7`  
		Last Modified: Tue, 02 Dec 2025 00:09:22 GMT  
		Size: 7.2 MB (7230316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52de536e5339daea653f15c27e78b4cf16e12a10d82ef4f286872bc4f4aafd9`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 90.0 KB (89961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae860099f824f4d5c845c472dccead8faa86f1afc2773e064de55ac8317fa514`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99458a7fe0e1036a55a30274f0e06e8baa5da805dac7a2d7f788bf02c9531c18`  
		Last Modified: Tue, 02 Dec 2025 00:09:30 GMT  
		Size: 59.9 MB (59888589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bba7682b037f71b8aea88b0676d075b4bcd35fa3390b95b1bd864d4999afb7d`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed47c75bfd062f331a396b716966fb250ee7485fee132a7b2942e732842fbf3`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:ec56f63d4804233c364f31addc653c748a9b7e58cc1b72a68562b7cfd4f5869d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3125bbdfa07949727984336157b0367e420ed260fb1153f6a4ac86374835df20`

```dockerfile
```

-	Layers:
	-	`sha256:e35660952afa463bcd149750757d217195b0afeb78547aeae6aecaf7697b4b82`  
		Last Modified: Tue, 02 Dec 2025 03:08:08 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:4c9e1d32783f3091ec573930696e1a02680c8b2e0a96588960e8cfb4785f0987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136499855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a132a67d9b1e15c2a6b6b5072baf4669d91a4c94c59594cde5e134a3f13f7e0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:03:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:03:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:03:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:03:35 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:08:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:08:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:08:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:08:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:08:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:08:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:52 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec0784ecb867af52b79e3f383d52e39182464803fd28c22d49d1ff019df6e4`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 7.5 MB (7461368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491247472d55430402882837b71580b20d49d688f85f713917e74b9c4dcfa29`  
		Last Modified: Tue, 02 Dec 2025 00:03:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681ac3424d8a722d9e60118306e4292f0558f8234066431fcf35fe24394a1bb8`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 17.6 MB (17550851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4ccba3516b05ed1ea12fcc5ff93f84c20331f6098765bc58aa14342452b044`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01cc08290b32581069106ced2f3f3eb8ee944803bea261cb440c95a59f3e88`  
		Last Modified: Tue, 02 Dec 2025 00:03:52 GMT  
		Size: 20.5 MB (20462776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3320b40de969faa831b8c731ba2d0e1b46c0099f07df033d271e79b3ae90cfa`  
		Last Modified: Tue, 02 Dec 2025 00:03:49 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6f871522091994e48824cf572b17680f5f65920875e93a33820ca79643cb83`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccd637b5bd3f36088e619e2cd9af1073d6cf18b4daae90c18da0bebaac04039`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fedb293900f104824c5bf607d49531816ebb696de67d2349e25c3b7235c7d4`  
		Last Modified: Tue, 02 Dec 2025 03:08:37 GMT  
		Size: 6.5 MB (6538170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f3efb3e0b8e692ee930467452c2b90850e32de6e81f525c8b5ecb809596cb1`  
		Last Modified: Tue, 02 Dec 2025 01:10:44 GMT  
		Size: 86.4 KB (86397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6a05cebb7258e8cc03a59c4ddbfab058b79a4254d47f5f7339c3cbb66e0f91`  
		Last Modified: Tue, 02 Dec 2025 01:10:45 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2700c9375899dc20256cee56347f7a94685712635d0a083c74baf5a4d0ac5809`  
		Last Modified: Tue, 02 Dec 2025 03:08:48 GMT  
		Size: 59.7 MB (59715683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f83379703e2b0dd6765daef6f82dba3e582ae979b57dfd62b9101c915e244`  
		Last Modified: Tue, 02 Dec 2025 01:10:48 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fb0afbbc9ea4bc8903a6671f34110ef481952a81c388cc585e9b21cd7f4e21`  
		Last Modified: Tue, 02 Dec 2025 01:10:44 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:81b93d08f8b08b14411acfcfd4683554ff94f1553aa1c42bb33bb2e43d453ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db32ac5181c3e6cf95fea47b5846cd4a761768ec6dc895055994af29bcb7718b`

```dockerfile
```

-	Layers:
	-	`sha256:9f6b2982982b5b6659faac06d4632eb9f834c5522239d5ab3c1c0c340c2664f7`  
		Last Modified: Tue, 02 Dec 2025 03:08:11 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:37269ed2d81f5f6d65910acc46f07807e7027efa4560c03b5c2c427c57b5b99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135915031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cb9c89488e9663f2162c6982870ff63ce946066edbedbf787cccfcb650d4a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:02:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:02:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:02:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:02:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:02:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:02:56 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:10:29 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:10:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:10:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:10:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:10:33 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8d6f5f280f3c754fdf75be610b9eaad7ee272876c0223bf2f3bd9a69fa411`  
		Last Modified: Tue, 02 Dec 2025 00:03:11 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e82d4d488e2618905f471024c5fe4d2e766267d8f3348b3dd7b6191630216`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f10b7b7acafc5f4d720b74cd91450008c1662de4a06650c39d1fb60537c2a6`  
		Last Modified: Tue, 02 Dec 2025 00:03:14 GMT  
		Size: 17.3 MB (17331274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53231739b67e10b4afa5aed2ecd60407f25e184a679cdbb1b5be2acafe29cc00`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c895eab34015734e14c5a975b34482844ee37ed6cae5b06a56089d9240b3`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 19.9 MB (19869837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549587bc62ff6067012fffc4124531c681e33704d75b4332e354e8e8c7ac9e94`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015487da6372d9bb9ef8a815c66c71f3c29cdd4a5dcaee2f5e87280d9717f00`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25860a630a1731a13c772ef03361714d3807678f3549f006ebe44c22140700b`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ac678ddec83e4354555da6ef9579f4ef2f9988789f66f9a5ca00e87db6b54`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 7.1 MB (7140876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8cd171770863e9348d4ee8c70d82ad8f289d2f4c1d388c224940feff19e47a`  
		Last Modified: Tue, 02 Dec 2025 00:11:01 GMT  
		Size: 99.5 KB (99516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5c60c1c2283f8e5a61f9ffda4011e80b738fd729f6732471650d647f62cb9`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c4891a520b352f266fdd87afc53d295cf90939a3cf3161134eee0a9f36e1d`  
		Last Modified: Tue, 02 Dec 2025 00:11:17 GMT  
		Size: 58.4 MB (58424894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d5d9da598fa4548678e746eb3de0f80e0197dc4482495dd269b371f4ab250`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ddcdacde67a928d9cfcb6dafce29f04eeb8bff016e6cd2756fea0f8a499d79`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:69a58a45b2f2152765e4d687b8e3006251f085c64eb9a725cd9562931e90989d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba11b7f0671e0843042aae85daa5eec651de997c5be2739f8d372d98a5fe0674`

```dockerfile
```

-	Layers:
	-	`sha256:70f851367f687fd4db17c04dc02a75b417cdb7a18c3bf70b7a00292fa8e33939`  
		Last Modified: Tue, 02 Dec 2025 03:08:14 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-cli`

```console
$ docker pull docker@sha256:b6b6bfc4ba4c55a1e921d6d37e4d6e11dd3d6c73e9e7e4a712371ace91e6c106
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

### `docker:29.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:06d66076bb85261b052f4b1fdf594cb94a90666282d19d1c8950e40f58a856d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75449058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807a85c29587d39053f60ea09e02d190f569f0becaf9cd592f2b77afa92b4d69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:08:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bca2c07d80098fe1c61e0aa26eac435752d6dca6a2d3837735a2f68eedd27f`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 8.2 MB (8232306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c13c6aae9df8eeb1b8fe904cbdc67165e49d9f6ca682577bdee0ff1fddb0e`  
		Last Modified: Tue, 02 Dec 2025 00:08:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbba1101f59cdf058694512346b7fb8aeda578243290fc893ba55d81ac314cd`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 18.8 MB (18762388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc6a25ab2f1cc6386ed9595b9c99245b984bddba79a401ede272b40c8a1d34`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3786f9aa3c17d408a9f2162d158dcac195becac82c72ee0a4b29c43f52649`  
		Last Modified: Tue, 02 Dec 2025 00:08:43 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de8d894975036d476ad31205669d2600d672441a0b78b3d35650f89daf8774`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8318820339c402ec6f7161ee23642657be448d0298de2ca2a4946643e99bf`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fca41ae3f7f0a9e8364572b85d6e7862b0a01a49813320a77b7cca46a3dc67`  
		Last Modified: Tue, 02 Dec 2025 00:08:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:26274226c8c0faadd21be8696f3a311564ad7a4ab1ef384c048553a24d3f0ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916e002882958960262548cbc5346e72669f994ab582698cb9f97c5a25a565e9`

```dockerfile
```

-	Layers:
	-	`sha256:a46ae34aa73068e39fe087bf2583406667a30359eb3f75440314f7c1acb9296a`  
		Last Modified: Tue, 02 Dec 2025 03:08:20 GMT  
		Size: 38.1 KB (38072 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:7dec30a9bddbb6a8022449d724ec7ccb8d72831f641c9318256e13621b115f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71162709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe592527df6e45624d69acd1f08345d80166ac1b721283466fa69b5e70d1fce4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:00:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:01:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:01:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:01:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:01:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:03 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd90142670bbaed6f585f4970fd1d53633e0869fd5272c8e3df77120bace0e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 8.1 MB (8140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642374c76164440ef8b823ab6bba0dd1bee0e2a2376c47bb5f4073a585413e04`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed115a71dbefda1db4593399cccc8dad9b72d92954e97811cb17ea6cbd16029`  
		Last Modified: Tue, 02 Dec 2025 00:01:24 GMT  
		Size: 17.6 MB (17559034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5443b6b267bcc407b81aa1fc56c89a28780986fdb8a6a0e262dc6cb167368cb`  
		Last Modified: Tue, 02 Dec 2025 00:01:23 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1408d4a896b763e6cf9b6eb5321ee325d093c04ddb275e901a85d57735dd87d`  
		Last Modified: Tue, 02 Dec 2025 00:01:21 GMT  
		Size: 20.5 MB (20480374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc905b6a443c6c8096533c447544d946dedb7a2450e9d8815424d25a2b70b5b8`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79661a927ae816f329cd8e6d5aebc5775b45d598f860218a7fa0bf34259fedae`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc8f4aa5c2b729f00263aa5f33b190bedfd7d94a05ac9ccb26f4f1995d10a1e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:59f483c5d14576f6604d8761286ec411d1e4cea808c56c6517fa68aa86482f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7eb9816e4263309859c9fa2544254d266fce016841a6dd9ebb252dfb60b369`

```dockerfile
```

-	Layers:
	-	`sha256:2b4874b8d5341ca253e2d4e4c06cb6938a34fde4eb798103ab4ba8f879527028`  
		Last Modified: Tue, 02 Dec 2025 03:08:23 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:e29562e7b2b07035db21a39fc060357a494d7cfb2aa8e6d1b34cdd2c28492ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70153607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682acbc8a7f3934bc163828bdbf4f86937e5f744b33fe889d224a4e560b25d5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:03:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:03:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:03:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:03:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec0784ecb867af52b79e3f383d52e39182464803fd28c22d49d1ff019df6e4`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 7.5 MB (7461368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491247472d55430402882837b71580b20d49d688f85f713917e74b9c4dcfa29`  
		Last Modified: Tue, 02 Dec 2025 00:03:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681ac3424d8a722d9e60118306e4292f0558f8234066431fcf35fe24394a1bb8`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 17.6 MB (17550851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4ccba3516b05ed1ea12fcc5ff93f84c20331f6098765bc58aa14342452b044`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01cc08290b32581069106ced2f3f3eb8ee944803bea261cb440c95a59f3e88`  
		Last Modified: Tue, 02 Dec 2025 00:03:52 GMT  
		Size: 20.5 MB (20462776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3320b40de969faa831b8c731ba2d0e1b46c0099f07df033d271e79b3ae90cfa`  
		Last Modified: Tue, 02 Dec 2025 00:03:49 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6f871522091994e48824cf572b17680f5f65920875e93a33820ca79643cb83`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccd637b5bd3f36088e619e2cd9af1073d6cf18b4daae90c18da0bebaac04039`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2a42b7168acc8dd7465a298f656d13b5ef3da6a4e4a802e7c2f758b3b87528fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d110713e939ebab1bfb3791674c56ccdb6a71e216860021350b985431c1398`

```dockerfile
```

-	Layers:
	-	`sha256:e3979750bdc58314c6ed89fe981aa70da96caf2931e7efe401364b9464cc2e37`  
		Last Modified: Tue, 02 Dec 2025 03:08:26 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:056f1c5ae751413a3801dc2a11917de4e3278964a995f552292e55b588a32db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70243742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b329681fa645f06008f07c64da4c89ed70718d7a45714e322d215dedb1ace80a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:02:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:02:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:02:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:02:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:02:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:02:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8d6f5f280f3c754fdf75be610b9eaad7ee272876c0223bf2f3bd9a69fa411`  
		Last Modified: Tue, 02 Dec 2025 00:03:11 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e82d4d488e2618905f471024c5fe4d2e766267d8f3348b3dd7b6191630216`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f10b7b7acafc5f4d720b74cd91450008c1662de4a06650c39d1fb60537c2a6`  
		Last Modified: Tue, 02 Dec 2025 00:03:14 GMT  
		Size: 17.3 MB (17331274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53231739b67e10b4afa5aed2ecd60407f25e184a679cdbb1b5be2acafe29cc00`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c895eab34015734e14c5a975b34482844ee37ed6cae5b06a56089d9240b3`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 19.9 MB (19869837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549587bc62ff6067012fffc4124531c681e33704d75b4332e354e8e8c7ac9e94`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015487da6372d9bb9ef8a815c66c71f3c29cdd4a5dcaee2f5e87280d9717f00`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25860a630a1731a13c772ef03361714d3807678f3549f006ebe44c22140700b`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7da5ae430420c1356c0bd6c28cbcbaad830ffe49f10f32553ae5a481daa8b7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2bc66f36721e245c614fa122147d157eb29e4a89b1d28c8819d7d789616898`

```dockerfile
```

-	Layers:
	-	`sha256:377912c6134d900c01b748697784d6625f52f655404bcc8267902a5e62ab31c7`  
		Last Modified: Tue, 02 Dec 2025 03:08:29 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-dind`

```console
$ docker pull docker@sha256:9b20eb23e1f0443655673efb9db76c4b18cc1b45de1fcf82b3c1b749b9647bdf
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

### `docker:29.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:e7722a3fdf461a91095cc11b6751da7e69a1bdd583df23b5837cd03bc3dcbf11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146834840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3d6683ede5a5e31409999791e15e1785c65344da6483593dd3af23c29bd562`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:08:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:07 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:35:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:35:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:35:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:35:13 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bca2c07d80098fe1c61e0aa26eac435752d6dca6a2d3837735a2f68eedd27f`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 8.2 MB (8232306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c13c6aae9df8eeb1b8fe904cbdc67165e49d9f6ca682577bdee0ff1fddb0e`  
		Last Modified: Tue, 02 Dec 2025 00:08:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbba1101f59cdf058694512346b7fb8aeda578243290fc893ba55d81ac314cd`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 18.8 MB (18762388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc6a25ab2f1cc6386ed9595b9c99245b984bddba79a401ede272b40c8a1d34`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3786f9aa3c17d408a9f2162d158dcac195becac82c72ee0a4b29c43f52649`  
		Last Modified: Tue, 02 Dec 2025 00:08:43 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de8d894975036d476ad31205669d2600d672441a0b78b3d35650f89daf8774`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8318820339c402ec6f7161ee23642657be448d0298de2ca2a4946643e99bf`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fca41ae3f7f0a9e8364572b85d6e7862b0a01a49813320a77b7cca46a3dc67`  
		Last Modified: Tue, 02 Dec 2025 00:08:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eaeb7e3ff54863b596ddf45aa1f53fe06b5bac153cd3057038bca861e20c27`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 6.9 MB (6905410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568debdaab006707818488bd30ccbe9d028b275d05c6ce65dd3b1aec6ecdd841`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6f1c21ebbe286ed54f5e70396d9124048a5aab0e142aa1b81824ff82ace94`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b638749a1ad920d398a23428bd3e49a14bdf1b01a65776444264fa6afec6effd`  
		Last Modified: Tue, 02 Dec 2025 00:36:12 GMT  
		Size: 64.4 MB (64383976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4c76068297a0e5e2b8b3f4b582b62ec0bd167377a14e5e849d084838dd7d65`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831f7baf80344c1ea02c8259ab473f8c112481bf3ba30f27311a27ae615a6ba9`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b3ffbc635daa4785c6e8540daa89e290342d9ce7574d182f603904c844e2ae55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cddfa71d427c6ffde929b85b3ac597a723b864fa7b755fb7e2b38bffcec4abf`

```dockerfile
```

-	Layers:
	-	`sha256:c293678f6e88a59d70f255b8b2d4d5370350c49c9cac522deee7e1ca928a771f`  
		Last Modified: Tue, 02 Dec 2025 03:08:05 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f4264dc6f53bf84c143abcd79f054061e949f91297519b16342df3b0fcf515d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138377571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5525feeb0b6b1996748694f01b24cce0d9825880fcc090ceaec227482995adb8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:00:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:01:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:01:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:01:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:01:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:03 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:08:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:08:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:08:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:08:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:08:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:08:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:47 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd90142670bbaed6f585f4970fd1d53633e0869fd5272c8e3df77120bace0e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 8.1 MB (8140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642374c76164440ef8b823ab6bba0dd1bee0e2a2376c47bb5f4073a585413e04`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed115a71dbefda1db4593399cccc8dad9b72d92954e97811cb17ea6cbd16029`  
		Last Modified: Tue, 02 Dec 2025 00:01:24 GMT  
		Size: 17.6 MB (17559034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5443b6b267bcc407b81aa1fc56c89a28780986fdb8a6a0e262dc6cb167368cb`  
		Last Modified: Tue, 02 Dec 2025 00:01:23 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1408d4a896b763e6cf9b6eb5321ee325d093c04ddb275e901a85d57735dd87d`  
		Last Modified: Tue, 02 Dec 2025 00:01:21 GMT  
		Size: 20.5 MB (20480374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc905b6a443c6c8096533c447544d946dedb7a2450e9d8815424d25a2b70b5b8`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79661a927ae816f329cd8e6d5aebc5775b45d598f860218a7fa0bf34259fedae`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc8f4aa5c2b729f00263aa5f33b190bedfd7d94a05ac9ccb26f4f1995d10a1e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f114e86733f934e05b8cc095e26ac7d23df0400c164367a5d0960c90ffbb7e7`  
		Last Modified: Tue, 02 Dec 2025 00:09:22 GMT  
		Size: 7.2 MB (7230316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52de536e5339daea653f15c27e78b4cf16e12a10d82ef4f286872bc4f4aafd9`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 90.0 KB (89961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae860099f824f4d5c845c472dccead8faa86f1afc2773e064de55ac8317fa514`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99458a7fe0e1036a55a30274f0e06e8baa5da805dac7a2d7f788bf02c9531c18`  
		Last Modified: Tue, 02 Dec 2025 00:09:30 GMT  
		Size: 59.9 MB (59888589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bba7682b037f71b8aea88b0676d075b4bcd35fa3390b95b1bd864d4999afb7d`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed47c75bfd062f331a396b716966fb250ee7485fee132a7b2942e732842fbf3`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ec56f63d4804233c364f31addc653c748a9b7e58cc1b72a68562b7cfd4f5869d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3125bbdfa07949727984336157b0367e420ed260fb1153f6a4ac86374835df20`

```dockerfile
```

-	Layers:
	-	`sha256:e35660952afa463bcd149750757d217195b0afeb78547aeae6aecaf7697b4b82`  
		Last Modified: Tue, 02 Dec 2025 03:08:08 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:4c9e1d32783f3091ec573930696e1a02680c8b2e0a96588960e8cfb4785f0987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136499855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a132a67d9b1e15c2a6b6b5072baf4669d91a4c94c59594cde5e134a3f13f7e0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:03:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:03:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:03:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:03:35 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:08:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:08:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:08:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:08:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:08:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:08:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:52 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec0784ecb867af52b79e3f383d52e39182464803fd28c22d49d1ff019df6e4`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 7.5 MB (7461368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491247472d55430402882837b71580b20d49d688f85f713917e74b9c4dcfa29`  
		Last Modified: Tue, 02 Dec 2025 00:03:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681ac3424d8a722d9e60118306e4292f0558f8234066431fcf35fe24394a1bb8`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 17.6 MB (17550851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4ccba3516b05ed1ea12fcc5ff93f84c20331f6098765bc58aa14342452b044`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01cc08290b32581069106ced2f3f3eb8ee944803bea261cb440c95a59f3e88`  
		Last Modified: Tue, 02 Dec 2025 00:03:52 GMT  
		Size: 20.5 MB (20462776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3320b40de969faa831b8c731ba2d0e1b46c0099f07df033d271e79b3ae90cfa`  
		Last Modified: Tue, 02 Dec 2025 00:03:49 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6f871522091994e48824cf572b17680f5f65920875e93a33820ca79643cb83`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccd637b5bd3f36088e619e2cd9af1073d6cf18b4daae90c18da0bebaac04039`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fedb293900f104824c5bf607d49531816ebb696de67d2349e25c3b7235c7d4`  
		Last Modified: Tue, 02 Dec 2025 03:08:37 GMT  
		Size: 6.5 MB (6538170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f3efb3e0b8e692ee930467452c2b90850e32de6e81f525c8b5ecb809596cb1`  
		Last Modified: Tue, 02 Dec 2025 01:10:44 GMT  
		Size: 86.4 KB (86397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6a05cebb7258e8cc03a59c4ddbfab058b79a4254d47f5f7339c3cbb66e0f91`  
		Last Modified: Tue, 02 Dec 2025 01:10:45 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2700c9375899dc20256cee56347f7a94685712635d0a083c74baf5a4d0ac5809`  
		Last Modified: Tue, 02 Dec 2025 03:08:48 GMT  
		Size: 59.7 MB (59715683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f83379703e2b0dd6765daef6f82dba3e582ae979b57dfd62b9101c915e244`  
		Last Modified: Tue, 02 Dec 2025 01:10:48 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fb0afbbc9ea4bc8903a6671f34110ef481952a81c388cc585e9b21cd7f4e21`  
		Last Modified: Tue, 02 Dec 2025 01:10:44 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:81b93d08f8b08b14411acfcfd4683554ff94f1553aa1c42bb33bb2e43d453ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db32ac5181c3e6cf95fea47b5846cd4a761768ec6dc895055994af29bcb7718b`

```dockerfile
```

-	Layers:
	-	`sha256:9f6b2982982b5b6659faac06d4632eb9f834c5522239d5ab3c1c0c340c2664f7`  
		Last Modified: Tue, 02 Dec 2025 03:08:11 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:37269ed2d81f5f6d65910acc46f07807e7027efa4560c03b5c2c427c57b5b99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135915031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cb9c89488e9663f2162c6982870ff63ce946066edbedbf787cccfcb650d4a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:02:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:02:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:02:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:02:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:02:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:02:56 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:10:29 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:10:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:10:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:10:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:10:33 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8d6f5f280f3c754fdf75be610b9eaad7ee272876c0223bf2f3bd9a69fa411`  
		Last Modified: Tue, 02 Dec 2025 00:03:11 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e82d4d488e2618905f471024c5fe4d2e766267d8f3348b3dd7b6191630216`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f10b7b7acafc5f4d720b74cd91450008c1662de4a06650c39d1fb60537c2a6`  
		Last Modified: Tue, 02 Dec 2025 00:03:14 GMT  
		Size: 17.3 MB (17331274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53231739b67e10b4afa5aed2ecd60407f25e184a679cdbb1b5be2acafe29cc00`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c895eab34015734e14c5a975b34482844ee37ed6cae5b06a56089d9240b3`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 19.9 MB (19869837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549587bc62ff6067012fffc4124531c681e33704d75b4332e354e8e8c7ac9e94`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015487da6372d9bb9ef8a815c66c71f3c29cdd4a5dcaee2f5e87280d9717f00`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25860a630a1731a13c772ef03361714d3807678f3549f006ebe44c22140700b`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ac678ddec83e4354555da6ef9579f4ef2f9988789f66f9a5ca00e87db6b54`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 7.1 MB (7140876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8cd171770863e9348d4ee8c70d82ad8f289d2f4c1d388c224940feff19e47a`  
		Last Modified: Tue, 02 Dec 2025 00:11:01 GMT  
		Size: 99.5 KB (99516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5c60c1c2283f8e5a61f9ffda4011e80b738fd729f6732471650d647f62cb9`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c4891a520b352f266fdd87afc53d295cf90939a3cf3161134eee0a9f36e1d`  
		Last Modified: Tue, 02 Dec 2025 00:11:17 GMT  
		Size: 58.4 MB (58424894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d5d9da598fa4548678e746eb3de0f80e0197dc4482495dd269b371f4ab250`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ddcdacde67a928d9cfcb6dafce29f04eeb8bff016e6cd2756fea0f8a499d79`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:69a58a45b2f2152765e4d687b8e3006251f085c64eb9a725cd9562931e90989d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba11b7f0671e0843042aae85daa5eec651de997c5be2739f8d372d98a5fe0674`

```dockerfile
```

-	Layers:
	-	`sha256:70f851367f687fd4db17c04dc02a75b417cdb7a18c3bf70b7a00292fa8e33939`  
		Last Modified: Tue, 02 Dec 2025 03:08:14 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-dind-rootless`

```console
$ docker pull docker@sha256:26d283e4272e65c34bec8b7703698f75583b470b7fa5d6ac7b0544632dcdc74d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:4d55728f99b9642731991198ac30737ae9269d10e0d4721f798d1a6c7b6b6646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167604793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f500029a797b09b09f16482f6fd1be288c57d9355fc7176acea27545f24040aa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:08:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:07 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:35:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:35:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:35:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:35:13 GMT
CMD []
# Tue, 02 Dec 2025 01:04:33 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 02 Dec 2025 01:04:33 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 02 Dec 2025 01:04:33 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 01:04:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 02 Dec 2025 01:04:34 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 02 Dec 2025 01:04:34 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 02 Dec 2025 01:04:34 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bca2c07d80098fe1c61e0aa26eac435752d6dca6a2d3837735a2f68eedd27f`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 8.2 MB (8232306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c13c6aae9df8eeb1b8fe904cbdc67165e49d9f6ca682577bdee0ff1fddb0e`  
		Last Modified: Tue, 02 Dec 2025 00:08:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbba1101f59cdf058694512346b7fb8aeda578243290fc893ba55d81ac314cd`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 18.8 MB (18762388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc6a25ab2f1cc6386ed9595b9c99245b984bddba79a401ede272b40c8a1d34`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3786f9aa3c17d408a9f2162d158dcac195becac82c72ee0a4b29c43f52649`  
		Last Modified: Tue, 02 Dec 2025 00:08:43 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de8d894975036d476ad31205669d2600d672441a0b78b3d35650f89daf8774`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8318820339c402ec6f7161ee23642657be448d0298de2ca2a4946643e99bf`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fca41ae3f7f0a9e8364572b85d6e7862b0a01a49813320a77b7cca46a3dc67`  
		Last Modified: Tue, 02 Dec 2025 00:08:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eaeb7e3ff54863b596ddf45aa1f53fe06b5bac153cd3057038bca861e20c27`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 6.9 MB (6905410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568debdaab006707818488bd30ccbe9d028b275d05c6ce65dd3b1aec6ecdd841`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6f1c21ebbe286ed54f5e70396d9124048a5aab0e142aa1b81824ff82ace94`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b638749a1ad920d398a23428bd3e49a14bdf1b01a65776444264fa6afec6effd`  
		Last Modified: Tue, 02 Dec 2025 00:36:12 GMT  
		Size: 64.4 MB (64383976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4c76068297a0e5e2b8b3f4b582b62ec0bd167377a14e5e849d084838dd7d65`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831f7baf80344c1ea02c8259ab473f8c112481bf3ba30f27311a27ae615a6ba9`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6ab179a37092cfe7a4ed7e56cfaa4245be172a64fa8983225d912989c5fcc5`  
		Last Modified: Tue, 02 Dec 2025 01:04:49 GMT  
		Size: 3.4 MB (3398376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff83acf3702948a722e974d3dfc0a3282ac4ea70c4b2338b9a522e2544f1ade5`  
		Last Modified: Tue, 02 Dec 2025 01:04:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef24dccdc8e52bba4677dc83acf458b27fc0ee05e8023ff60cd3092c847448a`  
		Last Modified: Tue, 02 Dec 2025 01:04:49 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675547768fa484d1c34426e57586edd545c80c258f8ee3b1daad209973a18e39`  
		Last Modified: Tue, 02 Dec 2025 01:04:52 GMT  
		Size: 17.4 MB (17370238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6970303a67916649ea0e564b703347d9b6d63a5499fd2317d7bc25825bac820e`  
		Last Modified: Tue, 02 Dec 2025 01:04:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:eb319559cabdac9b6d6e61682add0ddd92bc4a1f016e42cb5cb54cb4406e18fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8a901677136393b67572d4d6f9bc5a7138099f768ffa584d6a047f88e97c1f`

```dockerfile
```

-	Layers:
	-	`sha256:a3186791ef27178f63f3334dcbdf3618a5894a1a04a580d19d58df0aad0c51f6`  
		Last Modified: Tue, 02 Dec 2025 03:08:36 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:500d9983f84e3c1918053364b152d6c8678606181d1b47f39e6e56325f88a4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157013358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259bf946645a41d2af38ec03e3dbc71a98181d2ae1e3f4953a1d790b71712216`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:02:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:02:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:02:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:02:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:02:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:02:56 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:10:29 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:10:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:10:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:10:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:10:33 GMT
CMD []
# Tue, 02 Dec 2025 00:16:44 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 02 Dec 2025 00:16:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 02 Dec 2025 00:16:44 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:16:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 02 Dec 2025 00:16:45 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 02 Dec 2025 00:16:45 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 02 Dec 2025 00:16:45 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8d6f5f280f3c754fdf75be610b9eaad7ee272876c0223bf2f3bd9a69fa411`  
		Last Modified: Tue, 02 Dec 2025 00:03:11 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e82d4d488e2618905f471024c5fe4d2e766267d8f3348b3dd7b6191630216`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f10b7b7acafc5f4d720b74cd91450008c1662de4a06650c39d1fb60537c2a6`  
		Last Modified: Tue, 02 Dec 2025 00:03:14 GMT  
		Size: 17.3 MB (17331274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53231739b67e10b4afa5aed2ecd60407f25e184a679cdbb1b5be2acafe29cc00`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c895eab34015734e14c5a975b34482844ee37ed6cae5b06a56089d9240b3`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 19.9 MB (19869837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549587bc62ff6067012fffc4124531c681e33704d75b4332e354e8e8c7ac9e94`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015487da6372d9bb9ef8a815c66c71f3c29cdd4a5dcaee2f5e87280d9717f00`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25860a630a1731a13c772ef03361714d3807678f3549f006ebe44c22140700b`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ac678ddec83e4354555da6ef9579f4ef2f9988789f66f9a5ca00e87db6b54`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 7.1 MB (7140876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8cd171770863e9348d4ee8c70d82ad8f289d2f4c1d388c224940feff19e47a`  
		Last Modified: Tue, 02 Dec 2025 00:11:01 GMT  
		Size: 99.5 KB (99516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5c60c1c2283f8e5a61f9ffda4011e80b738fd729f6732471650d647f62cb9`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c4891a520b352f266fdd87afc53d295cf90939a3cf3161134eee0a9f36e1d`  
		Last Modified: Tue, 02 Dec 2025 00:11:17 GMT  
		Size: 58.4 MB (58424894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d5d9da598fa4548678e746eb3de0f80e0197dc4482495dd269b371f4ab250`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ddcdacde67a928d9cfcb6dafce29f04eeb8bff016e6cd2756fea0f8a499d79`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763091d1251eb3f132c7b256f6b764c4d0955511bb4d4cfa11a52a3748b983b4`  
		Last Modified: Tue, 02 Dec 2025 00:17:05 GMT  
		Size: 3.4 MB (3389942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7986a5219667182dcb2d7497f51bcaf7b8358e271f41f0423f8f6665e6e8e27`  
		Last Modified: Tue, 02 Dec 2025 00:17:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2c564976ca2ad686546fe1e57597bd2623c76c3d660e852e930f32acfb7ffc`  
		Last Modified: Tue, 02 Dec 2025 00:17:05 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f8d39c0e9195885f73df58fb87203a86f5600e9372dc7af6c6ced416c50de3`  
		Last Modified: Tue, 02 Dec 2025 00:17:10 GMT  
		Size: 17.7 MB (17707046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b4c481f84d857b2b25d71535d076ec14fe51bf97a7693bb84958d2cc97bc79`  
		Last Modified: Tue, 02 Dec 2025 00:17:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:293f1f699032f6d51172da18bfd76ae3d5160bae1b22229359b445b35e2f27e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8a0d27bc916671f250df0b710a855e84e8aa12c157c41c5e1ac989214fcadd`

```dockerfile
```

-	Layers:
	-	`sha256:43e535d7855d564532284ba0cc7bd59b7a8ba7a0be76ae888afdda1ac9c29482`  
		Last Modified: Tue, 02 Dec 2025 03:08:39 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-windowsservercore`

```console
$ docker pull docker@sha256:1c43c735429614f250536aac0dd2c328e6d0b893b299c60a260849bf484844e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:29.1-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:edb55a55a9709f716094eff0d619f5cccfbe7ab9c820d4cd94316a3dc80f85b0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301942510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd431f71a41f9ca0d66fa3490028ce3378094dc608e876e5a5e01d5f1c00a85`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 02 Dec 2025 00:02:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:03:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:03:18 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:03:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:03:38 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:03:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:03:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1274f6d3b6ceaa195acd16a17546b93878ef3c76e6b0c0ea475532ae81138829`  
		Last Modified: Tue, 02 Dec 2025 00:29:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18719cadfdf416a79dc2e3958aaaa04ba5f00625ff6e93ab3dec72cf2f51da`  
		Last Modified: Tue, 02 Dec 2025 00:29:25 GMT  
		Size: 394.4 KB (394389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacb90f7314fdc946208b5f3ff65f6c72d6649551c978d26418bda8d9e5a6890`  
		Last Modified: Tue, 02 Dec 2025 00:29:30 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad66afc50aa529e50d970dea5d3e8f437aab69ad9cb3882a256d4319b5b42d15`  
		Last Modified: Tue, 02 Dec 2025 00:29:33 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b85b05963e8f44359d0370018251cb0af969ffdbeeb8b5a7d16e32fa4e6e0`  
		Last Modified: Tue, 02 Dec 2025 01:01:49 GMT  
		Size: 19.4 MB (19445634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4369b8ed94ba65d95a6942b0a54d8302024faae5688bd932577bcc256abefee3`  
		Last Modified: Tue, 02 Dec 2025 00:29:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a49cd2f3d1017e97f6ed405d89cd3d09949977cd4e8b5b34fdb146b8da04a3`  
		Last Modified: Tue, 02 Dec 2025 00:29:41 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f583f8eec952d8c1f2b32d817e3b14c51c57780bc726d9eb1c393555075ba3c7`  
		Last Modified: Tue, 02 Dec 2025 00:29:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9def44a99f4bab2dcc70f25abcf502cbafd84b76181171949b51aa186814cce8`  
		Last Modified: Tue, 02 Dec 2025 01:01:52 GMT  
		Size: 23.9 MB (23942612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46335ebb4377421068829028c4feca1ce21bb336ddc77ffaff4cf2fdd07669d`  
		Last Modified: Tue, 02 Dec 2025 00:29:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6700c7401706484942b62f39837e732625ea2eae796316fd97da557c97d9a2bd`  
		Last Modified: Tue, 02 Dec 2025 00:29:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fcde18a4abb110b9720f6357dc8098af919dc2247e1fcb902d2dbce1dc2bbb`  
		Last Modified: Tue, 02 Dec 2025 00:29:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a06df7c12fbd246e254cc1c5ccda1ea8a3064c55627e865f6c813204a155a`  
		Last Modified: Tue, 02 Dec 2025 01:01:55 GMT  
		Size: 22.7 MB (22692302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.1-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:59fd73de957de338aebfa44cbc56e9e613995025b25e51d83b83c144f5f15828
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836458539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb88b8d8055f99a033e38f88e5335522379ea547e8004051da7417b42321791`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 02 Dec 2025 00:09:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:10:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:10:58 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:11:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:11:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:11:29 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:11:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:11:32 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:11:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:11:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:11:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:12:00 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:12:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca80c7273175042e00fe42b9acc4273bb878eee0a0c4c5fa397b7397b8841b60`  
		Last Modified: Tue, 02 Dec 2025 00:27:05 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de920d113346f7751e223cc4f56c9ac711e693c7bbad0a62661edd7a13e3cb18`  
		Last Modified: Tue, 02 Dec 2025 00:27:06 GMT  
		Size: 518.9 KB (518913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4006e793c124c40f2cd2b04d3620d9d0701f4a8b6b235a461ac6bf489cfee31`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b20b11149feeb6be69bcded688660b34c2ff915411a4a073b5a67b8511a88e`  
		Last Modified: Tue, 02 Dec 2025 00:27:07 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f920b83c504a555c3b5c26902e6a1ec22ef2c88c9afba067de16269b6f0429`  
		Last Modified: Tue, 02 Dec 2025 00:27:10 GMT  
		Size: 19.4 MB (19406772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf9e2e8b9aa98bf5c8b54f2bc38c78ea68496c411e4620b1762bd486b251406`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e633a60820512a97163b768f578d2ed4c4d4e6a403d9a260fc3625581aee37d6`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c418e2d05c842f6856d59f8030e8c3b42bc6d2060d9185961466724fb8ebb259`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cefba9d08372f4b315b8a9b066b2e795c2a6f31473405639443e63a3a13cb4e`  
		Last Modified: Tue, 02 Dec 2025 00:27:12 GMT  
		Size: 23.9 MB (23905567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9c528564d3c90f5342ffbe261f0e02cc558cd11bb1c2cda3901acce07c071e`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac38da0772c85387d94e42b5ac044035676912ba7b05c906b2b267f10c2c0e10`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90916836d70bec2b5e65b639f5ebfb46be73741a370798dee04edb8ee868a44b`  
		Last Modified: Tue, 02 Dec 2025 00:27:12 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42bcb722bb6159035d26e8273c1451882c9adf5073c21bba4efbc06e42c5f68`  
		Last Modified: Tue, 02 Dec 2025 00:27:14 GMT  
		Size: 22.7 MB (22653934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:da10f7e9be92554d35616813bc89c43489e9d0568b3682aa5dd4c573ce5e9a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:29.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:59fd73de957de338aebfa44cbc56e9e613995025b25e51d83b83c144f5f15828
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836458539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb88b8d8055f99a033e38f88e5335522379ea547e8004051da7417b42321791`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 02 Dec 2025 00:09:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:10:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:10:58 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:11:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:11:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:11:29 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:11:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:11:32 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:11:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:11:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:11:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:12:00 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:12:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca80c7273175042e00fe42b9acc4273bb878eee0a0c4c5fa397b7397b8841b60`  
		Last Modified: Tue, 02 Dec 2025 00:27:05 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de920d113346f7751e223cc4f56c9ac711e693c7bbad0a62661edd7a13e3cb18`  
		Last Modified: Tue, 02 Dec 2025 00:27:06 GMT  
		Size: 518.9 KB (518913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4006e793c124c40f2cd2b04d3620d9d0701f4a8b6b235a461ac6bf489cfee31`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b20b11149feeb6be69bcded688660b34c2ff915411a4a073b5a67b8511a88e`  
		Last Modified: Tue, 02 Dec 2025 00:27:07 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f920b83c504a555c3b5c26902e6a1ec22ef2c88c9afba067de16269b6f0429`  
		Last Modified: Tue, 02 Dec 2025 00:27:10 GMT  
		Size: 19.4 MB (19406772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf9e2e8b9aa98bf5c8b54f2bc38c78ea68496c411e4620b1762bd486b251406`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e633a60820512a97163b768f578d2ed4c4d4e6a403d9a260fc3625581aee37d6`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c418e2d05c842f6856d59f8030e8c3b42bc6d2060d9185961466724fb8ebb259`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cefba9d08372f4b315b8a9b066b2e795c2a6f31473405639443e63a3a13cb4e`  
		Last Modified: Tue, 02 Dec 2025 00:27:12 GMT  
		Size: 23.9 MB (23905567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9c528564d3c90f5342ffbe261f0e02cc558cd11bb1c2cda3901acce07c071e`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac38da0772c85387d94e42b5ac044035676912ba7b05c906b2b267f10c2c0e10`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90916836d70bec2b5e65b639f5ebfb46be73741a370798dee04edb8ee868a44b`  
		Last Modified: Tue, 02 Dec 2025 00:27:12 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42bcb722bb6159035d26e8273c1451882c9adf5073c21bba4efbc06e42c5f68`  
		Last Modified: Tue, 02 Dec 2025 00:27:14 GMT  
		Size: 22.7 MB (22653934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:5e399dd5dd0dfe81579a2bca9462ce91fd0af47c6c1f7a6b73ffbc942907f790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:29.1-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:edb55a55a9709f716094eff0d619f5cccfbe7ab9c820d4cd94316a3dc80f85b0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301942510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd431f71a41f9ca0d66fa3490028ce3378094dc608e876e5a5e01d5f1c00a85`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 02 Dec 2025 00:02:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:03:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:03:18 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:03:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:03:38 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:03:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:03:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1274f6d3b6ceaa195acd16a17546b93878ef3c76e6b0c0ea475532ae81138829`  
		Last Modified: Tue, 02 Dec 2025 00:29:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18719cadfdf416a79dc2e3958aaaa04ba5f00625ff6e93ab3dec72cf2f51da`  
		Last Modified: Tue, 02 Dec 2025 00:29:25 GMT  
		Size: 394.4 KB (394389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacb90f7314fdc946208b5f3ff65f6c72d6649551c978d26418bda8d9e5a6890`  
		Last Modified: Tue, 02 Dec 2025 00:29:30 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad66afc50aa529e50d970dea5d3e8f437aab69ad9cb3882a256d4319b5b42d15`  
		Last Modified: Tue, 02 Dec 2025 00:29:33 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b85b05963e8f44359d0370018251cb0af969ffdbeeb8b5a7d16e32fa4e6e0`  
		Last Modified: Tue, 02 Dec 2025 01:01:49 GMT  
		Size: 19.4 MB (19445634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4369b8ed94ba65d95a6942b0a54d8302024faae5688bd932577bcc256abefee3`  
		Last Modified: Tue, 02 Dec 2025 00:29:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a49cd2f3d1017e97f6ed405d89cd3d09949977cd4e8b5b34fdb146b8da04a3`  
		Last Modified: Tue, 02 Dec 2025 00:29:41 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f583f8eec952d8c1f2b32d817e3b14c51c57780bc726d9eb1c393555075ba3c7`  
		Last Modified: Tue, 02 Dec 2025 00:29:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9def44a99f4bab2dcc70f25abcf502cbafd84b76181171949b51aa186814cce8`  
		Last Modified: Tue, 02 Dec 2025 01:01:52 GMT  
		Size: 23.9 MB (23942612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46335ebb4377421068829028c4feca1ce21bb336ddc77ffaff4cf2fdd07669d`  
		Last Modified: Tue, 02 Dec 2025 00:29:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6700c7401706484942b62f39837e732625ea2eae796316fd97da557c97d9a2bd`  
		Last Modified: Tue, 02 Dec 2025 00:29:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fcde18a4abb110b9720f6357dc8098af919dc2247e1fcb902d2dbce1dc2bbb`  
		Last Modified: Tue, 02 Dec 2025 00:29:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a06df7c12fbd246e254cc1c5ccda1ea8a3064c55627e865f6c813204a155a`  
		Last Modified: Tue, 02 Dec 2025 01:01:55 GMT  
		Size: 22.7 MB (22692302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1.2`

**does not exist** (yet?)

## `docker:29.1.2-alpine3.22`

**does not exist** (yet?)

## `docker:29.1.2-cli`

**does not exist** (yet?)

## `docker:29.1.2-cli-alpine3.22`

**does not exist** (yet?)

## `docker:29.1.2-dind`

**does not exist** (yet?)

## `docker:29.1.2-dind-alpine3.22`

**does not exist** (yet?)

## `docker:29.1.2-dind-rootless`

**does not exist** (yet?)

## `docker:29.1.2-windowsservercore`

**does not exist** (yet?)

## `docker:29.1.2-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:29.1.2-windowsservercore-ltsc2025`

**does not exist** (yet?)

## `docker:cli`

```console
$ docker pull docker@sha256:b6b6bfc4ba4c55a1e921d6d37e4d6e11dd3d6c73e9e7e4a712371ace91e6c106
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
$ docker pull docker@sha256:06d66076bb85261b052f4b1fdf594cb94a90666282d19d1c8950e40f58a856d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75449058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807a85c29587d39053f60ea09e02d190f569f0becaf9cd592f2b77afa92b4d69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:08:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bca2c07d80098fe1c61e0aa26eac435752d6dca6a2d3837735a2f68eedd27f`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 8.2 MB (8232306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c13c6aae9df8eeb1b8fe904cbdc67165e49d9f6ca682577bdee0ff1fddb0e`  
		Last Modified: Tue, 02 Dec 2025 00:08:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbba1101f59cdf058694512346b7fb8aeda578243290fc893ba55d81ac314cd`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 18.8 MB (18762388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc6a25ab2f1cc6386ed9595b9c99245b984bddba79a401ede272b40c8a1d34`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3786f9aa3c17d408a9f2162d158dcac195becac82c72ee0a4b29c43f52649`  
		Last Modified: Tue, 02 Dec 2025 00:08:43 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de8d894975036d476ad31205669d2600d672441a0b78b3d35650f89daf8774`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8318820339c402ec6f7161ee23642657be448d0298de2ca2a4946643e99bf`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fca41ae3f7f0a9e8364572b85d6e7862b0a01a49813320a77b7cca46a3dc67`  
		Last Modified: Tue, 02 Dec 2025 00:08:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:26274226c8c0faadd21be8696f3a311564ad7a4ab1ef384c048553a24d3f0ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916e002882958960262548cbc5346e72669f994ab582698cb9f97c5a25a565e9`

```dockerfile
```

-	Layers:
	-	`sha256:a46ae34aa73068e39fe087bf2583406667a30359eb3f75440314f7c1acb9296a`  
		Last Modified: Tue, 02 Dec 2025 03:08:20 GMT  
		Size: 38.1 KB (38072 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:7dec30a9bddbb6a8022449d724ec7ccb8d72831f641c9318256e13621b115f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71162709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe592527df6e45624d69acd1f08345d80166ac1b721283466fa69b5e70d1fce4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:00:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:01:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:01:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:01:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:01:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:03 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd90142670bbaed6f585f4970fd1d53633e0869fd5272c8e3df77120bace0e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 8.1 MB (8140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642374c76164440ef8b823ab6bba0dd1bee0e2a2376c47bb5f4073a585413e04`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed115a71dbefda1db4593399cccc8dad9b72d92954e97811cb17ea6cbd16029`  
		Last Modified: Tue, 02 Dec 2025 00:01:24 GMT  
		Size: 17.6 MB (17559034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5443b6b267bcc407b81aa1fc56c89a28780986fdb8a6a0e262dc6cb167368cb`  
		Last Modified: Tue, 02 Dec 2025 00:01:23 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1408d4a896b763e6cf9b6eb5321ee325d093c04ddb275e901a85d57735dd87d`  
		Last Modified: Tue, 02 Dec 2025 00:01:21 GMT  
		Size: 20.5 MB (20480374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc905b6a443c6c8096533c447544d946dedb7a2450e9d8815424d25a2b70b5b8`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79661a927ae816f329cd8e6d5aebc5775b45d598f860218a7fa0bf34259fedae`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc8f4aa5c2b729f00263aa5f33b190bedfd7d94a05ac9ccb26f4f1995d10a1e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:59f483c5d14576f6604d8761286ec411d1e4cea808c56c6517fa68aa86482f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7eb9816e4263309859c9fa2544254d266fce016841a6dd9ebb252dfb60b369`

```dockerfile
```

-	Layers:
	-	`sha256:2b4874b8d5341ca253e2d4e4c06cb6938a34fde4eb798103ab4ba8f879527028`  
		Last Modified: Tue, 02 Dec 2025 03:08:23 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:e29562e7b2b07035db21a39fc060357a494d7cfb2aa8e6d1b34cdd2c28492ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70153607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682acbc8a7f3934bc163828bdbf4f86937e5f744b33fe889d224a4e560b25d5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:03:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:03:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:03:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:03:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec0784ecb867af52b79e3f383d52e39182464803fd28c22d49d1ff019df6e4`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 7.5 MB (7461368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491247472d55430402882837b71580b20d49d688f85f713917e74b9c4dcfa29`  
		Last Modified: Tue, 02 Dec 2025 00:03:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681ac3424d8a722d9e60118306e4292f0558f8234066431fcf35fe24394a1bb8`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 17.6 MB (17550851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4ccba3516b05ed1ea12fcc5ff93f84c20331f6098765bc58aa14342452b044`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01cc08290b32581069106ced2f3f3eb8ee944803bea261cb440c95a59f3e88`  
		Last Modified: Tue, 02 Dec 2025 00:03:52 GMT  
		Size: 20.5 MB (20462776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3320b40de969faa831b8c731ba2d0e1b46c0099f07df033d271e79b3ae90cfa`  
		Last Modified: Tue, 02 Dec 2025 00:03:49 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6f871522091994e48824cf572b17680f5f65920875e93a33820ca79643cb83`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccd637b5bd3f36088e619e2cd9af1073d6cf18b4daae90c18da0bebaac04039`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:2a42b7168acc8dd7465a298f656d13b5ef3da6a4e4a802e7c2f758b3b87528fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d110713e939ebab1bfb3791674c56ccdb6a71e216860021350b985431c1398`

```dockerfile
```

-	Layers:
	-	`sha256:e3979750bdc58314c6ed89fe981aa70da96caf2931e7efe401364b9464cc2e37`  
		Last Modified: Tue, 02 Dec 2025 03:08:26 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:056f1c5ae751413a3801dc2a11917de4e3278964a995f552292e55b588a32db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70243742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b329681fa645f06008f07c64da4c89ed70718d7a45714e322d215dedb1ace80a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:02:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:02:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:02:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:02:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:02:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:02:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8d6f5f280f3c754fdf75be610b9eaad7ee272876c0223bf2f3bd9a69fa411`  
		Last Modified: Tue, 02 Dec 2025 00:03:11 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e82d4d488e2618905f471024c5fe4d2e766267d8f3348b3dd7b6191630216`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f10b7b7acafc5f4d720b74cd91450008c1662de4a06650c39d1fb60537c2a6`  
		Last Modified: Tue, 02 Dec 2025 00:03:14 GMT  
		Size: 17.3 MB (17331274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53231739b67e10b4afa5aed2ecd60407f25e184a679cdbb1b5be2acafe29cc00`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c895eab34015734e14c5a975b34482844ee37ed6cae5b06a56089d9240b3`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 19.9 MB (19869837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549587bc62ff6067012fffc4124531c681e33704d75b4332e354e8e8c7ac9e94`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015487da6372d9bb9ef8a815c66c71f3c29cdd4a5dcaee2f5e87280d9717f00`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25860a630a1731a13c772ef03361714d3807678f3549f006ebe44c22140700b`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:7da5ae430420c1356c0bd6c28cbcbaad830ffe49f10f32553ae5a481daa8b7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2bc66f36721e245c614fa122147d157eb29e4a89b1d28c8819d7d789616898`

```dockerfile
```

-	Layers:
	-	`sha256:377912c6134d900c01b748697784d6625f52f655404bcc8267902a5e62ab31c7`  
		Last Modified: Tue, 02 Dec 2025 03:08:29 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:9b20eb23e1f0443655673efb9db76c4b18cc1b45de1fcf82b3c1b749b9647bdf
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
$ docker pull docker@sha256:e7722a3fdf461a91095cc11b6751da7e69a1bdd583df23b5837cd03bc3dcbf11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146834840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3d6683ede5a5e31409999791e15e1785c65344da6483593dd3af23c29bd562`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:08:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:07 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:35:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:35:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:35:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:35:13 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bca2c07d80098fe1c61e0aa26eac435752d6dca6a2d3837735a2f68eedd27f`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 8.2 MB (8232306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c13c6aae9df8eeb1b8fe904cbdc67165e49d9f6ca682577bdee0ff1fddb0e`  
		Last Modified: Tue, 02 Dec 2025 00:08:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbba1101f59cdf058694512346b7fb8aeda578243290fc893ba55d81ac314cd`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 18.8 MB (18762388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc6a25ab2f1cc6386ed9595b9c99245b984bddba79a401ede272b40c8a1d34`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3786f9aa3c17d408a9f2162d158dcac195becac82c72ee0a4b29c43f52649`  
		Last Modified: Tue, 02 Dec 2025 00:08:43 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de8d894975036d476ad31205669d2600d672441a0b78b3d35650f89daf8774`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8318820339c402ec6f7161ee23642657be448d0298de2ca2a4946643e99bf`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fca41ae3f7f0a9e8364572b85d6e7862b0a01a49813320a77b7cca46a3dc67`  
		Last Modified: Tue, 02 Dec 2025 00:08:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eaeb7e3ff54863b596ddf45aa1f53fe06b5bac153cd3057038bca861e20c27`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 6.9 MB (6905410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568debdaab006707818488bd30ccbe9d028b275d05c6ce65dd3b1aec6ecdd841`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6f1c21ebbe286ed54f5e70396d9124048a5aab0e142aa1b81824ff82ace94`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b638749a1ad920d398a23428bd3e49a14bdf1b01a65776444264fa6afec6effd`  
		Last Modified: Tue, 02 Dec 2025 00:36:12 GMT  
		Size: 64.4 MB (64383976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4c76068297a0e5e2b8b3f4b582b62ec0bd167377a14e5e849d084838dd7d65`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831f7baf80344c1ea02c8259ab473f8c112481bf3ba30f27311a27ae615a6ba9`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:b3ffbc635daa4785c6e8540daa89e290342d9ce7574d182f603904c844e2ae55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cddfa71d427c6ffde929b85b3ac597a723b864fa7b755fb7e2b38bffcec4abf`

```dockerfile
```

-	Layers:
	-	`sha256:c293678f6e88a59d70f255b8b2d4d5370350c49c9cac522deee7e1ca928a771f`  
		Last Modified: Tue, 02 Dec 2025 03:08:05 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f4264dc6f53bf84c143abcd79f054061e949f91297519b16342df3b0fcf515d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138377571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5525feeb0b6b1996748694f01b24cce0d9825880fcc090ceaec227482995adb8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:00:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:01:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:01:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:01:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:01:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:03 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:08:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:08:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:08:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:08:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:08:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:08:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:47 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd90142670bbaed6f585f4970fd1d53633e0869fd5272c8e3df77120bace0e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 8.1 MB (8140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642374c76164440ef8b823ab6bba0dd1bee0e2a2376c47bb5f4073a585413e04`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed115a71dbefda1db4593399cccc8dad9b72d92954e97811cb17ea6cbd16029`  
		Last Modified: Tue, 02 Dec 2025 00:01:24 GMT  
		Size: 17.6 MB (17559034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5443b6b267bcc407b81aa1fc56c89a28780986fdb8a6a0e262dc6cb167368cb`  
		Last Modified: Tue, 02 Dec 2025 00:01:23 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1408d4a896b763e6cf9b6eb5321ee325d093c04ddb275e901a85d57735dd87d`  
		Last Modified: Tue, 02 Dec 2025 00:01:21 GMT  
		Size: 20.5 MB (20480374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc905b6a443c6c8096533c447544d946dedb7a2450e9d8815424d25a2b70b5b8`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79661a927ae816f329cd8e6d5aebc5775b45d598f860218a7fa0bf34259fedae`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc8f4aa5c2b729f00263aa5f33b190bedfd7d94a05ac9ccb26f4f1995d10a1e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f114e86733f934e05b8cc095e26ac7d23df0400c164367a5d0960c90ffbb7e7`  
		Last Modified: Tue, 02 Dec 2025 00:09:22 GMT  
		Size: 7.2 MB (7230316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52de536e5339daea653f15c27e78b4cf16e12a10d82ef4f286872bc4f4aafd9`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 90.0 KB (89961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae860099f824f4d5c845c472dccead8faa86f1afc2773e064de55ac8317fa514`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99458a7fe0e1036a55a30274f0e06e8baa5da805dac7a2d7f788bf02c9531c18`  
		Last Modified: Tue, 02 Dec 2025 00:09:30 GMT  
		Size: 59.9 MB (59888589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bba7682b037f71b8aea88b0676d075b4bcd35fa3390b95b1bd864d4999afb7d`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed47c75bfd062f331a396b716966fb250ee7485fee132a7b2942e732842fbf3`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:ec56f63d4804233c364f31addc653c748a9b7e58cc1b72a68562b7cfd4f5869d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3125bbdfa07949727984336157b0367e420ed260fb1153f6a4ac86374835df20`

```dockerfile
```

-	Layers:
	-	`sha256:e35660952afa463bcd149750757d217195b0afeb78547aeae6aecaf7697b4b82`  
		Last Modified: Tue, 02 Dec 2025 03:08:08 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:4c9e1d32783f3091ec573930696e1a02680c8b2e0a96588960e8cfb4785f0987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136499855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a132a67d9b1e15c2a6b6b5072baf4669d91a4c94c59594cde5e134a3f13f7e0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:03:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:03:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:03:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:03:35 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:08:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:08:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:08:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:08:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:08:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:08:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:52 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec0784ecb867af52b79e3f383d52e39182464803fd28c22d49d1ff019df6e4`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 7.5 MB (7461368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491247472d55430402882837b71580b20d49d688f85f713917e74b9c4dcfa29`  
		Last Modified: Tue, 02 Dec 2025 00:03:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681ac3424d8a722d9e60118306e4292f0558f8234066431fcf35fe24394a1bb8`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 17.6 MB (17550851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4ccba3516b05ed1ea12fcc5ff93f84c20331f6098765bc58aa14342452b044`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01cc08290b32581069106ced2f3f3eb8ee944803bea261cb440c95a59f3e88`  
		Last Modified: Tue, 02 Dec 2025 00:03:52 GMT  
		Size: 20.5 MB (20462776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3320b40de969faa831b8c731ba2d0e1b46c0099f07df033d271e79b3ae90cfa`  
		Last Modified: Tue, 02 Dec 2025 00:03:49 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6f871522091994e48824cf572b17680f5f65920875e93a33820ca79643cb83`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccd637b5bd3f36088e619e2cd9af1073d6cf18b4daae90c18da0bebaac04039`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fedb293900f104824c5bf607d49531816ebb696de67d2349e25c3b7235c7d4`  
		Last Modified: Tue, 02 Dec 2025 03:08:37 GMT  
		Size: 6.5 MB (6538170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f3efb3e0b8e692ee930467452c2b90850e32de6e81f525c8b5ecb809596cb1`  
		Last Modified: Tue, 02 Dec 2025 01:10:44 GMT  
		Size: 86.4 KB (86397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6a05cebb7258e8cc03a59c4ddbfab058b79a4254d47f5f7339c3cbb66e0f91`  
		Last Modified: Tue, 02 Dec 2025 01:10:45 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2700c9375899dc20256cee56347f7a94685712635d0a083c74baf5a4d0ac5809`  
		Last Modified: Tue, 02 Dec 2025 03:08:48 GMT  
		Size: 59.7 MB (59715683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f83379703e2b0dd6765daef6f82dba3e582ae979b57dfd62b9101c915e244`  
		Last Modified: Tue, 02 Dec 2025 01:10:48 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fb0afbbc9ea4bc8903a6671f34110ef481952a81c388cc585e9b21cd7f4e21`  
		Last Modified: Tue, 02 Dec 2025 01:10:44 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:81b93d08f8b08b14411acfcfd4683554ff94f1553aa1c42bb33bb2e43d453ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db32ac5181c3e6cf95fea47b5846cd4a761768ec6dc895055994af29bcb7718b`

```dockerfile
```

-	Layers:
	-	`sha256:9f6b2982982b5b6659faac06d4632eb9f834c5522239d5ab3c1c0c340c2664f7`  
		Last Modified: Tue, 02 Dec 2025 03:08:11 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:37269ed2d81f5f6d65910acc46f07807e7027efa4560c03b5c2c427c57b5b99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135915031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cb9c89488e9663f2162c6982870ff63ce946066edbedbf787cccfcb650d4a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:02:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:02:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:02:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:02:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:02:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:02:56 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:10:29 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:10:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:10:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:10:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:10:33 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8d6f5f280f3c754fdf75be610b9eaad7ee272876c0223bf2f3bd9a69fa411`  
		Last Modified: Tue, 02 Dec 2025 00:03:11 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e82d4d488e2618905f471024c5fe4d2e766267d8f3348b3dd7b6191630216`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f10b7b7acafc5f4d720b74cd91450008c1662de4a06650c39d1fb60537c2a6`  
		Last Modified: Tue, 02 Dec 2025 00:03:14 GMT  
		Size: 17.3 MB (17331274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53231739b67e10b4afa5aed2ecd60407f25e184a679cdbb1b5be2acafe29cc00`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c895eab34015734e14c5a975b34482844ee37ed6cae5b06a56089d9240b3`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 19.9 MB (19869837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549587bc62ff6067012fffc4124531c681e33704d75b4332e354e8e8c7ac9e94`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015487da6372d9bb9ef8a815c66c71f3c29cdd4a5dcaee2f5e87280d9717f00`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25860a630a1731a13c772ef03361714d3807678f3549f006ebe44c22140700b`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ac678ddec83e4354555da6ef9579f4ef2f9988789f66f9a5ca00e87db6b54`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 7.1 MB (7140876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8cd171770863e9348d4ee8c70d82ad8f289d2f4c1d388c224940feff19e47a`  
		Last Modified: Tue, 02 Dec 2025 00:11:01 GMT  
		Size: 99.5 KB (99516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5c60c1c2283f8e5a61f9ffda4011e80b738fd729f6732471650d647f62cb9`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c4891a520b352f266fdd87afc53d295cf90939a3cf3161134eee0a9f36e1d`  
		Last Modified: Tue, 02 Dec 2025 00:11:17 GMT  
		Size: 58.4 MB (58424894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d5d9da598fa4548678e746eb3de0f80e0197dc4482495dd269b371f4ab250`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ddcdacde67a928d9cfcb6dafce29f04eeb8bff016e6cd2756fea0f8a499d79`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:69a58a45b2f2152765e4d687b8e3006251f085c64eb9a725cd9562931e90989d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba11b7f0671e0843042aae85daa5eec651de997c5be2739f8d372d98a5fe0674`

```dockerfile
```

-	Layers:
	-	`sha256:70f851367f687fd4db17c04dc02a75b417cdb7a18c3bf70b7a00292fa8e33939`  
		Last Modified: Tue, 02 Dec 2025 03:08:14 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:26d283e4272e65c34bec8b7703698f75583b470b7fa5d6ac7b0544632dcdc74d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:4d55728f99b9642731991198ac30737ae9269d10e0d4721f798d1a6c7b6b6646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167604793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f500029a797b09b09f16482f6fd1be288c57d9355fc7176acea27545f24040aa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:08:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:07 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:35:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:35:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:35:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:35:13 GMT
CMD []
# Tue, 02 Dec 2025 01:04:33 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 02 Dec 2025 01:04:33 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 02 Dec 2025 01:04:33 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 01:04:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 02 Dec 2025 01:04:34 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 02 Dec 2025 01:04:34 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 02 Dec 2025 01:04:34 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bca2c07d80098fe1c61e0aa26eac435752d6dca6a2d3837735a2f68eedd27f`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 8.2 MB (8232306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c13c6aae9df8eeb1b8fe904cbdc67165e49d9f6ca682577bdee0ff1fddb0e`  
		Last Modified: Tue, 02 Dec 2025 00:08:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbba1101f59cdf058694512346b7fb8aeda578243290fc893ba55d81ac314cd`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 18.8 MB (18762388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc6a25ab2f1cc6386ed9595b9c99245b984bddba79a401ede272b40c8a1d34`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3786f9aa3c17d408a9f2162d158dcac195becac82c72ee0a4b29c43f52649`  
		Last Modified: Tue, 02 Dec 2025 00:08:43 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de8d894975036d476ad31205669d2600d672441a0b78b3d35650f89daf8774`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8318820339c402ec6f7161ee23642657be448d0298de2ca2a4946643e99bf`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fca41ae3f7f0a9e8364572b85d6e7862b0a01a49813320a77b7cca46a3dc67`  
		Last Modified: Tue, 02 Dec 2025 00:08:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eaeb7e3ff54863b596ddf45aa1f53fe06b5bac153cd3057038bca861e20c27`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 6.9 MB (6905410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568debdaab006707818488bd30ccbe9d028b275d05c6ce65dd3b1aec6ecdd841`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6f1c21ebbe286ed54f5e70396d9124048a5aab0e142aa1b81824ff82ace94`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b638749a1ad920d398a23428bd3e49a14bdf1b01a65776444264fa6afec6effd`  
		Last Modified: Tue, 02 Dec 2025 00:36:12 GMT  
		Size: 64.4 MB (64383976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4c76068297a0e5e2b8b3f4b582b62ec0bd167377a14e5e849d084838dd7d65`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831f7baf80344c1ea02c8259ab473f8c112481bf3ba30f27311a27ae615a6ba9`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6ab179a37092cfe7a4ed7e56cfaa4245be172a64fa8983225d912989c5fcc5`  
		Last Modified: Tue, 02 Dec 2025 01:04:49 GMT  
		Size: 3.4 MB (3398376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff83acf3702948a722e974d3dfc0a3282ac4ea70c4b2338b9a522e2544f1ade5`  
		Last Modified: Tue, 02 Dec 2025 01:04:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef24dccdc8e52bba4677dc83acf458b27fc0ee05e8023ff60cd3092c847448a`  
		Last Modified: Tue, 02 Dec 2025 01:04:49 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675547768fa484d1c34426e57586edd545c80c258f8ee3b1daad209973a18e39`  
		Last Modified: Tue, 02 Dec 2025 01:04:52 GMT  
		Size: 17.4 MB (17370238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6970303a67916649ea0e564b703347d9b6d63a5499fd2317d7bc25825bac820e`  
		Last Modified: Tue, 02 Dec 2025 01:04:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:eb319559cabdac9b6d6e61682add0ddd92bc4a1f016e42cb5cb54cb4406e18fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8a901677136393b67572d4d6f9bc5a7138099f768ffa584d6a047f88e97c1f`

```dockerfile
```

-	Layers:
	-	`sha256:a3186791ef27178f63f3334dcbdf3618a5894a1a04a580d19d58df0aad0c51f6`  
		Last Modified: Tue, 02 Dec 2025 03:08:36 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:500d9983f84e3c1918053364b152d6c8678606181d1b47f39e6e56325f88a4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157013358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259bf946645a41d2af38ec03e3dbc71a98181d2ae1e3f4953a1d790b71712216`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:02:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:02:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:02:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:02:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:02:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:02:56 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:10:29 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:10:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:10:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:10:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:10:33 GMT
CMD []
# Tue, 02 Dec 2025 00:16:44 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 02 Dec 2025 00:16:44 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 02 Dec 2025 00:16:44 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:16:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 02 Dec 2025 00:16:45 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 02 Dec 2025 00:16:45 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 02 Dec 2025 00:16:45 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8d6f5f280f3c754fdf75be610b9eaad7ee272876c0223bf2f3bd9a69fa411`  
		Last Modified: Tue, 02 Dec 2025 00:03:11 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e82d4d488e2618905f471024c5fe4d2e766267d8f3348b3dd7b6191630216`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f10b7b7acafc5f4d720b74cd91450008c1662de4a06650c39d1fb60537c2a6`  
		Last Modified: Tue, 02 Dec 2025 00:03:14 GMT  
		Size: 17.3 MB (17331274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53231739b67e10b4afa5aed2ecd60407f25e184a679cdbb1b5be2acafe29cc00`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c895eab34015734e14c5a975b34482844ee37ed6cae5b06a56089d9240b3`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 19.9 MB (19869837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549587bc62ff6067012fffc4124531c681e33704d75b4332e354e8e8c7ac9e94`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015487da6372d9bb9ef8a815c66c71f3c29cdd4a5dcaee2f5e87280d9717f00`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25860a630a1731a13c772ef03361714d3807678f3549f006ebe44c22140700b`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ac678ddec83e4354555da6ef9579f4ef2f9988789f66f9a5ca00e87db6b54`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 7.1 MB (7140876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8cd171770863e9348d4ee8c70d82ad8f289d2f4c1d388c224940feff19e47a`  
		Last Modified: Tue, 02 Dec 2025 00:11:01 GMT  
		Size: 99.5 KB (99516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5c60c1c2283f8e5a61f9ffda4011e80b738fd729f6732471650d647f62cb9`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c4891a520b352f266fdd87afc53d295cf90939a3cf3161134eee0a9f36e1d`  
		Last Modified: Tue, 02 Dec 2025 00:11:17 GMT  
		Size: 58.4 MB (58424894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d5d9da598fa4548678e746eb3de0f80e0197dc4482495dd269b371f4ab250`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ddcdacde67a928d9cfcb6dafce29f04eeb8bff016e6cd2756fea0f8a499d79`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763091d1251eb3f132c7b256f6b764c4d0955511bb4d4cfa11a52a3748b983b4`  
		Last Modified: Tue, 02 Dec 2025 00:17:05 GMT  
		Size: 3.4 MB (3389942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7986a5219667182dcb2d7497f51bcaf7b8358e271f41f0423f8f6665e6e8e27`  
		Last Modified: Tue, 02 Dec 2025 00:17:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2c564976ca2ad686546fe1e57597bd2623c76c3d660e852e930f32acfb7ffc`  
		Last Modified: Tue, 02 Dec 2025 00:17:05 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f8d39c0e9195885f73df58fb87203a86f5600e9372dc7af6c6ced416c50de3`  
		Last Modified: Tue, 02 Dec 2025 00:17:10 GMT  
		Size: 17.7 MB (17707046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b4c481f84d857b2b25d71535d076ec14fe51bf97a7693bb84958d2cc97bc79`  
		Last Modified: Tue, 02 Dec 2025 00:17:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:293f1f699032f6d51172da18bfd76ae3d5160bae1b22229359b445b35e2f27e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8a0d27bc916671f250df0b710a855e84e8aa12c157c41c5e1ac989214fcadd`

```dockerfile
```

-	Layers:
	-	`sha256:43e535d7855d564532284ba0cc7bd59b7a8ba7a0be76ae888afdda1ac9c29482`  
		Last Modified: Tue, 02 Dec 2025 03:08:39 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:9b20eb23e1f0443655673efb9db76c4b18cc1b45de1fcf82b3c1b749b9647bdf
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
$ docker pull docker@sha256:e7722a3fdf461a91095cc11b6751da7e69a1bdd583df23b5837cd03bc3dcbf11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146834840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3d6683ede5a5e31409999791e15e1785c65344da6483593dd3af23c29bd562`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:08:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:08:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:08:04 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:08:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:08:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:08:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:08:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:07 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:35:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:35:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:35:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:35:13 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:35:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:35:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:35:13 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bca2c07d80098fe1c61e0aa26eac435752d6dca6a2d3837735a2f68eedd27f`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 8.2 MB (8232306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c13c6aae9df8eeb1b8fe904cbdc67165e49d9f6ca682577bdee0ff1fddb0e`  
		Last Modified: Tue, 02 Dec 2025 00:08:39 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbba1101f59cdf058694512346b7fb8aeda578243290fc893ba55d81ac314cd`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 18.8 MB (18762388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc6a25ab2f1cc6386ed9595b9c99245b984bddba79a401ede272b40c8a1d34`  
		Last Modified: Tue, 02 Dec 2025 00:08:42 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3786f9aa3c17d408a9f2162d158dcac195becac82c72ee0a4b29c43f52649`  
		Last Modified: Tue, 02 Dec 2025 00:08:43 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60de8d894975036d476ad31205669d2600d672441a0b78b3d35650f89daf8774`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc8318820339c402ec6f7161ee23642657be448d0298de2ca2a4946643e99bf`  
		Last Modified: Tue, 02 Dec 2025 00:08:40 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fca41ae3f7f0a9e8364572b85d6e7862b0a01a49813320a77b7cca46a3dc67`  
		Last Modified: Tue, 02 Dec 2025 00:08:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eaeb7e3ff54863b596ddf45aa1f53fe06b5bac153cd3057038bca861e20c27`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 6.9 MB (6905410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568debdaab006707818488bd30ccbe9d028b275d05c6ce65dd3b1aec6ecdd841`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6f1c21ebbe286ed54f5e70396d9124048a5aab0e142aa1b81824ff82ace94`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b638749a1ad920d398a23428bd3e49a14bdf1b01a65776444264fa6afec6effd`  
		Last Modified: Tue, 02 Dec 2025 00:36:12 GMT  
		Size: 64.4 MB (64383976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4c76068297a0e5e2b8b3f4b582b62ec0bd167377a14e5e849d084838dd7d65`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831f7baf80344c1ea02c8259ab473f8c112481bf3ba30f27311a27ae615a6ba9`  
		Last Modified: Tue, 02 Dec 2025 00:36:02 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:b3ffbc635daa4785c6e8540daa89e290342d9ce7574d182f603904c844e2ae55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cddfa71d427c6ffde929b85b3ac597a723b864fa7b755fb7e2b38bffcec4abf`

```dockerfile
```

-	Layers:
	-	`sha256:c293678f6e88a59d70f255b8b2d4d5370350c49c9cac522deee7e1ca928a771f`  
		Last Modified: Tue, 02 Dec 2025 03:08:05 GMT  
		Size: 34.5 KB (34547 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:f4264dc6f53bf84c143abcd79f054061e949f91297519b16342df3b0fcf515d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138377571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5525feeb0b6b1996748694f01b24cce0d9825880fcc090ceaec227482995adb8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:00:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:00:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:01:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:01:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:01:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:01:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:03 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:08:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:08:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:08:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:08:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:47 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:08:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:08:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:47 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd90142670bbaed6f585f4970fd1d53633e0869fd5272c8e3df77120bace0e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 8.1 MB (8140518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642374c76164440ef8b823ab6bba0dd1bee0e2a2376c47bb5f4073a585413e04`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed115a71dbefda1db4593399cccc8dad9b72d92954e97811cb17ea6cbd16029`  
		Last Modified: Tue, 02 Dec 2025 00:01:24 GMT  
		Size: 17.6 MB (17559034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5443b6b267bcc407b81aa1fc56c89a28780986fdb8a6a0e262dc6cb167368cb`  
		Last Modified: Tue, 02 Dec 2025 00:01:23 GMT  
		Size: 21.5 MB (21476552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1408d4a896b763e6cf9b6eb5321ee325d093c04ddb275e901a85d57735dd87d`  
		Last Modified: Tue, 02 Dec 2025 00:01:21 GMT  
		Size: 20.5 MB (20480374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc905b6a443c6c8096533c447544d946dedb7a2450e9d8815424d25a2b70b5b8`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79661a927ae816f329cd8e6d5aebc5775b45d598f860218a7fa0bf34259fedae`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc8f4aa5c2b729f00263aa5f33b190bedfd7d94a05ac9ccb26f4f1995d10a1e`  
		Last Modified: Tue, 02 Dec 2025 00:01:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f114e86733f934e05b8cc095e26ac7d23df0400c164367a5d0960c90ffbb7e7`  
		Last Modified: Tue, 02 Dec 2025 00:09:22 GMT  
		Size: 7.2 MB (7230316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52de536e5339daea653f15c27e78b4cf16e12a10d82ef4f286872bc4f4aafd9`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 90.0 KB (89961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae860099f824f4d5c845c472dccead8faa86f1afc2773e064de55ac8317fa514`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99458a7fe0e1036a55a30274f0e06e8baa5da805dac7a2d7f788bf02c9531c18`  
		Last Modified: Tue, 02 Dec 2025 00:09:30 GMT  
		Size: 59.9 MB (59888589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bba7682b037f71b8aea88b0676d075b4bcd35fa3390b95b1bd864d4999afb7d`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed47c75bfd062f331a396b716966fb250ee7485fee132a7b2942e732842fbf3`  
		Last Modified: Tue, 02 Dec 2025 00:09:21 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:ec56f63d4804233c364f31addc653c748a9b7e58cc1b72a68562b7cfd4f5869d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3125bbdfa07949727984336157b0367e420ed260fb1153f6a4ac86374835df20`

```dockerfile
```

-	Layers:
	-	`sha256:e35660952afa463bcd149750757d217195b0afeb78547aeae6aecaf7697b4b82`  
		Last Modified: Tue, 02 Dec 2025 03:08:08 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:4c9e1d32783f3091ec573930696e1a02680c8b2e0a96588960e8cfb4785f0987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136499855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a132a67d9b1e15c2a6b6b5072baf4669d91a4c94c59594cde5e134a3f13f7e0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:03:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:03:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:03:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:03:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:03:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:03:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:03:35 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:08:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:08:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:08:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:08:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:08:52 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:08:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:08:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:08:52 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ec0784ecb867af52b79e3f383d52e39182464803fd28c22d49d1ff019df6e4`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 7.5 MB (7461368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491247472d55430402882837b71580b20d49d688f85f713917e74b9c4dcfa29`  
		Last Modified: Tue, 02 Dec 2025 00:03:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681ac3424d8a722d9e60118306e4292f0558f8234066431fcf35fe24394a1bb8`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 17.6 MB (17550851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4ccba3516b05ed1ea12fcc5ff93f84c20331f6098765bc58aa14342452b044`  
		Last Modified: Tue, 02 Dec 2025 00:03:51 GMT  
		Size: 21.5 MB (21454904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01cc08290b32581069106ced2f3f3eb8ee944803bea261cb440c95a59f3e88`  
		Last Modified: Tue, 02 Dec 2025 00:03:52 GMT  
		Size: 20.5 MB (20462776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3320b40de969faa831b8c731ba2d0e1b46c0099f07df033d271e79b3ae90cfa`  
		Last Modified: Tue, 02 Dec 2025 00:03:49 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6f871522091994e48824cf572b17680f5f65920875e93a33820ca79643cb83`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccd637b5bd3f36088e619e2cd9af1073d6cf18b4daae90c18da0bebaac04039`  
		Last Modified: Tue, 02 Dec 2025 00:03:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fedb293900f104824c5bf607d49531816ebb696de67d2349e25c3b7235c7d4`  
		Last Modified: Tue, 02 Dec 2025 03:08:37 GMT  
		Size: 6.5 MB (6538170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f3efb3e0b8e692ee930467452c2b90850e32de6e81f525c8b5ecb809596cb1`  
		Last Modified: Tue, 02 Dec 2025 01:10:44 GMT  
		Size: 86.4 KB (86397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6a05cebb7258e8cc03a59c4ddbfab058b79a4254d47f5f7339c3cbb66e0f91`  
		Last Modified: Tue, 02 Dec 2025 01:10:45 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2700c9375899dc20256cee56347f7a94685712635d0a083c74baf5a4d0ac5809`  
		Last Modified: Tue, 02 Dec 2025 03:08:48 GMT  
		Size: 59.7 MB (59715683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f83379703e2b0dd6765daef6f82dba3e582ae979b57dfd62b9101c915e244`  
		Last Modified: Tue, 02 Dec 2025 01:10:48 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fb0afbbc9ea4bc8903a6671f34110ef481952a81c388cc585e9b21cd7f4e21`  
		Last Modified: Tue, 02 Dec 2025 01:10:44 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:81b93d08f8b08b14411acfcfd4683554ff94f1553aa1c42bb33bb2e43d453ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db32ac5181c3e6cf95fea47b5846cd4a761768ec6dc895055994af29bcb7718b`

```dockerfile
```

-	Layers:
	-	`sha256:9f6b2982982b5b6659faac06d4632eb9f834c5522239d5ab3c1c0c340c2664f7`  
		Last Modified: Tue, 02 Dec 2025 03:08:11 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:37269ed2d81f5f6d65910acc46f07807e7027efa4560c03b5c2c427c57b5b99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135915031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cb9c89488e9663f2162c6982870ff63ce946066edbedbf787cccfcb650d4a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 00:02:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 02 Dec 2025 00:02:52 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:02:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 02 Dec 2025 00:02:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:02:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 02 Dec 2025 00:02:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:02:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Dec 2025 00:02:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 02 Dec 2025 00:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:02:56 GMT
CMD ["sh"]
# Tue, 02 Dec 2025 00:10:29 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 02 Dec 2025 00:10:30 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 02 Dec 2025 00:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 02 Dec 2025 00:10:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:10:33 GMT
VOLUME [/var/lib/docker]
# Tue, 02 Dec 2025 00:10:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 02 Dec 2025 00:10:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 02 Dec 2025 00:10:33 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec8d6f5f280f3c754fdf75be610b9eaad7ee272876c0223bf2f3bd9a69fa411`  
		Last Modified: Tue, 02 Dec 2025 00:03:11 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e82d4d488e2618905f471024c5fe4d2e766267d8f3348b3dd7b6191630216`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f10b7b7acafc5f4d720b74cd91450008c1662de4a06650c39d1fb60537c2a6`  
		Last Modified: Tue, 02 Dec 2025 00:03:14 GMT  
		Size: 17.3 MB (17331274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53231739b67e10b4afa5aed2ecd60407f25e184a679cdbb1b5be2acafe29cc00`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c895eab34015734e14c5a975b34482844ee37ed6cae5b06a56089d9240b3`  
		Last Modified: Tue, 02 Dec 2025 00:03:12 GMT  
		Size: 19.9 MB (19869837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549587bc62ff6067012fffc4124531c681e33704d75b4332e354e8e8c7ac9e94`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015487da6372d9bb9ef8a815c66c71f3c29cdd4a5dcaee2f5e87280d9717f00`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25860a630a1731a13c772ef03361714d3807678f3549f006ebe44c22140700b`  
		Last Modified: Tue, 02 Dec 2025 00:03:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ac678ddec83e4354555da6ef9579f4ef2f9988789f66f9a5ca00e87db6b54`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 7.1 MB (7140876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8cd171770863e9348d4ee8c70d82ad8f289d2f4c1d388c224940feff19e47a`  
		Last Modified: Tue, 02 Dec 2025 00:11:01 GMT  
		Size: 99.5 KB (99516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb5c60c1c2283f8e5a61f9ffda4011e80b738fd729f6732471650d647f62cb9`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c4891a520b352f266fdd87afc53d295cf90939a3cf3161134eee0a9f36e1d`  
		Last Modified: Tue, 02 Dec 2025 00:11:17 GMT  
		Size: 58.4 MB (58424894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d5d9da598fa4548678e746eb3de0f80e0197dc4482495dd269b371f4ab250`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ddcdacde67a928d9cfcb6dafce29f04eeb8bff016e6cd2756fea0f8a499d79`  
		Last Modified: Tue, 02 Dec 2025 00:11:02 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:69a58a45b2f2152765e4d687b8e3006251f085c64eb9a725cd9562931e90989d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba11b7f0671e0843042aae85daa5eec651de997c5be2739f8d372d98a5fe0674`

```dockerfile
```

-	Layers:
	-	`sha256:70f851367f687fd4db17c04dc02a75b417cdb7a18c3bf70b7a00292fa8e33939`  
		Last Modified: Tue, 02 Dec 2025 03:08:14 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:1c43c735429614f250536aac0dd2c328e6d0b893b299c60a260849bf484844e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:edb55a55a9709f716094eff0d619f5cccfbe7ab9c820d4cd94316a3dc80f85b0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301942510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd431f71a41f9ca0d66fa3490028ce3378094dc608e876e5a5e01d5f1c00a85`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 02 Dec 2025 00:02:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:03:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:03:18 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:03:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:03:38 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:03:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:03:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1274f6d3b6ceaa195acd16a17546b93878ef3c76e6b0c0ea475532ae81138829`  
		Last Modified: Tue, 02 Dec 2025 00:29:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18719cadfdf416a79dc2e3958aaaa04ba5f00625ff6e93ab3dec72cf2f51da`  
		Last Modified: Tue, 02 Dec 2025 00:29:25 GMT  
		Size: 394.4 KB (394389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacb90f7314fdc946208b5f3ff65f6c72d6649551c978d26418bda8d9e5a6890`  
		Last Modified: Tue, 02 Dec 2025 00:29:30 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad66afc50aa529e50d970dea5d3e8f437aab69ad9cb3882a256d4319b5b42d15`  
		Last Modified: Tue, 02 Dec 2025 00:29:33 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b85b05963e8f44359d0370018251cb0af969ffdbeeb8b5a7d16e32fa4e6e0`  
		Last Modified: Tue, 02 Dec 2025 01:01:49 GMT  
		Size: 19.4 MB (19445634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4369b8ed94ba65d95a6942b0a54d8302024faae5688bd932577bcc256abefee3`  
		Last Modified: Tue, 02 Dec 2025 00:29:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a49cd2f3d1017e97f6ed405d89cd3d09949977cd4e8b5b34fdb146b8da04a3`  
		Last Modified: Tue, 02 Dec 2025 00:29:41 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f583f8eec952d8c1f2b32d817e3b14c51c57780bc726d9eb1c393555075ba3c7`  
		Last Modified: Tue, 02 Dec 2025 00:29:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9def44a99f4bab2dcc70f25abcf502cbafd84b76181171949b51aa186814cce8`  
		Last Modified: Tue, 02 Dec 2025 01:01:52 GMT  
		Size: 23.9 MB (23942612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46335ebb4377421068829028c4feca1ce21bb336ddc77ffaff4cf2fdd07669d`  
		Last Modified: Tue, 02 Dec 2025 00:29:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6700c7401706484942b62f39837e732625ea2eae796316fd97da557c97d9a2bd`  
		Last Modified: Tue, 02 Dec 2025 00:29:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fcde18a4abb110b9720f6357dc8098af919dc2247e1fcb902d2dbce1dc2bbb`  
		Last Modified: Tue, 02 Dec 2025 00:29:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a06df7c12fbd246e254cc1c5ccda1ea8a3064c55627e865f6c813204a155a`  
		Last Modified: Tue, 02 Dec 2025 01:01:55 GMT  
		Size: 22.7 MB (22692302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:59fd73de957de338aebfa44cbc56e9e613995025b25e51d83b83c144f5f15828
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836458539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb88b8d8055f99a033e38f88e5335522379ea547e8004051da7417b42321791`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 02 Dec 2025 00:09:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:10:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:10:58 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:11:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:11:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:11:29 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:11:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:11:32 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:11:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:11:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:11:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:12:00 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:12:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca80c7273175042e00fe42b9acc4273bb878eee0a0c4c5fa397b7397b8841b60`  
		Last Modified: Tue, 02 Dec 2025 00:27:05 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de920d113346f7751e223cc4f56c9ac711e693c7bbad0a62661edd7a13e3cb18`  
		Last Modified: Tue, 02 Dec 2025 00:27:06 GMT  
		Size: 518.9 KB (518913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4006e793c124c40f2cd2b04d3620d9d0701f4a8b6b235a461ac6bf489cfee31`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b20b11149feeb6be69bcded688660b34c2ff915411a4a073b5a67b8511a88e`  
		Last Modified: Tue, 02 Dec 2025 00:27:07 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f920b83c504a555c3b5c26902e6a1ec22ef2c88c9afba067de16269b6f0429`  
		Last Modified: Tue, 02 Dec 2025 00:27:10 GMT  
		Size: 19.4 MB (19406772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf9e2e8b9aa98bf5c8b54f2bc38c78ea68496c411e4620b1762bd486b251406`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e633a60820512a97163b768f578d2ed4c4d4e6a403d9a260fc3625581aee37d6`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c418e2d05c842f6856d59f8030e8c3b42bc6d2060d9185961466724fb8ebb259`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cefba9d08372f4b315b8a9b066b2e795c2a6f31473405639443e63a3a13cb4e`  
		Last Modified: Tue, 02 Dec 2025 00:27:12 GMT  
		Size: 23.9 MB (23905567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9c528564d3c90f5342ffbe261f0e02cc558cd11bb1c2cda3901acce07c071e`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac38da0772c85387d94e42b5ac044035676912ba7b05c906b2b267f10c2c0e10`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90916836d70bec2b5e65b639f5ebfb46be73741a370798dee04edb8ee868a44b`  
		Last Modified: Tue, 02 Dec 2025 00:27:12 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42bcb722bb6159035d26e8273c1451882c9adf5073c21bba4efbc06e42c5f68`  
		Last Modified: Tue, 02 Dec 2025 00:27:14 GMT  
		Size: 22.7 MB (22653934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:da10f7e9be92554d35616813bc89c43489e9d0568b3682aa5dd4c573ce5e9a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:59fd73de957de338aebfa44cbc56e9e613995025b25e51d83b83c144f5f15828
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836458539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb88b8d8055f99a033e38f88e5335522379ea547e8004051da7417b42321791`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 02 Dec 2025 00:09:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:10:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:10:58 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:11:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:11:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:11:29 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:11:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:11:32 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:11:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:11:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:11:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:12:00 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:12:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca80c7273175042e00fe42b9acc4273bb878eee0a0c4c5fa397b7397b8841b60`  
		Last Modified: Tue, 02 Dec 2025 00:27:05 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de920d113346f7751e223cc4f56c9ac711e693c7bbad0a62661edd7a13e3cb18`  
		Last Modified: Tue, 02 Dec 2025 00:27:06 GMT  
		Size: 518.9 KB (518913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4006e793c124c40f2cd2b04d3620d9d0701f4a8b6b235a461ac6bf489cfee31`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b20b11149feeb6be69bcded688660b34c2ff915411a4a073b5a67b8511a88e`  
		Last Modified: Tue, 02 Dec 2025 00:27:07 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f920b83c504a555c3b5c26902e6a1ec22ef2c88c9afba067de16269b6f0429`  
		Last Modified: Tue, 02 Dec 2025 00:27:10 GMT  
		Size: 19.4 MB (19406772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf9e2e8b9aa98bf5c8b54f2bc38c78ea68496c411e4620b1762bd486b251406`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e633a60820512a97163b768f578d2ed4c4d4e6a403d9a260fc3625581aee37d6`  
		Last Modified: Tue, 02 Dec 2025 00:27:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c418e2d05c842f6856d59f8030e8c3b42bc6d2060d9185961466724fb8ebb259`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cefba9d08372f4b315b8a9b066b2e795c2a6f31473405639443e63a3a13cb4e`  
		Last Modified: Tue, 02 Dec 2025 00:27:12 GMT  
		Size: 23.9 MB (23905567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9c528564d3c90f5342ffbe261f0e02cc558cd11bb1c2cda3901acce07c071e`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac38da0772c85387d94e42b5ac044035676912ba7b05c906b2b267f10c2c0e10`  
		Last Modified: Tue, 02 Dec 2025 00:27:11 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90916836d70bec2b5e65b639f5ebfb46be73741a370798dee04edb8ee868a44b`  
		Last Modified: Tue, 02 Dec 2025 00:27:12 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42bcb722bb6159035d26e8273c1451882c9adf5073c21bba4efbc06e42c5f68`  
		Last Modified: Tue, 02 Dec 2025 00:27:14 GMT  
		Size: 22.7 MB (22653934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:5e399dd5dd0dfe81579a2bca9462ce91fd0af47c6c1f7a6b73ffbc942907f790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:edb55a55a9709f716094eff0d619f5cccfbe7ab9c820d4cd94316a3dc80f85b0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301942510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd431f71a41f9ca0d66fa3490028ce3378094dc608e876e5a5e01d5f1c00a85`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 02 Dec 2025 00:02:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 00:03:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 00:03:18 GMT
ENV DOCKER_VERSION=29.1.1
# Tue, 02 Dec 2025 00:03:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.1.zip
# Tue, 02 Dec 2025 00:03:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 02 Dec 2025 00:03:37 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 02 Dec 2025 00:03:38 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 02 Dec 2025 00:03:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 00:03:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Tue, 02 Dec 2025 00:03:50 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Tue, 02 Dec 2025 00:03:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1274f6d3b6ceaa195acd16a17546b93878ef3c76e6b0c0ea475532ae81138829`  
		Last Modified: Tue, 02 Dec 2025 00:29:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18719cadfdf416a79dc2e3958aaaa04ba5f00625ff6e93ab3dec72cf2f51da`  
		Last Modified: Tue, 02 Dec 2025 00:29:25 GMT  
		Size: 394.4 KB (394389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacb90f7314fdc946208b5f3ff65f6c72d6649551c978d26418bda8d9e5a6890`  
		Last Modified: Tue, 02 Dec 2025 00:29:30 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad66afc50aa529e50d970dea5d3e8f437aab69ad9cb3882a256d4319b5b42d15`  
		Last Modified: Tue, 02 Dec 2025 00:29:33 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b85b05963e8f44359d0370018251cb0af969ffdbeeb8b5a7d16e32fa4e6e0`  
		Last Modified: Tue, 02 Dec 2025 01:01:49 GMT  
		Size: 19.4 MB (19445634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4369b8ed94ba65d95a6942b0a54d8302024faae5688bd932577bcc256abefee3`  
		Last Modified: Tue, 02 Dec 2025 00:29:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a49cd2f3d1017e97f6ed405d89cd3d09949977cd4e8b5b34fdb146b8da04a3`  
		Last Modified: Tue, 02 Dec 2025 00:29:41 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f583f8eec952d8c1f2b32d817e3b14c51c57780bc726d9eb1c393555075ba3c7`  
		Last Modified: Tue, 02 Dec 2025 00:29:45 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9def44a99f4bab2dcc70f25abcf502cbafd84b76181171949b51aa186814cce8`  
		Last Modified: Tue, 02 Dec 2025 01:01:52 GMT  
		Size: 23.9 MB (23942612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46335ebb4377421068829028c4feca1ce21bb336ddc77ffaff4cf2fdd07669d`  
		Last Modified: Tue, 02 Dec 2025 00:29:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6700c7401706484942b62f39837e732625ea2eae796316fd97da557c97d9a2bd`  
		Last Modified: Tue, 02 Dec 2025 00:29:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fcde18a4abb110b9720f6357dc8098af919dc2247e1fcb902d2dbce1dc2bbb`  
		Last Modified: Tue, 02 Dec 2025 00:29:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17a06df7c12fbd246e254cc1c5ccda1ea8a3064c55627e865f6c813204a155a`  
		Last Modified: Tue, 02 Dec 2025 01:01:55 GMT  
		Size: 22.7 MB (22692302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

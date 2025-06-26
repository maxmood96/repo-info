<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.3`](#docker283)
-	[`docker:28.3-cli`](#docker283-cli)
-	[`docker:28.3-dind`](#docker283-dind)
-	[`docker:28.3-dind-rootless`](#docker283-dind-rootless)
-	[`docker:28.3-windowsservercore`](#docker283-windowsservercore)
-	[`docker:28.3-windowsservercore-ltsc2022`](#docker283-windowsservercore-ltsc2022)
-	[`docker:28.3-windowsservercore-ltsc2025`](#docker283-windowsservercore-ltsc2025)
-	[`docker:28.3.0`](#docker2830)
-	[`docker:28.3.0-alpine3.22`](#docker2830-alpine322)
-	[`docker:28.3.0-cli`](#docker2830-cli)
-	[`docker:28.3.0-cli-alpine3.22`](#docker2830-cli-alpine322)
-	[`docker:28.3.0-dind`](#docker2830-dind)
-	[`docker:28.3.0-dind-alpine3.22`](#docker2830-dind-alpine322)
-	[`docker:28.3.0-dind-rootless`](#docker2830-dind-rootless)
-	[`docker:28.3.0-windowsservercore`](#docker2830-windowsservercore)
-	[`docker:28.3.0-windowsservercore-ltsc2022`](#docker2830-windowsservercore-ltsc2022)
-	[`docker:28.3.0-windowsservercore-ltsc2025`](#docker2830-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:d33eb93fe02683e984e6f8a93c0b3d85bb74f56ec83922bc39fb34ba23ab42bc
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
$ docker pull docker@sha256:bd5712b912e233b9cbca5ed94664dda05655537f56323d55f5435be0df084f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144906835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6892cb0e669d8bf6d40d1421bfd62b0aec81041706f7b45de7a03514cfef527b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:6d82b2f6555dd414407f11111af5c2028f1205e50140594c33edfdaf9add7fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281f5c43f6b438ece0586157f96cec3dbde12c3e55fb80b93dcb5e08c92bc9c0`

```dockerfile
```

-	Layers:
	-	`sha256:f99b7342f71018419b6d22e5f772de11b7f1619ac5707ad3f2610ac9f834684c`  
		Last Modified: Wed, 25 Jun 2025 20:07:28 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:0e7bd5b322a7adee7f87d5da6133602a1b13943207c1c119e3fa8bc150662de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135881655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e5f0a26fdef7325b82b98ac05955a1e1ab6990eee865f5d40b5eb1c2b380f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ff3c42dfe8b909933270cb290d5b16dad7c39ef1c61d930695bccb4af028b`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 7.2 MB (7230273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf5f2cd81da4f9935d1b8f1e0c69e9690065ce54192c47285c02007b855ab71`  
		Last Modified: Wed, 25 Jun 2025 19:09:57 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9315c92c22796071003a7353007bcfafc2dde73136adc0ee6c1f859c9ead82`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eabbd9d791bab2458faac47bddb10b59b825dc9b8a6e958d893dad0d62d2b13`  
		Last Modified: Wed, 25 Jun 2025 19:10:07 GMT  
		Size: 58.2 MB (58196245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2fa52243ccad08598f463d20022392c4e63de6a7fa3389a2d3f13bc5072850`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18747036c5bfd27297ec304b7871a2c0a0cab99bc9cac7dcd22593dc95f704d0`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:999ce16d0b42a6156eae74e0a48680ba57dfefa8409ec8cb3140e4abfa0b8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1afb05bba7f7a8f5e78c1e59548ece1fd7da038bb3addbbb866344b023c03`

```dockerfile
```

-	Layers:
	-	`sha256:9849cf691a13b263da46b7691c04aa707880fde9055dd21ca78616d50691794a`  
		Last Modified: Wed, 25 Jun 2025 20:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4c6ec3de04e99f6aba4a50701988210b9d0bfbcee4f4715aba2b6f968145ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134179998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e5f59ba3ffbbe22e927ebf4f2cfd1f28d553a63e5803230880f12c7bb9137d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a13ff228646fe31640f66680c77b8179b59cf030776d4dc27e0b8a4073a1161`  
		Last Modified: Wed, 25 Jun 2025 19:09:40 GMT  
		Size: 6.5 MB (6538132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e439188892f1f8a228ea037911e2843fc2f69b92e2847007cf69bfb07cae8e9`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 86.5 KB (86492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82b72c117f21d49e7e8d6934422e959de7f39d5971cb8bf2bc5a612c6f321b6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5741868cb033a7c74a817afc1bbfc0b66636546ad2b2819fd90b5b72cd7314`  
		Last Modified: Wed, 25 Jun 2025 19:09:44 GMT  
		Size: 58.2 MB (58196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f745e31047d1161b57e77243e0a39cfb9fc008c772fa16ee7c67ed75c9051b`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbf907fef629de9d464812fadbd09c96845cd8dcf8c4c1acf19dbc216347bc6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:5e7ea7e55af96477d6205063362129df645015586d168d3abc5fddf5af1f9756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77876fbab01e5b51149471bea0941cfcebf64d55778d638330e8ec92546e5340`

```dockerfile
```

-	Layers:
	-	`sha256:35d28f9246501c698aa882110ff7cb8d3d1ee99e8454a3b8fac5fa6665d20ca9`  
		Last Modified: Wed, 25 Jun 2025 20:07:35 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:852d19966630687c3ad157b217ace73e93c823aaf34c396f4aaef675bee52a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135648800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b957e61342f7dd8223305f18ccc713082c3ef5c69722449cb8b8fdbeb8319012`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:a2c73991ca6ca907adb176cce487de5342c67b9d610999b2711012d6dae3fd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070a2badedc718d9b3896e9dcd97389153b5d537dcaaaf577fe0560b77eb6e2`

```dockerfile
```

-	Layers:
	-	`sha256:364f514ac25163eb6400a49f2a109178e8f6779987fe82a10b5bb1acbf9282bc`  
		Last Modified: Thu, 26 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:be316e9f9a158bdd04d175cac7867be4561d9718c8f45331ba09f839854d6ac4
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
$ docker pull docker@sha256:e15d465988c670df7863f019b7bbffadc2fb5a89355183d2f77c9541af6f5f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75386866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c308218afb92593639450e489ef8638050ab55a6c49065a2fbc8a52f70bd7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:95954b4d8cb3ecd9e948ffac374a91f07bfeffef3b0c5c17dd0f6aaa5deab1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf73ac7a434f1e1608f059171e612c92ef03248ba073d582b984939f205e7bb`

```dockerfile
```

-	Layers:
	-	`sha256:659dc4fc8c676ae5ecee4b9f1c73a5096d5d03e6459f28d1554f3f2211f5a592`  
		Last Modified: Wed, 25 Jun 2025 20:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ca185f5711941016ddadcfaa648bdc27c90418f2282d093c6bc751aa3e7ba38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70359081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9ff19e1547d18c4a360fa003b26cb878d2f1ec67647bc6159bfb0320fd306`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8bd2cad79060bb5785bed3792250043dec874b2660a91b8acff6cbbd7c39bbbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee647cfa7ad7371b150be4ce91c2395bcd50e25ae0986066f39ec2db1307b8ef`

```dockerfile
```

-	Layers:
	-	`sha256:3c84ecc5e16e1816184f43bbc41f0010df0495baeb95c58e0b47743bbecfb4e7`  
		Last Modified: Wed, 25 Jun 2025 20:07:48 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:7f2567fc8f1b52e8b7fc40fbec2270157a426255e299307c1fdf6291134a4bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69353151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f148d0ade3d87c4d8d77dd87529f575e2008e919bb844a947247561ec03c82db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:234783c583655b5fba47f029b646f86832181f4e7693051a58456c45043c099c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8693516fb4d64dd200448d3da2a32b3deb0e4634e4f4faaa6dc35984a4d873e`

```dockerfile
```

-	Layers:
	-	`sha256:d7b8ebd195f16dbf716810084fd30cbc4943c0d20f94cf8055a15691fd5203ce`  
		Last Modified: Wed, 25 Jun 2025 20:07:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2b4c39548793a279667d4ced40e5e68af421e8ff4000c101ee2f7e5b299573b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70940773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c4520ee754d509808a5e81ed1749fcb77b10dea95542447afafeccebaca66e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:026dc96b447b564878e37a1732f26aa77491519e943779e9f5e336580774335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a66b0aed9a637a80f3fbfb7b609cc336667c89535146dd5bda65fc05777ce3`

```dockerfile
```

-	Layers:
	-	`sha256:c2f530f380386ce5972d923f6ec42373f519edff7acfd63e4e1934eeb86652b4`  
		Last Modified: Wed, 25 Jun 2025 20:07:54 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:d33eb93fe02683e984e6f8a93c0b3d85bb74f56ec83922bc39fb34ba23ab42bc
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
$ docker pull docker@sha256:bd5712b912e233b9cbca5ed94664dda05655537f56323d55f5435be0df084f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144906835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6892cb0e669d8bf6d40d1421bfd62b0aec81041706f7b45de7a03514cfef527b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6d82b2f6555dd414407f11111af5c2028f1205e50140594c33edfdaf9add7fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281f5c43f6b438ece0586157f96cec3dbde12c3e55fb80b93dcb5e08c92bc9c0`

```dockerfile
```

-	Layers:
	-	`sha256:f99b7342f71018419b6d22e5f772de11b7f1619ac5707ad3f2610ac9f834684c`  
		Last Modified: Wed, 25 Jun 2025 20:07:28 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:0e7bd5b322a7adee7f87d5da6133602a1b13943207c1c119e3fa8bc150662de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135881655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e5f0a26fdef7325b82b98ac05955a1e1ab6990eee865f5d40b5eb1c2b380f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ff3c42dfe8b909933270cb290d5b16dad7c39ef1c61d930695bccb4af028b`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 7.2 MB (7230273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf5f2cd81da4f9935d1b8f1e0c69e9690065ce54192c47285c02007b855ab71`  
		Last Modified: Wed, 25 Jun 2025 19:09:57 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9315c92c22796071003a7353007bcfafc2dde73136adc0ee6c1f859c9ead82`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eabbd9d791bab2458faac47bddb10b59b825dc9b8a6e958d893dad0d62d2b13`  
		Last Modified: Wed, 25 Jun 2025 19:10:07 GMT  
		Size: 58.2 MB (58196245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2fa52243ccad08598f463d20022392c4e63de6a7fa3389a2d3f13bc5072850`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18747036c5bfd27297ec304b7871a2c0a0cab99bc9cac7dcd22593dc95f704d0`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:999ce16d0b42a6156eae74e0a48680ba57dfefa8409ec8cb3140e4abfa0b8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1afb05bba7f7a8f5e78c1e59548ece1fd7da038bb3addbbb866344b023c03`

```dockerfile
```

-	Layers:
	-	`sha256:9849cf691a13b263da46b7691c04aa707880fde9055dd21ca78616d50691794a`  
		Last Modified: Wed, 25 Jun 2025 20:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4c6ec3de04e99f6aba4a50701988210b9d0bfbcee4f4715aba2b6f968145ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134179998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e5f59ba3ffbbe22e927ebf4f2cfd1f28d553a63e5803230880f12c7bb9137d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a13ff228646fe31640f66680c77b8179b59cf030776d4dc27e0b8a4073a1161`  
		Last Modified: Wed, 25 Jun 2025 19:09:40 GMT  
		Size: 6.5 MB (6538132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e439188892f1f8a228ea037911e2843fc2f69b92e2847007cf69bfb07cae8e9`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 86.5 KB (86492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82b72c117f21d49e7e8d6934422e959de7f39d5971cb8bf2bc5a612c6f321b6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5741868cb033a7c74a817afc1bbfc0b66636546ad2b2819fd90b5b72cd7314`  
		Last Modified: Wed, 25 Jun 2025 19:09:44 GMT  
		Size: 58.2 MB (58196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f745e31047d1161b57e77243e0a39cfb9fc008c772fa16ee7c67ed75c9051b`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbf907fef629de9d464812fadbd09c96845cd8dcf8c4c1acf19dbc216347bc6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5e7ea7e55af96477d6205063362129df645015586d168d3abc5fddf5af1f9756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77876fbab01e5b51149471bea0941cfcebf64d55778d638330e8ec92546e5340`

```dockerfile
```

-	Layers:
	-	`sha256:35d28f9246501c698aa882110ff7cb8d3d1ee99e8454a3b8fac5fa6665d20ca9`  
		Last Modified: Wed, 25 Jun 2025 20:07:35 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:852d19966630687c3ad157b217ace73e93c823aaf34c396f4aaef675bee52a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135648800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b957e61342f7dd8223305f18ccc713082c3ef5c69722449cb8b8fdbeb8319012`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a2c73991ca6ca907adb176cce487de5342c67b9d610999b2711012d6dae3fd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070a2badedc718d9b3896e9dcd97389153b5d537dcaaaf577fe0560b77eb6e2`

```dockerfile
```

-	Layers:
	-	`sha256:364f514ac25163eb6400a49f2a109178e8f6779987fe82a10b5bb1acbf9282bc`  
		Last Modified: Thu, 26 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:6c2c0d6beb885c9c9741e9227a2c8bb25126b948831afda4a6c4221d6cadbb91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:7fafee3e6a673e4c95d8b8583e939baa5c4103872c26d5074032bb49e8643b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163487607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f7bdc571bf67b9957bd1f5fe4522ba3f5fd48b35b409599e6c30f10c3ca55f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101bccb38f5fc26e226b3aed7f5d43d304a31e4ae35365d48a66d9fc6b533934`  
		Last Modified: Wed, 25 Jun 2025 18:08:52 GMT  
		Size: 993.3 KB (993273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a974f1a114c34599fb5b4760b77413667489c7048fcc9ac21ce87e5cf6422b`  
		Last Modified: Wed, 25 Jun 2025 18:08:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7696a5f9b7e74a2aa514a55ac7e0cfe971b1141c3c5850830fb8e0689f90135a`  
		Last Modified: Wed, 25 Jun 2025 18:08:52 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95141cff2fd6549c5acae115725c4e519b8c7db11a411d0e9ad82b50c9b34933`  
		Last Modified: Wed, 25 Jun 2025 18:08:55 GMT  
		Size: 17.6 MB (17586160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e85fa937ebf06addcb8d1bbdba91a1e0e33297fe50a8ccf5498a3bc159cba6c`  
		Last Modified: Wed, 25 Jun 2025 18:08:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:68f5dd9b1a738661c4c28156a3a6991ffc58978ee0c97f94ce54420b8f0ba20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f9119e3abb10c3af2fe52c9872f6b58f7a68f9014b033b3e011746f9e262f9`

```dockerfile
```

-	Layers:
	-	`sha256:5d2c99dd36e26bd782604aa9a1d14e2cefa0620ba8ace2d9e4259bad786846ba`  
		Last Modified: Wed, 25 Jun 2025 20:07:49 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a6bdd6495f432d9e77784f68f76efbbb3c1876f32f241af8ec504eb422370bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154690467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367b736522af6576dc89a15b7ee3c18b96c615d7e19acbcc7337fcc9e369d27c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5b66d211d051c20b2b8fa072c573c801a3adfd1d5f78c9d8d98055034dc9e7`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 1.0 MB (1022998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c908d2ebbfc7e6af38b4d76f325a249fa359e7f524e0316bbac900fa8f5537d9`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e3f97ea27b30130cf4a126e578dc57f0c0083a14c56fd56f3f1c6b6fa5ac8c`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287bf6b6e7ca52eb877ac8a25ac379d4dee7dfe8d860e93321e2bea6e071b8bb`  
		Last Modified: Thu, 26 Jun 2025 03:49:23 GMT  
		Size: 18.0 MB (18017325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2657fca26a04fb60ad2dd915fd0c4265b8be7854c9d68e19e05ec4372bbaa4d9`  
		Last Modified: Thu, 26 Jun 2025 03:49:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:88444b092967d974c32eb7853e9c4b5224d33ba1f1c8d0d57229afa39d1e4a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e4e22e9b75ecb5b98766fb00c00d442bf16258821538c09572ea9c4121594`

```dockerfile
```

-	Layers:
	-	`sha256:8cf7d1bd28dd5d695964242d21c1d714fc4616311036c7fbf166b8c83e3d1403`  
		Last Modified: Thu, 26 Jun 2025 05:07:29 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:961151cbda8766cc99af45924dff0bbbe5c1cd4495373a695cf1dde042adf75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:4079ca5c6c04c424df4cd0952427103783d7f1d5ee13cf250feb9fa7daf702d3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542396755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd1d4f1571e67132e18d27de3ca1ad05ccf64dc10867dd91a34a3164f66a1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Wed, 25 Jun 2025 18:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 18:00:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 18:00:26 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 18:00:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 18:00:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:39 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 18:00:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 18:00:41 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 18:00:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 18:00:52 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 18:01:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b8ee3e9b4b19ac3cb8209b1fec6595c5c0f0fcabc7a9896a46d0ce1f8120bc`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c2dfd0eecb72a14ba95e5ea944ae4941085237952c6b1093966c4f7bfd81c0`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 413.4 KB (413433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732b2abe01a3c431782a440319afcda808697dceebe6fb33b0927e4755690a9`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c642d396a1d409b25ffd02b82f1d9dc6fa3292f21f7f5a51fa7d42f04c025931`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24e676af11cfd3f615a01c8fdecccf9838fe1ce9428ca1291b1492c3f652244`  
		Last Modified: Wed, 25 Jun 2025 18:04:48 GMT  
		Size: 20.9 MB (20871278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0ce9a47ab92c7c251fc9a4f319bc0a5c505107b9e40d0620cf8f928d0e8770`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5008628017fda828a9b90038aa68ea54ee822ac314c8cb4a176de73899dffe3`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72c88a732462f04bc82cda46e0d5bd6db2cb303a9902366d52b6cd1356c1358`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8648b2be10b75a285f1ad75edba61a2bdab08d39267a0998cf77a02d533c7b70`  
		Last Modified: Wed, 25 Jun 2025 18:04:49 GMT  
		Size: 22.7 MB (22693786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83073c0d9f0f34eb666f0222d2f49f718651544b64e4abe583410895710320a1`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35317ffe0ab3851bf4d623b78b15c97eb3e6af22fba759fd4c70636f41b4732`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4637463d4ffc77ae1c82079a154b8ec12faafaeffe0913a0d09deaf28bb49f7`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac7f531a859530f45f62257febda686a917ec0c545cd18a333d7fe3c0263e1`  
		Last Modified: Wed, 25 Jun 2025 18:04:50 GMT  
		Size: 22.2 MB (22232346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:70e34fc394cc0bbe07afb7936e0a6d10abae07e6343f2adfaf13cba9c0f6be17
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346284808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5b2835fcc7572b7508a52e3098bb05924a789e59baff2cf579969608ce543d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Wed, 25 Jun 2025 17:54:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 17:55:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 17:55:41 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 17:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 17:56:02 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 17:56:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 17:56:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fe415a5d4c4e0bf9f51cfbfd6c53baf78ef30a68f632d510e3173d228ec7e`  
		Last Modified: Wed, 25 Jun 2025 17:56:55 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d732acd5b34fa2dc704a91dde188904e8c977774edfa16f0bfa032200a611831`  
		Last Modified: Wed, 25 Jun 2025 17:56:56 GMT  
		Size: 356.3 KB (356325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb31ba7c382ae188ddfcd0df5bae106d2b1a66e54a578343ffd763ec23ee02c`  
		Last Modified: Wed, 25 Jun 2025 17:56:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacd2505104dc3c0daf2469a31a539880b7e41ee2017eb7b75bd204861800b6e`  
		Last Modified: Wed, 25 Jun 2025 17:56:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76a7d1495c30218a8b02c22b8199ee65ddc9041e1b67ecc868be2b5be8cde68`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 20.8 MB (20827807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ea181f6649206ff19d0147312fda9397ff0be604a29b9a2d5a129111b08fca`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ae454c928c4496c0f562fe3503157fa0d1a06b286d8a04c62641dc1fe604b0`  
		Last Modified: Wed, 25 Jun 2025 17:57:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ee2c6ab911fbbfd12f7eece75e8cd2107544bce17bf4054c509f5172a609c1`  
		Last Modified: Wed, 25 Jun 2025 17:57:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d3fa685524bda12581d5b1c38ad03460b11147adb582f2eb25ba0d40c97d4b`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 22.7 MB (22652434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d02f084c1719a8edce4ef03af5f09ec922f79f2214d443b99ed84aac6fd43`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421d689fa4721f56c6cdbb292a97e67b100810930f43c25e1216000154a1e57a`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ba7fc52773bf998c43237d460a09c65e59e6d4a1bb2e2d58e75cc23013d43`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112a0a68c74b56bf752081ce36f98ad96808d67fd81c0ab24f1744b08db9d9`  
		Last Modified: Wed, 25 Jun 2025 17:57:12 GMT  
		Size: 22.2 MB (22185055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3a63fe3d9ab8c76984d372685bf69740f4dc4b9f8b136c8144528d2a626e08a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:70e34fc394cc0bbe07afb7936e0a6d10abae07e6343f2adfaf13cba9c0f6be17
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346284808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5b2835fcc7572b7508a52e3098bb05924a789e59baff2cf579969608ce543d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Wed, 25 Jun 2025 17:54:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 17:55:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 17:55:41 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 17:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 17:56:02 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 17:56:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 17:56:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fe415a5d4c4e0bf9f51cfbfd6c53baf78ef30a68f632d510e3173d228ec7e`  
		Last Modified: Wed, 25 Jun 2025 17:56:55 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d732acd5b34fa2dc704a91dde188904e8c977774edfa16f0bfa032200a611831`  
		Last Modified: Wed, 25 Jun 2025 17:56:56 GMT  
		Size: 356.3 KB (356325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb31ba7c382ae188ddfcd0df5bae106d2b1a66e54a578343ffd763ec23ee02c`  
		Last Modified: Wed, 25 Jun 2025 17:56:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacd2505104dc3c0daf2469a31a539880b7e41ee2017eb7b75bd204861800b6e`  
		Last Modified: Wed, 25 Jun 2025 17:56:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76a7d1495c30218a8b02c22b8199ee65ddc9041e1b67ecc868be2b5be8cde68`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 20.8 MB (20827807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ea181f6649206ff19d0147312fda9397ff0be604a29b9a2d5a129111b08fca`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ae454c928c4496c0f562fe3503157fa0d1a06b286d8a04c62641dc1fe604b0`  
		Last Modified: Wed, 25 Jun 2025 17:57:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ee2c6ab911fbbfd12f7eece75e8cd2107544bce17bf4054c509f5172a609c1`  
		Last Modified: Wed, 25 Jun 2025 17:57:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d3fa685524bda12581d5b1c38ad03460b11147adb582f2eb25ba0d40c97d4b`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 22.7 MB (22652434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d02f084c1719a8edce4ef03af5f09ec922f79f2214d443b99ed84aac6fd43`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421d689fa4721f56c6cdbb292a97e67b100810930f43c25e1216000154a1e57a`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ba7fc52773bf998c43237d460a09c65e59e6d4a1bb2e2d58e75cc23013d43`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112a0a68c74b56bf752081ce36f98ad96808d67fd81c0ab24f1744b08db9d9`  
		Last Modified: Wed, 25 Jun 2025 17:57:12 GMT  
		Size: 22.2 MB (22185055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:3e78e4b3bbd7a8b9663fa3b09411da2139569cccfb6c179bb80cfa3c8b27a535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:4079ca5c6c04c424df4cd0952427103783d7f1d5ee13cf250feb9fa7daf702d3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542396755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd1d4f1571e67132e18d27de3ca1ad05ccf64dc10867dd91a34a3164f66a1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Wed, 25 Jun 2025 18:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 18:00:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 18:00:26 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 18:00:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 18:00:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:39 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 18:00:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 18:00:41 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 18:00:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 18:00:52 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 18:01:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b8ee3e9b4b19ac3cb8209b1fec6595c5c0f0fcabc7a9896a46d0ce1f8120bc`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c2dfd0eecb72a14ba95e5ea944ae4941085237952c6b1093966c4f7bfd81c0`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 413.4 KB (413433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732b2abe01a3c431782a440319afcda808697dceebe6fb33b0927e4755690a9`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c642d396a1d409b25ffd02b82f1d9dc6fa3292f21f7f5a51fa7d42f04c025931`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24e676af11cfd3f615a01c8fdecccf9838fe1ce9428ca1291b1492c3f652244`  
		Last Modified: Wed, 25 Jun 2025 18:04:48 GMT  
		Size: 20.9 MB (20871278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0ce9a47ab92c7c251fc9a4f319bc0a5c505107b9e40d0620cf8f928d0e8770`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5008628017fda828a9b90038aa68ea54ee822ac314c8cb4a176de73899dffe3`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72c88a732462f04bc82cda46e0d5bd6db2cb303a9902366d52b6cd1356c1358`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8648b2be10b75a285f1ad75edba61a2bdab08d39267a0998cf77a02d533c7b70`  
		Last Modified: Wed, 25 Jun 2025 18:04:49 GMT  
		Size: 22.7 MB (22693786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83073c0d9f0f34eb666f0222d2f49f718651544b64e4abe583410895710320a1`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35317ffe0ab3851bf4d623b78b15c97eb3e6af22fba759fd4c70636f41b4732`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4637463d4ffc77ae1c82079a154b8ec12faafaeffe0913a0d09deaf28bb49f7`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac7f531a859530f45f62257febda686a917ec0c545cd18a333d7fe3c0263e1`  
		Last Modified: Wed, 25 Jun 2025 18:04:50 GMT  
		Size: 22.2 MB (22232346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3`

```console
$ docker pull docker@sha256:d33eb93fe02683e984e6f8a93c0b3d85bb74f56ec83922bc39fb34ba23ab42bc
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

### `docker:28.3` - linux; amd64

```console
$ docker pull docker@sha256:bd5712b912e233b9cbca5ed94664dda05655537f56323d55f5435be0df084f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144906835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6892cb0e669d8bf6d40d1421bfd62b0aec81041706f7b45de7a03514cfef527b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:6d82b2f6555dd414407f11111af5c2028f1205e50140594c33edfdaf9add7fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281f5c43f6b438ece0586157f96cec3dbde12c3e55fb80b93dcb5e08c92bc9c0`

```dockerfile
```

-	Layers:
	-	`sha256:f99b7342f71018419b6d22e5f772de11b7f1619ac5707ad3f2610ac9f834684c`  
		Last Modified: Wed, 25 Jun 2025 20:07:28 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:0e7bd5b322a7adee7f87d5da6133602a1b13943207c1c119e3fa8bc150662de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135881655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e5f0a26fdef7325b82b98ac05955a1e1ab6990eee865f5d40b5eb1c2b380f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ff3c42dfe8b909933270cb290d5b16dad7c39ef1c61d930695bccb4af028b`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 7.2 MB (7230273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf5f2cd81da4f9935d1b8f1e0c69e9690065ce54192c47285c02007b855ab71`  
		Last Modified: Wed, 25 Jun 2025 19:09:57 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9315c92c22796071003a7353007bcfafc2dde73136adc0ee6c1f859c9ead82`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eabbd9d791bab2458faac47bddb10b59b825dc9b8a6e958d893dad0d62d2b13`  
		Last Modified: Wed, 25 Jun 2025 19:10:07 GMT  
		Size: 58.2 MB (58196245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2fa52243ccad08598f463d20022392c4e63de6a7fa3389a2d3f13bc5072850`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18747036c5bfd27297ec304b7871a2c0a0cab99bc9cac7dcd22593dc95f704d0`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:999ce16d0b42a6156eae74e0a48680ba57dfefa8409ec8cb3140e4abfa0b8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1afb05bba7f7a8f5e78c1e59548ece1fd7da038bb3addbbb866344b023c03`

```dockerfile
```

-	Layers:
	-	`sha256:9849cf691a13b263da46b7691c04aa707880fde9055dd21ca78616d50691794a`  
		Last Modified: Wed, 25 Jun 2025 20:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4c6ec3de04e99f6aba4a50701988210b9d0bfbcee4f4715aba2b6f968145ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134179998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e5f59ba3ffbbe22e927ebf4f2cfd1f28d553a63e5803230880f12c7bb9137d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a13ff228646fe31640f66680c77b8179b59cf030776d4dc27e0b8a4073a1161`  
		Last Modified: Wed, 25 Jun 2025 19:09:40 GMT  
		Size: 6.5 MB (6538132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e439188892f1f8a228ea037911e2843fc2f69b92e2847007cf69bfb07cae8e9`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 86.5 KB (86492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82b72c117f21d49e7e8d6934422e959de7f39d5971cb8bf2bc5a612c6f321b6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5741868cb033a7c74a817afc1bbfc0b66636546ad2b2819fd90b5b72cd7314`  
		Last Modified: Wed, 25 Jun 2025 19:09:44 GMT  
		Size: 58.2 MB (58196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f745e31047d1161b57e77243e0a39cfb9fc008c772fa16ee7c67ed75c9051b`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbf907fef629de9d464812fadbd09c96845cd8dcf8c4c1acf19dbc216347bc6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:5e7ea7e55af96477d6205063362129df645015586d168d3abc5fddf5af1f9756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77876fbab01e5b51149471bea0941cfcebf64d55778d638330e8ec92546e5340`

```dockerfile
```

-	Layers:
	-	`sha256:35d28f9246501c698aa882110ff7cb8d3d1ee99e8454a3b8fac5fa6665d20ca9`  
		Last Modified: Wed, 25 Jun 2025 20:07:35 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:852d19966630687c3ad157b217ace73e93c823aaf34c396f4aaef675bee52a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135648800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b957e61342f7dd8223305f18ccc713082c3ef5c69722449cb8b8fdbeb8319012`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:a2c73991ca6ca907adb176cce487de5342c67b9d610999b2711012d6dae3fd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070a2badedc718d9b3896e9dcd97389153b5d537dcaaaf577fe0560b77eb6e2`

```dockerfile
```

-	Layers:
	-	`sha256:364f514ac25163eb6400a49f2a109178e8f6779987fe82a10b5bb1acbf9282bc`  
		Last Modified: Thu, 26 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-cli`

```console
$ docker pull docker@sha256:be316e9f9a158bdd04d175cac7867be4561d9718c8f45331ba09f839854d6ac4
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

### `docker:28.3-cli` - linux; amd64

```console
$ docker pull docker@sha256:e15d465988c670df7863f019b7bbffadc2fb5a89355183d2f77c9541af6f5f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75386866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c308218afb92593639450e489ef8638050ab55a6c49065a2fbc8a52f70bd7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:95954b4d8cb3ecd9e948ffac374a91f07bfeffef3b0c5c17dd0f6aaa5deab1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf73ac7a434f1e1608f059171e612c92ef03248ba073d582b984939f205e7bb`

```dockerfile
```

-	Layers:
	-	`sha256:659dc4fc8c676ae5ecee4b9f1c73a5096d5d03e6459f28d1554f3f2211f5a592`  
		Last Modified: Wed, 25 Jun 2025 20:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ca185f5711941016ddadcfaa648bdc27c90418f2282d093c6bc751aa3e7ba38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70359081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9ff19e1547d18c4a360fa003b26cb878d2f1ec67647bc6159bfb0320fd306`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8bd2cad79060bb5785bed3792250043dec874b2660a91b8acff6cbbd7c39bbbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee647cfa7ad7371b150be4ce91c2395bcd50e25ae0986066f39ec2db1307b8ef`

```dockerfile
```

-	Layers:
	-	`sha256:3c84ecc5e16e1816184f43bbc41f0010df0495baeb95c58e0b47743bbecfb4e7`  
		Last Modified: Wed, 25 Jun 2025 20:07:48 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:7f2567fc8f1b52e8b7fc40fbec2270157a426255e299307c1fdf6291134a4bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69353151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f148d0ade3d87c4d8d77dd87529f575e2008e919bb844a947247561ec03c82db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:234783c583655b5fba47f029b646f86832181f4e7693051a58456c45043c099c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8693516fb4d64dd200448d3da2a32b3deb0e4634e4f4faaa6dc35984a4d873e`

```dockerfile
```

-	Layers:
	-	`sha256:d7b8ebd195f16dbf716810084fd30cbc4943c0d20f94cf8055a15691fd5203ce`  
		Last Modified: Wed, 25 Jun 2025 20:07:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2b4c39548793a279667d4ced40e5e68af421e8ff4000c101ee2f7e5b299573b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70940773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c4520ee754d509808a5e81ed1749fcb77b10dea95542447afafeccebaca66e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:026dc96b447b564878e37a1732f26aa77491519e943779e9f5e336580774335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a66b0aed9a637a80f3fbfb7b609cc336667c89535146dd5bda65fc05777ce3`

```dockerfile
```

-	Layers:
	-	`sha256:c2f530f380386ce5972d923f6ec42373f519edff7acfd63e4e1934eeb86652b4`  
		Last Modified: Wed, 25 Jun 2025 20:07:54 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-dind`

```console
$ docker pull docker@sha256:d33eb93fe02683e984e6f8a93c0b3d85bb74f56ec83922bc39fb34ba23ab42bc
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

### `docker:28.3-dind` - linux; amd64

```console
$ docker pull docker@sha256:bd5712b912e233b9cbca5ed94664dda05655537f56323d55f5435be0df084f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144906835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6892cb0e669d8bf6d40d1421bfd62b0aec81041706f7b45de7a03514cfef527b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6d82b2f6555dd414407f11111af5c2028f1205e50140594c33edfdaf9add7fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281f5c43f6b438ece0586157f96cec3dbde12c3e55fb80b93dcb5e08c92bc9c0`

```dockerfile
```

-	Layers:
	-	`sha256:f99b7342f71018419b6d22e5f772de11b7f1619ac5707ad3f2610ac9f834684c`  
		Last Modified: Wed, 25 Jun 2025 20:07:28 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:0e7bd5b322a7adee7f87d5da6133602a1b13943207c1c119e3fa8bc150662de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135881655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e5f0a26fdef7325b82b98ac05955a1e1ab6990eee865f5d40b5eb1c2b380f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ff3c42dfe8b909933270cb290d5b16dad7c39ef1c61d930695bccb4af028b`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 7.2 MB (7230273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf5f2cd81da4f9935d1b8f1e0c69e9690065ce54192c47285c02007b855ab71`  
		Last Modified: Wed, 25 Jun 2025 19:09:57 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9315c92c22796071003a7353007bcfafc2dde73136adc0ee6c1f859c9ead82`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eabbd9d791bab2458faac47bddb10b59b825dc9b8a6e958d893dad0d62d2b13`  
		Last Modified: Wed, 25 Jun 2025 19:10:07 GMT  
		Size: 58.2 MB (58196245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2fa52243ccad08598f463d20022392c4e63de6a7fa3389a2d3f13bc5072850`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18747036c5bfd27297ec304b7871a2c0a0cab99bc9cac7dcd22593dc95f704d0`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:999ce16d0b42a6156eae74e0a48680ba57dfefa8409ec8cb3140e4abfa0b8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1afb05bba7f7a8f5e78c1e59548ece1fd7da038bb3addbbb866344b023c03`

```dockerfile
```

-	Layers:
	-	`sha256:9849cf691a13b263da46b7691c04aa707880fde9055dd21ca78616d50691794a`  
		Last Modified: Wed, 25 Jun 2025 20:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4c6ec3de04e99f6aba4a50701988210b9d0bfbcee4f4715aba2b6f968145ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134179998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e5f59ba3ffbbe22e927ebf4f2cfd1f28d553a63e5803230880f12c7bb9137d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a13ff228646fe31640f66680c77b8179b59cf030776d4dc27e0b8a4073a1161`  
		Last Modified: Wed, 25 Jun 2025 19:09:40 GMT  
		Size: 6.5 MB (6538132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e439188892f1f8a228ea037911e2843fc2f69b92e2847007cf69bfb07cae8e9`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 86.5 KB (86492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82b72c117f21d49e7e8d6934422e959de7f39d5971cb8bf2bc5a612c6f321b6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5741868cb033a7c74a817afc1bbfc0b66636546ad2b2819fd90b5b72cd7314`  
		Last Modified: Wed, 25 Jun 2025 19:09:44 GMT  
		Size: 58.2 MB (58196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f745e31047d1161b57e77243e0a39cfb9fc008c772fa16ee7c67ed75c9051b`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbf907fef629de9d464812fadbd09c96845cd8dcf8c4c1acf19dbc216347bc6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5e7ea7e55af96477d6205063362129df645015586d168d3abc5fddf5af1f9756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77876fbab01e5b51149471bea0941cfcebf64d55778d638330e8ec92546e5340`

```dockerfile
```

-	Layers:
	-	`sha256:35d28f9246501c698aa882110ff7cb8d3d1ee99e8454a3b8fac5fa6665d20ca9`  
		Last Modified: Wed, 25 Jun 2025 20:07:35 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:852d19966630687c3ad157b217ace73e93c823aaf34c396f4aaef675bee52a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135648800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b957e61342f7dd8223305f18ccc713082c3ef5c69722449cb8b8fdbeb8319012`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a2c73991ca6ca907adb176cce487de5342c67b9d610999b2711012d6dae3fd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070a2badedc718d9b3896e9dcd97389153b5d537dcaaaf577fe0560b77eb6e2`

```dockerfile
```

-	Layers:
	-	`sha256:364f514ac25163eb6400a49f2a109178e8f6779987fe82a10b5bb1acbf9282bc`  
		Last Modified: Thu, 26 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-dind-rootless`

```console
$ docker pull docker@sha256:6c2c0d6beb885c9c9741e9227a2c8bb25126b948831afda4a6c4221d6cadbb91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:7fafee3e6a673e4c95d8b8583e939baa5c4103872c26d5074032bb49e8643b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163487607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f7bdc571bf67b9957bd1f5fe4522ba3f5fd48b35b409599e6c30f10c3ca55f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101bccb38f5fc26e226b3aed7f5d43d304a31e4ae35365d48a66d9fc6b533934`  
		Last Modified: Wed, 25 Jun 2025 18:08:52 GMT  
		Size: 993.3 KB (993273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a974f1a114c34599fb5b4760b77413667489c7048fcc9ac21ce87e5cf6422b`  
		Last Modified: Wed, 25 Jun 2025 18:08:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7696a5f9b7e74a2aa514a55ac7e0cfe971b1141c3c5850830fb8e0689f90135a`  
		Last Modified: Wed, 25 Jun 2025 18:08:52 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95141cff2fd6549c5acae115725c4e519b8c7db11a411d0e9ad82b50c9b34933`  
		Last Modified: Wed, 25 Jun 2025 18:08:55 GMT  
		Size: 17.6 MB (17586160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e85fa937ebf06addcb8d1bbdba91a1e0e33297fe50a8ccf5498a3bc159cba6c`  
		Last Modified: Wed, 25 Jun 2025 18:08:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:68f5dd9b1a738661c4c28156a3a6991ffc58978ee0c97f94ce54420b8f0ba20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f9119e3abb10c3af2fe52c9872f6b58f7a68f9014b033b3e011746f9e262f9`

```dockerfile
```

-	Layers:
	-	`sha256:5d2c99dd36e26bd782604aa9a1d14e2cefa0620ba8ace2d9e4259bad786846ba`  
		Last Modified: Wed, 25 Jun 2025 20:07:49 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a6bdd6495f432d9e77784f68f76efbbb3c1876f32f241af8ec504eb422370bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154690467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367b736522af6576dc89a15b7ee3c18b96c615d7e19acbcc7337fcc9e369d27c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5b66d211d051c20b2b8fa072c573c801a3adfd1d5f78c9d8d98055034dc9e7`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 1.0 MB (1022998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c908d2ebbfc7e6af38b4d76f325a249fa359e7f524e0316bbac900fa8f5537d9`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e3f97ea27b30130cf4a126e578dc57f0c0083a14c56fd56f3f1c6b6fa5ac8c`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287bf6b6e7ca52eb877ac8a25ac379d4dee7dfe8d860e93321e2bea6e071b8bb`  
		Last Modified: Thu, 26 Jun 2025 03:49:23 GMT  
		Size: 18.0 MB (18017325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2657fca26a04fb60ad2dd915fd0c4265b8be7854c9d68e19e05ec4372bbaa4d9`  
		Last Modified: Thu, 26 Jun 2025 03:49:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:88444b092967d974c32eb7853e9c4b5224d33ba1f1c8d0d57229afa39d1e4a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e4e22e9b75ecb5b98766fb00c00d442bf16258821538c09572ea9c4121594`

```dockerfile
```

-	Layers:
	-	`sha256:8cf7d1bd28dd5d695964242d21c1d714fc4616311036c7fbf166b8c83e3d1403`  
		Last Modified: Thu, 26 Jun 2025 05:07:29 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-windowsservercore`

```console
$ docker pull docker@sha256:961151cbda8766cc99af45924dff0bbbe5c1cd4495373a695cf1dde042adf75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:28.3-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:4079ca5c6c04c424df4cd0952427103783d7f1d5ee13cf250feb9fa7daf702d3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542396755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd1d4f1571e67132e18d27de3ca1ad05ccf64dc10867dd91a34a3164f66a1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Wed, 25 Jun 2025 18:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 18:00:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 18:00:26 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 18:00:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 18:00:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:39 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 18:00:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 18:00:41 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 18:00:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 18:00:52 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 18:01:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b8ee3e9b4b19ac3cb8209b1fec6595c5c0f0fcabc7a9896a46d0ce1f8120bc`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c2dfd0eecb72a14ba95e5ea944ae4941085237952c6b1093966c4f7bfd81c0`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 413.4 KB (413433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732b2abe01a3c431782a440319afcda808697dceebe6fb33b0927e4755690a9`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c642d396a1d409b25ffd02b82f1d9dc6fa3292f21f7f5a51fa7d42f04c025931`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24e676af11cfd3f615a01c8fdecccf9838fe1ce9428ca1291b1492c3f652244`  
		Last Modified: Wed, 25 Jun 2025 18:04:48 GMT  
		Size: 20.9 MB (20871278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0ce9a47ab92c7c251fc9a4f319bc0a5c505107b9e40d0620cf8f928d0e8770`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5008628017fda828a9b90038aa68ea54ee822ac314c8cb4a176de73899dffe3`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72c88a732462f04bc82cda46e0d5bd6db2cb303a9902366d52b6cd1356c1358`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8648b2be10b75a285f1ad75edba61a2bdab08d39267a0998cf77a02d533c7b70`  
		Last Modified: Wed, 25 Jun 2025 18:04:49 GMT  
		Size: 22.7 MB (22693786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83073c0d9f0f34eb666f0222d2f49f718651544b64e4abe583410895710320a1`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35317ffe0ab3851bf4d623b78b15c97eb3e6af22fba759fd4c70636f41b4732`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4637463d4ffc77ae1c82079a154b8ec12faafaeffe0913a0d09deaf28bb49f7`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac7f531a859530f45f62257febda686a917ec0c545cd18a333d7fe3c0263e1`  
		Last Modified: Wed, 25 Jun 2025 18:04:50 GMT  
		Size: 22.2 MB (22232346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.3-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:70e34fc394cc0bbe07afb7936e0a6d10abae07e6343f2adfaf13cba9c0f6be17
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346284808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5b2835fcc7572b7508a52e3098bb05924a789e59baff2cf579969608ce543d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Wed, 25 Jun 2025 17:54:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 17:55:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 17:55:41 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 17:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 17:56:02 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 17:56:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 17:56:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fe415a5d4c4e0bf9f51cfbfd6c53baf78ef30a68f632d510e3173d228ec7e`  
		Last Modified: Wed, 25 Jun 2025 17:56:55 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d732acd5b34fa2dc704a91dde188904e8c977774edfa16f0bfa032200a611831`  
		Last Modified: Wed, 25 Jun 2025 17:56:56 GMT  
		Size: 356.3 KB (356325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb31ba7c382ae188ddfcd0df5bae106d2b1a66e54a578343ffd763ec23ee02c`  
		Last Modified: Wed, 25 Jun 2025 17:56:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacd2505104dc3c0daf2469a31a539880b7e41ee2017eb7b75bd204861800b6e`  
		Last Modified: Wed, 25 Jun 2025 17:56:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76a7d1495c30218a8b02c22b8199ee65ddc9041e1b67ecc868be2b5be8cde68`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 20.8 MB (20827807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ea181f6649206ff19d0147312fda9397ff0be604a29b9a2d5a129111b08fca`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ae454c928c4496c0f562fe3503157fa0d1a06b286d8a04c62641dc1fe604b0`  
		Last Modified: Wed, 25 Jun 2025 17:57:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ee2c6ab911fbbfd12f7eece75e8cd2107544bce17bf4054c509f5172a609c1`  
		Last Modified: Wed, 25 Jun 2025 17:57:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d3fa685524bda12581d5b1c38ad03460b11147adb582f2eb25ba0d40c97d4b`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 22.7 MB (22652434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d02f084c1719a8edce4ef03af5f09ec922f79f2214d443b99ed84aac6fd43`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421d689fa4721f56c6cdbb292a97e67b100810930f43c25e1216000154a1e57a`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ba7fc52773bf998c43237d460a09c65e59e6d4a1bb2e2d58e75cc23013d43`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112a0a68c74b56bf752081ce36f98ad96808d67fd81c0ab24f1744b08db9d9`  
		Last Modified: Wed, 25 Jun 2025 17:57:12 GMT  
		Size: 22.2 MB (22185055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3a63fe3d9ab8c76984d372685bf69740f4dc4b9f8b136c8144528d2a626e08a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:28.3-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:70e34fc394cc0bbe07afb7936e0a6d10abae07e6343f2adfaf13cba9c0f6be17
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346284808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5b2835fcc7572b7508a52e3098bb05924a789e59baff2cf579969608ce543d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Wed, 25 Jun 2025 17:54:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 17:55:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 17:55:41 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 17:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 17:56:02 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 17:56:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 17:56:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fe415a5d4c4e0bf9f51cfbfd6c53baf78ef30a68f632d510e3173d228ec7e`  
		Last Modified: Wed, 25 Jun 2025 17:56:55 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d732acd5b34fa2dc704a91dde188904e8c977774edfa16f0bfa032200a611831`  
		Last Modified: Wed, 25 Jun 2025 17:56:56 GMT  
		Size: 356.3 KB (356325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb31ba7c382ae188ddfcd0df5bae106d2b1a66e54a578343ffd763ec23ee02c`  
		Last Modified: Wed, 25 Jun 2025 17:56:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacd2505104dc3c0daf2469a31a539880b7e41ee2017eb7b75bd204861800b6e`  
		Last Modified: Wed, 25 Jun 2025 17:56:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76a7d1495c30218a8b02c22b8199ee65ddc9041e1b67ecc868be2b5be8cde68`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 20.8 MB (20827807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ea181f6649206ff19d0147312fda9397ff0be604a29b9a2d5a129111b08fca`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ae454c928c4496c0f562fe3503157fa0d1a06b286d8a04c62641dc1fe604b0`  
		Last Modified: Wed, 25 Jun 2025 17:57:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ee2c6ab911fbbfd12f7eece75e8cd2107544bce17bf4054c509f5172a609c1`  
		Last Modified: Wed, 25 Jun 2025 17:57:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d3fa685524bda12581d5b1c38ad03460b11147adb582f2eb25ba0d40c97d4b`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 22.7 MB (22652434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d02f084c1719a8edce4ef03af5f09ec922f79f2214d443b99ed84aac6fd43`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421d689fa4721f56c6cdbb292a97e67b100810930f43c25e1216000154a1e57a`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ba7fc52773bf998c43237d460a09c65e59e6d4a1bb2e2d58e75cc23013d43`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112a0a68c74b56bf752081ce36f98ad96808d67fd81c0ab24f1744b08db9d9`  
		Last Modified: Wed, 25 Jun 2025 17:57:12 GMT  
		Size: 22.2 MB (22185055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:3e78e4b3bbd7a8b9663fa3b09411da2139569cccfb6c179bb80cfa3c8b27a535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28.3-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:4079ca5c6c04c424df4cd0952427103783d7f1d5ee13cf250feb9fa7daf702d3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542396755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd1d4f1571e67132e18d27de3ca1ad05ccf64dc10867dd91a34a3164f66a1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Wed, 25 Jun 2025 18:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 18:00:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 18:00:26 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 18:00:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 18:00:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:39 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 18:00:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 18:00:41 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 18:00:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 18:00:52 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 18:01:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b8ee3e9b4b19ac3cb8209b1fec6595c5c0f0fcabc7a9896a46d0ce1f8120bc`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c2dfd0eecb72a14ba95e5ea944ae4941085237952c6b1093966c4f7bfd81c0`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 413.4 KB (413433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732b2abe01a3c431782a440319afcda808697dceebe6fb33b0927e4755690a9`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c642d396a1d409b25ffd02b82f1d9dc6fa3292f21f7f5a51fa7d42f04c025931`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24e676af11cfd3f615a01c8fdecccf9838fe1ce9428ca1291b1492c3f652244`  
		Last Modified: Wed, 25 Jun 2025 18:04:48 GMT  
		Size: 20.9 MB (20871278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0ce9a47ab92c7c251fc9a4f319bc0a5c505107b9e40d0620cf8f928d0e8770`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5008628017fda828a9b90038aa68ea54ee822ac314c8cb4a176de73899dffe3`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72c88a732462f04bc82cda46e0d5bd6db2cb303a9902366d52b6cd1356c1358`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8648b2be10b75a285f1ad75edba61a2bdab08d39267a0998cf77a02d533c7b70`  
		Last Modified: Wed, 25 Jun 2025 18:04:49 GMT  
		Size: 22.7 MB (22693786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83073c0d9f0f34eb666f0222d2f49f718651544b64e4abe583410895710320a1`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35317ffe0ab3851bf4d623b78b15c97eb3e6af22fba759fd4c70636f41b4732`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4637463d4ffc77ae1c82079a154b8ec12faafaeffe0913a0d09deaf28bb49f7`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac7f531a859530f45f62257febda686a917ec0c545cd18a333d7fe3c0263e1`  
		Last Modified: Wed, 25 Jun 2025 18:04:50 GMT  
		Size: 22.2 MB (22232346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3.0`

```console
$ docker pull docker@sha256:d33eb93fe02683e984e6f8a93c0b3d85bb74f56ec83922bc39fb34ba23ab42bc
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

### `docker:28.3.0` - linux; amd64

```console
$ docker pull docker@sha256:bd5712b912e233b9cbca5ed94664dda05655537f56323d55f5435be0df084f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144906835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6892cb0e669d8bf6d40d1421bfd62b0aec81041706f7b45de7a03514cfef527b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0` - unknown; unknown

```console
$ docker pull docker@sha256:6d82b2f6555dd414407f11111af5c2028f1205e50140594c33edfdaf9add7fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281f5c43f6b438ece0586157f96cec3dbde12c3e55fb80b93dcb5e08c92bc9c0`

```dockerfile
```

-	Layers:
	-	`sha256:f99b7342f71018419b6d22e5f772de11b7f1619ac5707ad3f2610ac9f834684c`  
		Last Modified: Wed, 25 Jun 2025 20:07:28 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:0e7bd5b322a7adee7f87d5da6133602a1b13943207c1c119e3fa8bc150662de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135881655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e5f0a26fdef7325b82b98ac05955a1e1ab6990eee865f5d40b5eb1c2b380f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ff3c42dfe8b909933270cb290d5b16dad7c39ef1c61d930695bccb4af028b`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 7.2 MB (7230273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf5f2cd81da4f9935d1b8f1e0c69e9690065ce54192c47285c02007b855ab71`  
		Last Modified: Wed, 25 Jun 2025 19:09:57 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9315c92c22796071003a7353007bcfafc2dde73136adc0ee6c1f859c9ead82`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eabbd9d791bab2458faac47bddb10b59b825dc9b8a6e958d893dad0d62d2b13`  
		Last Modified: Wed, 25 Jun 2025 19:10:07 GMT  
		Size: 58.2 MB (58196245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2fa52243ccad08598f463d20022392c4e63de6a7fa3389a2d3f13bc5072850`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18747036c5bfd27297ec304b7871a2c0a0cab99bc9cac7dcd22593dc95f704d0`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0` - unknown; unknown

```console
$ docker pull docker@sha256:999ce16d0b42a6156eae74e0a48680ba57dfefa8409ec8cb3140e4abfa0b8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1afb05bba7f7a8f5e78c1e59548ece1fd7da038bb3addbbb866344b023c03`

```dockerfile
```

-	Layers:
	-	`sha256:9849cf691a13b263da46b7691c04aa707880fde9055dd21ca78616d50691794a`  
		Last Modified: Wed, 25 Jun 2025 20:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4c6ec3de04e99f6aba4a50701988210b9d0bfbcee4f4715aba2b6f968145ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134179998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e5f59ba3ffbbe22e927ebf4f2cfd1f28d553a63e5803230880f12c7bb9137d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a13ff228646fe31640f66680c77b8179b59cf030776d4dc27e0b8a4073a1161`  
		Last Modified: Wed, 25 Jun 2025 19:09:40 GMT  
		Size: 6.5 MB (6538132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e439188892f1f8a228ea037911e2843fc2f69b92e2847007cf69bfb07cae8e9`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 86.5 KB (86492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82b72c117f21d49e7e8d6934422e959de7f39d5971cb8bf2bc5a612c6f321b6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5741868cb033a7c74a817afc1bbfc0b66636546ad2b2819fd90b5b72cd7314`  
		Last Modified: Wed, 25 Jun 2025 19:09:44 GMT  
		Size: 58.2 MB (58196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f745e31047d1161b57e77243e0a39cfb9fc008c772fa16ee7c67ed75c9051b`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbf907fef629de9d464812fadbd09c96845cd8dcf8c4c1acf19dbc216347bc6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0` - unknown; unknown

```console
$ docker pull docker@sha256:5e7ea7e55af96477d6205063362129df645015586d168d3abc5fddf5af1f9756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77876fbab01e5b51149471bea0941cfcebf64d55778d638330e8ec92546e5340`

```dockerfile
```

-	Layers:
	-	`sha256:35d28f9246501c698aa882110ff7cb8d3d1ee99e8454a3b8fac5fa6665d20ca9`  
		Last Modified: Wed, 25 Jun 2025 20:07:35 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:852d19966630687c3ad157b217ace73e93c823aaf34c396f4aaef675bee52a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135648800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b957e61342f7dd8223305f18ccc713082c3ef5c69722449cb8b8fdbeb8319012`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0` - unknown; unknown

```console
$ docker pull docker@sha256:a2c73991ca6ca907adb176cce487de5342c67b9d610999b2711012d6dae3fd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070a2badedc718d9b3896e9dcd97389153b5d537dcaaaf577fe0560b77eb6e2`

```dockerfile
```

-	Layers:
	-	`sha256:364f514ac25163eb6400a49f2a109178e8f6779987fe82a10b5bb1acbf9282bc`  
		Last Modified: Thu, 26 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.0-alpine3.22`

```console
$ docker pull docker@sha256:d33eb93fe02683e984e6f8a93c0b3d85bb74f56ec83922bc39fb34ba23ab42bc
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

### `docker:28.3.0-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:bd5712b912e233b9cbca5ed94664dda05655537f56323d55f5435be0df084f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144906835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6892cb0e669d8bf6d40d1421bfd62b0aec81041706f7b45de7a03514cfef527b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6d82b2f6555dd414407f11111af5c2028f1205e50140594c33edfdaf9add7fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281f5c43f6b438ece0586157f96cec3dbde12c3e55fb80b93dcb5e08c92bc9c0`

```dockerfile
```

-	Layers:
	-	`sha256:f99b7342f71018419b6d22e5f772de11b7f1619ac5707ad3f2610ac9f834684c`  
		Last Modified: Wed, 25 Jun 2025 20:07:28 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:0e7bd5b322a7adee7f87d5da6133602a1b13943207c1c119e3fa8bc150662de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135881655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e5f0a26fdef7325b82b98ac05955a1e1ab6990eee865f5d40b5eb1c2b380f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ff3c42dfe8b909933270cb290d5b16dad7c39ef1c61d930695bccb4af028b`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 7.2 MB (7230273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf5f2cd81da4f9935d1b8f1e0c69e9690065ce54192c47285c02007b855ab71`  
		Last Modified: Wed, 25 Jun 2025 19:09:57 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9315c92c22796071003a7353007bcfafc2dde73136adc0ee6c1f859c9ead82`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eabbd9d791bab2458faac47bddb10b59b825dc9b8a6e958d893dad0d62d2b13`  
		Last Modified: Wed, 25 Jun 2025 19:10:07 GMT  
		Size: 58.2 MB (58196245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2fa52243ccad08598f463d20022392c4e63de6a7fa3389a2d3f13bc5072850`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18747036c5bfd27297ec304b7871a2c0a0cab99bc9cac7dcd22593dc95f704d0`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:999ce16d0b42a6156eae74e0a48680ba57dfefa8409ec8cb3140e4abfa0b8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1afb05bba7f7a8f5e78c1e59548ece1fd7da038bb3addbbb866344b023c03`

```dockerfile
```

-	Layers:
	-	`sha256:9849cf691a13b263da46b7691c04aa707880fde9055dd21ca78616d50691794a`  
		Last Modified: Wed, 25 Jun 2025 20:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4c6ec3de04e99f6aba4a50701988210b9d0bfbcee4f4715aba2b6f968145ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134179998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e5f59ba3ffbbe22e927ebf4f2cfd1f28d553a63e5803230880f12c7bb9137d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a13ff228646fe31640f66680c77b8179b59cf030776d4dc27e0b8a4073a1161`  
		Last Modified: Wed, 25 Jun 2025 19:09:40 GMT  
		Size: 6.5 MB (6538132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e439188892f1f8a228ea037911e2843fc2f69b92e2847007cf69bfb07cae8e9`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 86.5 KB (86492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82b72c117f21d49e7e8d6934422e959de7f39d5971cb8bf2bc5a612c6f321b6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5741868cb033a7c74a817afc1bbfc0b66636546ad2b2819fd90b5b72cd7314`  
		Last Modified: Wed, 25 Jun 2025 19:09:44 GMT  
		Size: 58.2 MB (58196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f745e31047d1161b57e77243e0a39cfb9fc008c772fa16ee7c67ed75c9051b`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbf907fef629de9d464812fadbd09c96845cd8dcf8c4c1acf19dbc216347bc6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:5e7ea7e55af96477d6205063362129df645015586d168d3abc5fddf5af1f9756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77876fbab01e5b51149471bea0941cfcebf64d55778d638330e8ec92546e5340`

```dockerfile
```

-	Layers:
	-	`sha256:35d28f9246501c698aa882110ff7cb8d3d1ee99e8454a3b8fac5fa6665d20ca9`  
		Last Modified: Wed, 25 Jun 2025 20:07:35 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:852d19966630687c3ad157b217ace73e93c823aaf34c396f4aaef675bee52a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135648800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b957e61342f7dd8223305f18ccc713082c3ef5c69722449cb8b8fdbeb8319012`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:a2c73991ca6ca907adb176cce487de5342c67b9d610999b2711012d6dae3fd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070a2badedc718d9b3896e9dcd97389153b5d537dcaaaf577fe0560b77eb6e2`

```dockerfile
```

-	Layers:
	-	`sha256:364f514ac25163eb6400a49f2a109178e8f6779987fe82a10b5bb1acbf9282bc`  
		Last Modified: Thu, 26 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.0-cli`

```console
$ docker pull docker@sha256:be316e9f9a158bdd04d175cac7867be4561d9718c8f45331ba09f839854d6ac4
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

### `docker:28.3.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:e15d465988c670df7863f019b7bbffadc2fb5a89355183d2f77c9541af6f5f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75386866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c308218afb92593639450e489ef8638050ab55a6c49065a2fbc8a52f70bd7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:95954b4d8cb3ecd9e948ffac374a91f07bfeffef3b0c5c17dd0f6aaa5deab1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf73ac7a434f1e1608f059171e612c92ef03248ba073d582b984939f205e7bb`

```dockerfile
```

-	Layers:
	-	`sha256:659dc4fc8c676ae5ecee4b9f1c73a5096d5d03e6459f28d1554f3f2211f5a592`  
		Last Modified: Wed, 25 Jun 2025 20:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ca185f5711941016ddadcfaa648bdc27c90418f2282d093c6bc751aa3e7ba38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70359081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9ff19e1547d18c4a360fa003b26cb878d2f1ec67647bc6159bfb0320fd306`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8bd2cad79060bb5785bed3792250043dec874b2660a91b8acff6cbbd7c39bbbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee647cfa7ad7371b150be4ce91c2395bcd50e25ae0986066f39ec2db1307b8ef`

```dockerfile
```

-	Layers:
	-	`sha256:3c84ecc5e16e1816184f43bbc41f0010df0495baeb95c58e0b47743bbecfb4e7`  
		Last Modified: Wed, 25 Jun 2025 20:07:48 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:7f2567fc8f1b52e8b7fc40fbec2270157a426255e299307c1fdf6291134a4bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69353151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f148d0ade3d87c4d8d77dd87529f575e2008e919bb844a947247561ec03c82db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:234783c583655b5fba47f029b646f86832181f4e7693051a58456c45043c099c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8693516fb4d64dd200448d3da2a32b3deb0e4634e4f4faaa6dc35984a4d873e`

```dockerfile
```

-	Layers:
	-	`sha256:d7b8ebd195f16dbf716810084fd30cbc4943c0d20f94cf8055a15691fd5203ce`  
		Last Modified: Wed, 25 Jun 2025 20:07:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2b4c39548793a279667d4ced40e5e68af421e8ff4000c101ee2f7e5b299573b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70940773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c4520ee754d509808a5e81ed1749fcb77b10dea95542447afafeccebaca66e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:026dc96b447b564878e37a1732f26aa77491519e943779e9f5e336580774335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a66b0aed9a637a80f3fbfb7b609cc336667c89535146dd5bda65fc05777ce3`

```dockerfile
```

-	Layers:
	-	`sha256:c2f530f380386ce5972d923f6ec42373f519edff7acfd63e4e1934eeb86652b4`  
		Last Modified: Wed, 25 Jun 2025 20:07:54 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.0-cli-alpine3.22`

```console
$ docker pull docker@sha256:be316e9f9a158bdd04d175cac7867be4561d9718c8f45331ba09f839854d6ac4
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

### `docker:28.3.0-cli-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:e15d465988c670df7863f019b7bbffadc2fb5a89355183d2f77c9541af6f5f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75386866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c308218afb92593639450e489ef8638050ab55a6c49065a2fbc8a52f70bd7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:95954b4d8cb3ecd9e948ffac374a91f07bfeffef3b0c5c17dd0f6aaa5deab1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf73ac7a434f1e1608f059171e612c92ef03248ba073d582b984939f205e7bb`

```dockerfile
```

-	Layers:
	-	`sha256:659dc4fc8c676ae5ecee4b9f1c73a5096d5d03e6459f28d1554f3f2211f5a592`  
		Last Modified: Wed, 25 Jun 2025 20:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ca185f5711941016ddadcfaa648bdc27c90418f2282d093c6bc751aa3e7ba38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70359081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9ff19e1547d18c4a360fa003b26cb878d2f1ec67647bc6159bfb0320fd306`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:8bd2cad79060bb5785bed3792250043dec874b2660a91b8acff6cbbd7c39bbbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee647cfa7ad7371b150be4ce91c2395bcd50e25ae0986066f39ec2db1307b8ef`

```dockerfile
```

-	Layers:
	-	`sha256:3c84ecc5e16e1816184f43bbc41f0010df0495baeb95c58e0b47743bbecfb4e7`  
		Last Modified: Wed, 25 Jun 2025 20:07:48 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:7f2567fc8f1b52e8b7fc40fbec2270157a426255e299307c1fdf6291134a4bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69353151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f148d0ade3d87c4d8d77dd87529f575e2008e919bb844a947247561ec03c82db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:234783c583655b5fba47f029b646f86832181f4e7693051a58456c45043c099c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8693516fb4d64dd200448d3da2a32b3deb0e4634e4f4faaa6dc35984a4d873e`

```dockerfile
```

-	Layers:
	-	`sha256:d7b8ebd195f16dbf716810084fd30cbc4943c0d20f94cf8055a15691fd5203ce`  
		Last Modified: Wed, 25 Jun 2025 20:07:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2b4c39548793a279667d4ced40e5e68af421e8ff4000c101ee2f7e5b299573b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70940773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c4520ee754d509808a5e81ed1749fcb77b10dea95542447afafeccebaca66e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:026dc96b447b564878e37a1732f26aa77491519e943779e9f5e336580774335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a66b0aed9a637a80f3fbfb7b609cc336667c89535146dd5bda65fc05777ce3`

```dockerfile
```

-	Layers:
	-	`sha256:c2f530f380386ce5972d923f6ec42373f519edff7acfd63e4e1934eeb86652b4`  
		Last Modified: Wed, 25 Jun 2025 20:07:54 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.0-dind`

```console
$ docker pull docker@sha256:d33eb93fe02683e984e6f8a93c0b3d85bb74f56ec83922bc39fb34ba23ab42bc
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

### `docker:28.3.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:bd5712b912e233b9cbca5ed94664dda05655537f56323d55f5435be0df084f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144906835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6892cb0e669d8bf6d40d1421bfd62b0aec81041706f7b45de7a03514cfef527b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6d82b2f6555dd414407f11111af5c2028f1205e50140594c33edfdaf9add7fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281f5c43f6b438ece0586157f96cec3dbde12c3e55fb80b93dcb5e08c92bc9c0`

```dockerfile
```

-	Layers:
	-	`sha256:f99b7342f71018419b6d22e5f772de11b7f1619ac5707ad3f2610ac9f834684c`  
		Last Modified: Wed, 25 Jun 2025 20:07:28 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:0e7bd5b322a7adee7f87d5da6133602a1b13943207c1c119e3fa8bc150662de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135881655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e5f0a26fdef7325b82b98ac05955a1e1ab6990eee865f5d40b5eb1c2b380f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ff3c42dfe8b909933270cb290d5b16dad7c39ef1c61d930695bccb4af028b`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 7.2 MB (7230273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf5f2cd81da4f9935d1b8f1e0c69e9690065ce54192c47285c02007b855ab71`  
		Last Modified: Wed, 25 Jun 2025 19:09:57 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9315c92c22796071003a7353007bcfafc2dde73136adc0ee6c1f859c9ead82`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eabbd9d791bab2458faac47bddb10b59b825dc9b8a6e958d893dad0d62d2b13`  
		Last Modified: Wed, 25 Jun 2025 19:10:07 GMT  
		Size: 58.2 MB (58196245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2fa52243ccad08598f463d20022392c4e63de6a7fa3389a2d3f13bc5072850`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18747036c5bfd27297ec304b7871a2c0a0cab99bc9cac7dcd22593dc95f704d0`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:999ce16d0b42a6156eae74e0a48680ba57dfefa8409ec8cb3140e4abfa0b8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1afb05bba7f7a8f5e78c1e59548ece1fd7da038bb3addbbb866344b023c03`

```dockerfile
```

-	Layers:
	-	`sha256:9849cf691a13b263da46b7691c04aa707880fde9055dd21ca78616d50691794a`  
		Last Modified: Wed, 25 Jun 2025 20:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4c6ec3de04e99f6aba4a50701988210b9d0bfbcee4f4715aba2b6f968145ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134179998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e5f59ba3ffbbe22e927ebf4f2cfd1f28d553a63e5803230880f12c7bb9137d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a13ff228646fe31640f66680c77b8179b59cf030776d4dc27e0b8a4073a1161`  
		Last Modified: Wed, 25 Jun 2025 19:09:40 GMT  
		Size: 6.5 MB (6538132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e439188892f1f8a228ea037911e2843fc2f69b92e2847007cf69bfb07cae8e9`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 86.5 KB (86492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82b72c117f21d49e7e8d6934422e959de7f39d5971cb8bf2bc5a612c6f321b6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5741868cb033a7c74a817afc1bbfc0b66636546ad2b2819fd90b5b72cd7314`  
		Last Modified: Wed, 25 Jun 2025 19:09:44 GMT  
		Size: 58.2 MB (58196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f745e31047d1161b57e77243e0a39cfb9fc008c772fa16ee7c67ed75c9051b`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbf907fef629de9d464812fadbd09c96845cd8dcf8c4c1acf19dbc216347bc6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5e7ea7e55af96477d6205063362129df645015586d168d3abc5fddf5af1f9756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77876fbab01e5b51149471bea0941cfcebf64d55778d638330e8ec92546e5340`

```dockerfile
```

-	Layers:
	-	`sha256:35d28f9246501c698aa882110ff7cb8d3d1ee99e8454a3b8fac5fa6665d20ca9`  
		Last Modified: Wed, 25 Jun 2025 20:07:35 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:852d19966630687c3ad157b217ace73e93c823aaf34c396f4aaef675bee52a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135648800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b957e61342f7dd8223305f18ccc713082c3ef5c69722449cb8b8fdbeb8319012`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a2c73991ca6ca907adb176cce487de5342c67b9d610999b2711012d6dae3fd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070a2badedc718d9b3896e9dcd97389153b5d537dcaaaf577fe0560b77eb6e2`

```dockerfile
```

-	Layers:
	-	`sha256:364f514ac25163eb6400a49f2a109178e8f6779987fe82a10b5bb1acbf9282bc`  
		Last Modified: Thu, 26 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.0-dind-alpine3.22`

```console
$ docker pull docker@sha256:d33eb93fe02683e984e6f8a93c0b3d85bb74f56ec83922bc39fb34ba23ab42bc
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

### `docker:28.3.0-dind-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:bd5712b912e233b9cbca5ed94664dda05655537f56323d55f5435be0df084f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144906835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6892cb0e669d8bf6d40d1421bfd62b0aec81041706f7b45de7a03514cfef527b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6d82b2f6555dd414407f11111af5c2028f1205e50140594c33edfdaf9add7fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281f5c43f6b438ece0586157f96cec3dbde12c3e55fb80b93dcb5e08c92bc9c0`

```dockerfile
```

-	Layers:
	-	`sha256:f99b7342f71018419b6d22e5f772de11b7f1619ac5707ad3f2610ac9f834684c`  
		Last Modified: Wed, 25 Jun 2025 20:07:28 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-dind-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:0e7bd5b322a7adee7f87d5da6133602a1b13943207c1c119e3fa8bc150662de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135881655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e5f0a26fdef7325b82b98ac05955a1e1ab6990eee865f5d40b5eb1c2b380f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ff3c42dfe8b909933270cb290d5b16dad7c39ef1c61d930695bccb4af028b`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 7.2 MB (7230273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf5f2cd81da4f9935d1b8f1e0c69e9690065ce54192c47285c02007b855ab71`  
		Last Modified: Wed, 25 Jun 2025 19:09:57 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9315c92c22796071003a7353007bcfafc2dde73136adc0ee6c1f859c9ead82`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eabbd9d791bab2458faac47bddb10b59b825dc9b8a6e958d893dad0d62d2b13`  
		Last Modified: Wed, 25 Jun 2025 19:10:07 GMT  
		Size: 58.2 MB (58196245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2fa52243ccad08598f463d20022392c4e63de6a7fa3389a2d3f13bc5072850`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18747036c5bfd27297ec304b7871a2c0a0cab99bc9cac7dcd22593dc95f704d0`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:999ce16d0b42a6156eae74e0a48680ba57dfefa8409ec8cb3140e4abfa0b8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1afb05bba7f7a8f5e78c1e59548ece1fd7da038bb3addbbb866344b023c03`

```dockerfile
```

-	Layers:
	-	`sha256:9849cf691a13b263da46b7691c04aa707880fde9055dd21ca78616d50691794a`  
		Last Modified: Wed, 25 Jun 2025 20:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-dind-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4c6ec3de04e99f6aba4a50701988210b9d0bfbcee4f4715aba2b6f968145ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134179998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e5f59ba3ffbbe22e927ebf4f2cfd1f28d553a63e5803230880f12c7bb9137d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a13ff228646fe31640f66680c77b8179b59cf030776d4dc27e0b8a4073a1161`  
		Last Modified: Wed, 25 Jun 2025 19:09:40 GMT  
		Size: 6.5 MB (6538132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e439188892f1f8a228ea037911e2843fc2f69b92e2847007cf69bfb07cae8e9`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 86.5 KB (86492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82b72c117f21d49e7e8d6934422e959de7f39d5971cb8bf2bc5a612c6f321b6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5741868cb033a7c74a817afc1bbfc0b66636546ad2b2819fd90b5b72cd7314`  
		Last Modified: Wed, 25 Jun 2025 19:09:44 GMT  
		Size: 58.2 MB (58196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f745e31047d1161b57e77243e0a39cfb9fc008c772fa16ee7c67ed75c9051b`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbf907fef629de9d464812fadbd09c96845cd8dcf8c4c1acf19dbc216347bc6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:5e7ea7e55af96477d6205063362129df645015586d168d3abc5fddf5af1f9756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77876fbab01e5b51149471bea0941cfcebf64d55778d638330e8ec92546e5340`

```dockerfile
```

-	Layers:
	-	`sha256:35d28f9246501c698aa882110ff7cb8d3d1ee99e8454a3b8fac5fa6665d20ca9`  
		Last Modified: Wed, 25 Jun 2025 20:07:35 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-dind-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:852d19966630687c3ad157b217ace73e93c823aaf34c396f4aaef675bee52a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135648800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b957e61342f7dd8223305f18ccc713082c3ef5c69722449cb8b8fdbeb8319012`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:a2c73991ca6ca907adb176cce487de5342c67b9d610999b2711012d6dae3fd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070a2badedc718d9b3896e9dcd97389153b5d537dcaaaf577fe0560b77eb6e2`

```dockerfile
```

-	Layers:
	-	`sha256:364f514ac25163eb6400a49f2a109178e8f6779987fe82a10b5bb1acbf9282bc`  
		Last Modified: Thu, 26 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.0-dind-rootless`

```console
$ docker pull docker@sha256:6c2c0d6beb885c9c9741e9227a2c8bb25126b948831afda4a6c4221d6cadbb91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.3.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:7fafee3e6a673e4c95d8b8583e939baa5c4103872c26d5074032bb49e8643b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163487607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f7bdc571bf67b9957bd1f5fe4522ba3f5fd48b35b409599e6c30f10c3ca55f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101bccb38f5fc26e226b3aed7f5d43d304a31e4ae35365d48a66d9fc6b533934`  
		Last Modified: Wed, 25 Jun 2025 18:08:52 GMT  
		Size: 993.3 KB (993273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a974f1a114c34599fb5b4760b77413667489c7048fcc9ac21ce87e5cf6422b`  
		Last Modified: Wed, 25 Jun 2025 18:08:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7696a5f9b7e74a2aa514a55ac7e0cfe971b1141c3c5850830fb8e0689f90135a`  
		Last Modified: Wed, 25 Jun 2025 18:08:52 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95141cff2fd6549c5acae115725c4e519b8c7db11a411d0e9ad82b50c9b34933`  
		Last Modified: Wed, 25 Jun 2025 18:08:55 GMT  
		Size: 17.6 MB (17586160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e85fa937ebf06addcb8d1bbdba91a1e0e33297fe50a8ccf5498a3bc159cba6c`  
		Last Modified: Wed, 25 Jun 2025 18:08:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:68f5dd9b1a738661c4c28156a3a6991ffc58978ee0c97f94ce54420b8f0ba20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f9119e3abb10c3af2fe52c9872f6b58f7a68f9014b033b3e011746f9e262f9`

```dockerfile
```

-	Layers:
	-	`sha256:5d2c99dd36e26bd782604aa9a1d14e2cefa0620ba8ace2d9e4259bad786846ba`  
		Last Modified: Wed, 25 Jun 2025 20:07:49 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a6bdd6495f432d9e77784f68f76efbbb3c1876f32f241af8ec504eb422370bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154690467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367b736522af6576dc89a15b7ee3c18b96c615d7e19acbcc7337fcc9e369d27c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5b66d211d051c20b2b8fa072c573c801a3adfd1d5f78c9d8d98055034dc9e7`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 1.0 MB (1022998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c908d2ebbfc7e6af38b4d76f325a249fa359e7f524e0316bbac900fa8f5537d9`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e3f97ea27b30130cf4a126e578dc57f0c0083a14c56fd56f3f1c6b6fa5ac8c`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287bf6b6e7ca52eb877ac8a25ac379d4dee7dfe8d860e93321e2bea6e071b8bb`  
		Last Modified: Thu, 26 Jun 2025 03:49:23 GMT  
		Size: 18.0 MB (18017325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2657fca26a04fb60ad2dd915fd0c4265b8be7854c9d68e19e05ec4372bbaa4d9`  
		Last Modified: Thu, 26 Jun 2025 03:49:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:88444b092967d974c32eb7853e9c4b5224d33ba1f1c8d0d57229afa39d1e4a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e4e22e9b75ecb5b98766fb00c00d442bf16258821538c09572ea9c4121594`

```dockerfile
```

-	Layers:
	-	`sha256:8cf7d1bd28dd5d695964242d21c1d714fc4616311036c7fbf166b8c83e3d1403`  
		Last Modified: Thu, 26 Jun 2025 05:07:29 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.0-windowsservercore`

```console
$ docker pull docker@sha256:961151cbda8766cc99af45924dff0bbbe5c1cd4495373a695cf1dde042adf75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:28.3.0-windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:4079ca5c6c04c424df4cd0952427103783d7f1d5ee13cf250feb9fa7daf702d3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542396755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd1d4f1571e67132e18d27de3ca1ad05ccf64dc10867dd91a34a3164f66a1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Wed, 25 Jun 2025 18:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 18:00:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 18:00:26 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 18:00:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 18:00:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:39 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 18:00:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 18:00:41 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 18:00:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 18:00:52 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 18:01:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b8ee3e9b4b19ac3cb8209b1fec6595c5c0f0fcabc7a9896a46d0ce1f8120bc`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c2dfd0eecb72a14ba95e5ea944ae4941085237952c6b1093966c4f7bfd81c0`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 413.4 KB (413433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732b2abe01a3c431782a440319afcda808697dceebe6fb33b0927e4755690a9`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c642d396a1d409b25ffd02b82f1d9dc6fa3292f21f7f5a51fa7d42f04c025931`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24e676af11cfd3f615a01c8fdecccf9838fe1ce9428ca1291b1492c3f652244`  
		Last Modified: Wed, 25 Jun 2025 18:04:48 GMT  
		Size: 20.9 MB (20871278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0ce9a47ab92c7c251fc9a4f319bc0a5c505107b9e40d0620cf8f928d0e8770`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5008628017fda828a9b90038aa68ea54ee822ac314c8cb4a176de73899dffe3`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72c88a732462f04bc82cda46e0d5bd6db2cb303a9902366d52b6cd1356c1358`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8648b2be10b75a285f1ad75edba61a2bdab08d39267a0998cf77a02d533c7b70`  
		Last Modified: Wed, 25 Jun 2025 18:04:49 GMT  
		Size: 22.7 MB (22693786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83073c0d9f0f34eb666f0222d2f49f718651544b64e4abe583410895710320a1`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35317ffe0ab3851bf4d623b78b15c97eb3e6af22fba759fd4c70636f41b4732`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4637463d4ffc77ae1c82079a154b8ec12faafaeffe0913a0d09deaf28bb49f7`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac7f531a859530f45f62257febda686a917ec0c545cd18a333d7fe3c0263e1`  
		Last Modified: Wed, 25 Jun 2025 18:04:50 GMT  
		Size: 22.2 MB (22232346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.3.0-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:70e34fc394cc0bbe07afb7936e0a6d10abae07e6343f2adfaf13cba9c0f6be17
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346284808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5b2835fcc7572b7508a52e3098bb05924a789e59baff2cf579969608ce543d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Wed, 25 Jun 2025 17:54:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 17:55:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 17:55:41 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 17:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 17:56:02 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 17:56:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 17:56:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fe415a5d4c4e0bf9f51cfbfd6c53baf78ef30a68f632d510e3173d228ec7e`  
		Last Modified: Wed, 25 Jun 2025 17:56:55 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d732acd5b34fa2dc704a91dde188904e8c977774edfa16f0bfa032200a611831`  
		Last Modified: Wed, 25 Jun 2025 17:56:56 GMT  
		Size: 356.3 KB (356325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb31ba7c382ae188ddfcd0df5bae106d2b1a66e54a578343ffd763ec23ee02c`  
		Last Modified: Wed, 25 Jun 2025 17:56:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacd2505104dc3c0daf2469a31a539880b7e41ee2017eb7b75bd204861800b6e`  
		Last Modified: Wed, 25 Jun 2025 17:56:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76a7d1495c30218a8b02c22b8199ee65ddc9041e1b67ecc868be2b5be8cde68`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 20.8 MB (20827807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ea181f6649206ff19d0147312fda9397ff0be604a29b9a2d5a129111b08fca`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ae454c928c4496c0f562fe3503157fa0d1a06b286d8a04c62641dc1fe604b0`  
		Last Modified: Wed, 25 Jun 2025 17:57:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ee2c6ab911fbbfd12f7eece75e8cd2107544bce17bf4054c509f5172a609c1`  
		Last Modified: Wed, 25 Jun 2025 17:57:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d3fa685524bda12581d5b1c38ad03460b11147adb582f2eb25ba0d40c97d4b`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 22.7 MB (22652434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d02f084c1719a8edce4ef03af5f09ec922f79f2214d443b99ed84aac6fd43`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421d689fa4721f56c6cdbb292a97e67b100810930f43c25e1216000154a1e57a`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ba7fc52773bf998c43237d460a09c65e59e6d4a1bb2e2d58e75cc23013d43`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112a0a68c74b56bf752081ce36f98ad96808d67fd81c0ab24f1744b08db9d9`  
		Last Modified: Wed, 25 Jun 2025 17:57:12 GMT  
		Size: 22.2 MB (22185055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3a63fe3d9ab8c76984d372685bf69740f4dc4b9f8b136c8144528d2a626e08a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:28.3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:70e34fc394cc0bbe07afb7936e0a6d10abae07e6343f2adfaf13cba9c0f6be17
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346284808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5b2835fcc7572b7508a52e3098bb05924a789e59baff2cf579969608ce543d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Wed, 25 Jun 2025 17:54:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 17:55:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 17:55:41 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 17:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 17:56:02 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 17:56:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 17:56:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fe415a5d4c4e0bf9f51cfbfd6c53baf78ef30a68f632d510e3173d228ec7e`  
		Last Modified: Wed, 25 Jun 2025 17:56:55 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d732acd5b34fa2dc704a91dde188904e8c977774edfa16f0bfa032200a611831`  
		Last Modified: Wed, 25 Jun 2025 17:56:56 GMT  
		Size: 356.3 KB (356325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb31ba7c382ae188ddfcd0df5bae106d2b1a66e54a578343ffd763ec23ee02c`  
		Last Modified: Wed, 25 Jun 2025 17:56:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacd2505104dc3c0daf2469a31a539880b7e41ee2017eb7b75bd204861800b6e`  
		Last Modified: Wed, 25 Jun 2025 17:56:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76a7d1495c30218a8b02c22b8199ee65ddc9041e1b67ecc868be2b5be8cde68`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 20.8 MB (20827807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ea181f6649206ff19d0147312fda9397ff0be604a29b9a2d5a129111b08fca`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ae454c928c4496c0f562fe3503157fa0d1a06b286d8a04c62641dc1fe604b0`  
		Last Modified: Wed, 25 Jun 2025 17:57:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ee2c6ab911fbbfd12f7eece75e8cd2107544bce17bf4054c509f5172a609c1`  
		Last Modified: Wed, 25 Jun 2025 17:57:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d3fa685524bda12581d5b1c38ad03460b11147adb582f2eb25ba0d40c97d4b`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 22.7 MB (22652434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d02f084c1719a8edce4ef03af5f09ec922f79f2214d443b99ed84aac6fd43`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421d689fa4721f56c6cdbb292a97e67b100810930f43c25e1216000154a1e57a`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ba7fc52773bf998c43237d460a09c65e59e6d4a1bb2e2d58e75cc23013d43`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112a0a68c74b56bf752081ce36f98ad96808d67fd81c0ab24f1744b08db9d9`  
		Last Modified: Wed, 25 Jun 2025 17:57:12 GMT  
		Size: 22.2 MB (22185055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:3e78e4b3bbd7a8b9663fa3b09411da2139569cccfb6c179bb80cfa3c8b27a535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:28.3.0-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:4079ca5c6c04c424df4cd0952427103783d7f1d5ee13cf250feb9fa7daf702d3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542396755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd1d4f1571e67132e18d27de3ca1ad05ccf64dc10867dd91a34a3164f66a1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Wed, 25 Jun 2025 18:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 18:00:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 18:00:26 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 18:00:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 18:00:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:39 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 18:00:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 18:00:41 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 18:00:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 18:00:52 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 18:01:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b8ee3e9b4b19ac3cb8209b1fec6595c5c0f0fcabc7a9896a46d0ce1f8120bc`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c2dfd0eecb72a14ba95e5ea944ae4941085237952c6b1093966c4f7bfd81c0`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 413.4 KB (413433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732b2abe01a3c431782a440319afcda808697dceebe6fb33b0927e4755690a9`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c642d396a1d409b25ffd02b82f1d9dc6fa3292f21f7f5a51fa7d42f04c025931`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24e676af11cfd3f615a01c8fdecccf9838fe1ce9428ca1291b1492c3f652244`  
		Last Modified: Wed, 25 Jun 2025 18:04:48 GMT  
		Size: 20.9 MB (20871278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0ce9a47ab92c7c251fc9a4f319bc0a5c505107b9e40d0620cf8f928d0e8770`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5008628017fda828a9b90038aa68ea54ee822ac314c8cb4a176de73899dffe3`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72c88a732462f04bc82cda46e0d5bd6db2cb303a9902366d52b6cd1356c1358`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8648b2be10b75a285f1ad75edba61a2bdab08d39267a0998cf77a02d533c7b70`  
		Last Modified: Wed, 25 Jun 2025 18:04:49 GMT  
		Size: 22.7 MB (22693786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83073c0d9f0f34eb666f0222d2f49f718651544b64e4abe583410895710320a1`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35317ffe0ab3851bf4d623b78b15c97eb3e6af22fba759fd4c70636f41b4732`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4637463d4ffc77ae1c82079a154b8ec12faafaeffe0913a0d09deaf28bb49f7`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac7f531a859530f45f62257febda686a917ec0c545cd18a333d7fe3c0263e1`  
		Last Modified: Wed, 25 Jun 2025 18:04:50 GMT  
		Size: 22.2 MB (22232346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:be316e9f9a158bdd04d175cac7867be4561d9718c8f45331ba09f839854d6ac4
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
$ docker pull docker@sha256:e15d465988c670df7863f019b7bbffadc2fb5a89355183d2f77c9541af6f5f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75386866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c308218afb92593639450e489ef8638050ab55a6c49065a2fbc8a52f70bd7a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:95954b4d8cb3ecd9e948ffac374a91f07bfeffef3b0c5c17dd0f6aaa5deab1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf73ac7a434f1e1608f059171e612c92ef03248ba073d582b984939f205e7bb`

```dockerfile
```

-	Layers:
	-	`sha256:659dc4fc8c676ae5ecee4b9f1c73a5096d5d03e6459f28d1554f3f2211f5a592`  
		Last Modified: Wed, 25 Jun 2025 20:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:6ca185f5711941016ddadcfaa648bdc27c90418f2282d093c6bc751aa3e7ba38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70359081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9ff19e1547d18c4a360fa003b26cb878d2f1ec67647bc6159bfb0320fd306`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:8bd2cad79060bb5785bed3792250043dec874b2660a91b8acff6cbbd7c39bbbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee647cfa7ad7371b150be4ce91c2395bcd50e25ae0986066f39ec2db1307b8ef`

```dockerfile
```

-	Layers:
	-	`sha256:3c84ecc5e16e1816184f43bbc41f0010df0495baeb95c58e0b47743bbecfb4e7`  
		Last Modified: Wed, 25 Jun 2025 20:07:48 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:7f2567fc8f1b52e8b7fc40fbec2270157a426255e299307c1fdf6291134a4bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69353151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f148d0ade3d87c4d8d77dd87529f575e2008e919bb844a947247561ec03c82db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:234783c583655b5fba47f029b646f86832181f4e7693051a58456c45043c099c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8693516fb4d64dd200448d3da2a32b3deb0e4634e4f4faaa6dc35984a4d873e`

```dockerfile
```

-	Layers:
	-	`sha256:d7b8ebd195f16dbf716810084fd30cbc4943c0d20f94cf8055a15691fd5203ce`  
		Last Modified: Wed, 25 Jun 2025 20:07:50 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2b4c39548793a279667d4ced40e5e68af421e8ff4000c101ee2f7e5b299573b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70940773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c4520ee754d509808a5e81ed1749fcb77b10dea95542447afafeccebaca66e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:026dc96b447b564878e37a1732f26aa77491519e943779e9f5e336580774335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a66b0aed9a637a80f3fbfb7b609cc336667c89535146dd5bda65fc05777ce3`

```dockerfile
```

-	Layers:
	-	`sha256:c2f530f380386ce5972d923f6ec42373f519edff7acfd63e4e1934eeb86652b4`  
		Last Modified: Wed, 25 Jun 2025 20:07:54 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:d33eb93fe02683e984e6f8a93c0b3d85bb74f56ec83922bc39fb34ba23ab42bc
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
$ docker pull docker@sha256:bd5712b912e233b9cbca5ed94664dda05655537f56323d55f5435be0df084f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144906835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6892cb0e669d8bf6d40d1421bfd62b0aec81041706f7b45de7a03514cfef527b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:6d82b2f6555dd414407f11111af5c2028f1205e50140594c33edfdaf9add7fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281f5c43f6b438ece0586157f96cec3dbde12c3e55fb80b93dcb5e08c92bc9c0`

```dockerfile
```

-	Layers:
	-	`sha256:f99b7342f71018419b6d22e5f772de11b7f1619ac5707ad3f2610ac9f834684c`  
		Last Modified: Wed, 25 Jun 2025 20:07:28 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:0e7bd5b322a7adee7f87d5da6133602a1b13943207c1c119e3fa8bc150662de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135881655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e5f0a26fdef7325b82b98ac05955a1e1ab6990eee865f5d40b5eb1c2b380f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ff3c42dfe8b909933270cb290d5b16dad7c39ef1c61d930695bccb4af028b`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 7.2 MB (7230273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf5f2cd81da4f9935d1b8f1e0c69e9690065ce54192c47285c02007b855ab71`  
		Last Modified: Wed, 25 Jun 2025 19:09:57 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9315c92c22796071003a7353007bcfafc2dde73136adc0ee6c1f859c9ead82`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eabbd9d791bab2458faac47bddb10b59b825dc9b8a6e958d893dad0d62d2b13`  
		Last Modified: Wed, 25 Jun 2025 19:10:07 GMT  
		Size: 58.2 MB (58196245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2fa52243ccad08598f463d20022392c4e63de6a7fa3389a2d3f13bc5072850`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18747036c5bfd27297ec304b7871a2c0a0cab99bc9cac7dcd22593dc95f704d0`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:999ce16d0b42a6156eae74e0a48680ba57dfefa8409ec8cb3140e4abfa0b8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1afb05bba7f7a8f5e78c1e59548ece1fd7da038bb3addbbb866344b023c03`

```dockerfile
```

-	Layers:
	-	`sha256:9849cf691a13b263da46b7691c04aa707880fde9055dd21ca78616d50691794a`  
		Last Modified: Wed, 25 Jun 2025 20:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4c6ec3de04e99f6aba4a50701988210b9d0bfbcee4f4715aba2b6f968145ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134179998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e5f59ba3ffbbe22e927ebf4f2cfd1f28d553a63e5803230880f12c7bb9137d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a13ff228646fe31640f66680c77b8179b59cf030776d4dc27e0b8a4073a1161`  
		Last Modified: Wed, 25 Jun 2025 19:09:40 GMT  
		Size: 6.5 MB (6538132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e439188892f1f8a228ea037911e2843fc2f69b92e2847007cf69bfb07cae8e9`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 86.5 KB (86492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82b72c117f21d49e7e8d6934422e959de7f39d5971cb8bf2bc5a612c6f321b6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5741868cb033a7c74a817afc1bbfc0b66636546ad2b2819fd90b5b72cd7314`  
		Last Modified: Wed, 25 Jun 2025 19:09:44 GMT  
		Size: 58.2 MB (58196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f745e31047d1161b57e77243e0a39cfb9fc008c772fa16ee7c67ed75c9051b`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbf907fef629de9d464812fadbd09c96845cd8dcf8c4c1acf19dbc216347bc6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:5e7ea7e55af96477d6205063362129df645015586d168d3abc5fddf5af1f9756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77876fbab01e5b51149471bea0941cfcebf64d55778d638330e8ec92546e5340`

```dockerfile
```

-	Layers:
	-	`sha256:35d28f9246501c698aa882110ff7cb8d3d1ee99e8454a3b8fac5fa6665d20ca9`  
		Last Modified: Wed, 25 Jun 2025 20:07:35 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:852d19966630687c3ad157b217ace73e93c823aaf34c396f4aaef675bee52a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135648800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b957e61342f7dd8223305f18ccc713082c3ef5c69722449cb8b8fdbeb8319012`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a2c73991ca6ca907adb176cce487de5342c67b9d610999b2711012d6dae3fd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070a2badedc718d9b3896e9dcd97389153b5d537dcaaaf577fe0560b77eb6e2`

```dockerfile
```

-	Layers:
	-	`sha256:364f514ac25163eb6400a49f2a109178e8f6779987fe82a10b5bb1acbf9282bc`  
		Last Modified: Thu, 26 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:6c2c0d6beb885c9c9741e9227a2c8bb25126b948831afda4a6c4221d6cadbb91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:7fafee3e6a673e4c95d8b8583e939baa5c4103872c26d5074032bb49e8643b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163487607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f7bdc571bf67b9957bd1f5fe4522ba3f5fd48b35b409599e6c30f10c3ca55f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101bccb38f5fc26e226b3aed7f5d43d304a31e4ae35365d48a66d9fc6b533934`  
		Last Modified: Wed, 25 Jun 2025 18:08:52 GMT  
		Size: 993.3 KB (993273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a974f1a114c34599fb5b4760b77413667489c7048fcc9ac21ce87e5cf6422b`  
		Last Modified: Wed, 25 Jun 2025 18:08:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7696a5f9b7e74a2aa514a55ac7e0cfe971b1141c3c5850830fb8e0689f90135a`  
		Last Modified: Wed, 25 Jun 2025 18:08:52 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95141cff2fd6549c5acae115725c4e519b8c7db11a411d0e9ad82b50c9b34933`  
		Last Modified: Wed, 25 Jun 2025 18:08:55 GMT  
		Size: 17.6 MB (17586160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e85fa937ebf06addcb8d1bbdba91a1e0e33297fe50a8ccf5498a3bc159cba6c`  
		Last Modified: Wed, 25 Jun 2025 18:08:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:68f5dd9b1a738661c4c28156a3a6991ffc58978ee0c97f94ce54420b8f0ba20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f9119e3abb10c3af2fe52c9872f6b58f7a68f9014b033b3e011746f9e262f9`

```dockerfile
```

-	Layers:
	-	`sha256:5d2c99dd36e26bd782604aa9a1d14e2cefa0620ba8ace2d9e4259bad786846ba`  
		Last Modified: Wed, 25 Jun 2025 20:07:49 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a6bdd6495f432d9e77784f68f76efbbb3c1876f32f241af8ec504eb422370bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154690467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367b736522af6576dc89a15b7ee3c18b96c615d7e19acbcc7337fcc9e369d27c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5b66d211d051c20b2b8fa072c573c801a3adfd1d5f78c9d8d98055034dc9e7`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 1.0 MB (1022998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c908d2ebbfc7e6af38b4d76f325a249fa359e7f524e0316bbac900fa8f5537d9`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e3f97ea27b30130cf4a126e578dc57f0c0083a14c56fd56f3f1c6b6fa5ac8c`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287bf6b6e7ca52eb877ac8a25ac379d4dee7dfe8d860e93321e2bea6e071b8bb`  
		Last Modified: Thu, 26 Jun 2025 03:49:23 GMT  
		Size: 18.0 MB (18017325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2657fca26a04fb60ad2dd915fd0c4265b8be7854c9d68e19e05ec4372bbaa4d9`  
		Last Modified: Thu, 26 Jun 2025 03:49:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:88444b092967d974c32eb7853e9c4b5224d33ba1f1c8d0d57229afa39d1e4a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e4e22e9b75ecb5b98766fb00c00d442bf16258821538c09572ea9c4121594`

```dockerfile
```

-	Layers:
	-	`sha256:8cf7d1bd28dd5d695964242d21c1d714fc4616311036c7fbf166b8c83e3d1403`  
		Last Modified: Thu, 26 Jun 2025 05:07:29 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:d33eb93fe02683e984e6f8a93c0b3d85bb74f56ec83922bc39fb34ba23ab42bc
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
$ docker pull docker@sha256:bd5712b912e233b9cbca5ed94664dda05655537f56323d55f5435be0df084f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144906835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6892cb0e669d8bf6d40d1421bfd62b0aec81041706f7b45de7a03514cfef527b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289210598593d44930f05bb3271d4af3b977b3a902b21cacbedeb10afffd0f7`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 8.2 MB (8207467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b72e5efab2285f2d7b4bfa6ac91090b98030a1637417d3f8e4f56463caefe`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a85d6ba8bd2bcaf3ca4781d7eb12b7fee88906797900f2a5674093d720c8fe`  
		Last Modified: Wed, 25 Jun 2025 17:59:34 GMT  
		Size: 20.5 MB (20460120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcf9b7e804719836a5804e2c0d047f2ca918f6f79d0827c05f93bb43264e32`  
		Last Modified: Wed, 25 Jun 2025 17:59:35 GMT  
		Size: 21.7 MB (21664162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11c760d55de431737966c9dc224dfa49712a4efb6fcd6f9516d66d1a73a26c`  
		Last Modified: Wed, 25 Jun 2025 17:59:32 GMT  
		Size: 21.3 MB (21256116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c894803c93b892e90c19cc0f08bfdbddea4c24cf3e7861283db4bf04ed804`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a138df0e0829fb1af40fe41153855eef9200ab45b6592d4b25b7bcb31711e1`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e1feda6a75aa73cbdc2334e5c0032cadf43f88503fd79aa221ab063a5caf2`  
		Last Modified: Wed, 25 Jun 2025 17:59:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a3ff144a84ef4653a0ebcedbb4304caa75ed8329fb957583b0c2c1c43bac2`  
		Last Modified: Wed, 25 Jun 2025 18:08:13 GMT  
		Size: 6.9 MB (6905573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a786df52bc31cbdd1cb79723e38b0fcc61560de9d225265218290bf76be0e601`  
		Last Modified: Wed, 25 Jun 2025 18:08:11 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086cd1daa2b29526ea4af857fbf487e957fd5de32467d80136a62129f792859d`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e3d005d0efc0e299584bcc711eab04fdac65f76e5a39a3a227973aac3d9383`  
		Last Modified: Wed, 25 Jun 2025 18:08:17 GMT  
		Size: 62.5 MB (62517909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba08ed4b94086c2d03ef996e23461afcdd9c7e7d0724b718a6a8f22ff717c7`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f194ce3319b486d360f509a6b1494d04291b8aff4a40d3a74938599566b623f`  
		Last Modified: Wed, 25 Jun 2025 18:08:10 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:6d82b2f6555dd414407f11111af5c2028f1205e50140594c33edfdaf9add7fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281f5c43f6b438ece0586157f96cec3dbde12c3e55fb80b93dcb5e08c92bc9c0`

```dockerfile
```

-	Layers:
	-	`sha256:f99b7342f71018419b6d22e5f772de11b7f1619ac5707ad3f2610ac9f834684c`  
		Last Modified: Wed, 25 Jun 2025 20:07:28 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:0e7bd5b322a7adee7f87d5da6133602a1b13943207c1c119e3fa8bc150662de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135881655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456e5f0a26fdef7325b82b98ac05955a1e1ab6990eee865f5d40b5eb1c2b380f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e53f526b8a259bd0a40a1e4bd0b2260cff84e1e8b971b67710b00aa26bf23`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 18.5 MB (18450874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e045309567bd3067c3cf10a1fb430ad752a41f119321624784597490af9db`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.3 MB (20295398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b708a3832f9e0ddbd7b42af95fac889812a4b22286209b550050324bcc63`  
		Last Modified: Wed, 25 Jun 2025 20:07:46 GMT  
		Size: 20.0 MB (19995055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c8b72a00084a4c5962ef50770618540e41ecbeee4749f78a704b31ba66901`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f52318f36870b722ce91ddfbd0d5dfada3be993acb5cc3c60894378da27f8f`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ba14bd348eb4245e0feab353c1de242bb2bdc5cd62930a7a3904b4f94a583`  
		Last Modified: Wed, 25 Jun 2025 20:07:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ff3c42dfe8b909933270cb290d5b16dad7c39ef1c61d930695bccb4af028b`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 7.2 MB (7230273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf5f2cd81da4f9935d1b8f1e0c69e9690065ce54192c47285c02007b855ab71`  
		Last Modified: Wed, 25 Jun 2025 19:09:57 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9315c92c22796071003a7353007bcfafc2dde73136adc0ee6c1f859c9ead82`  
		Last Modified: Wed, 25 Jun 2025 19:09:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eabbd9d791bab2458faac47bddb10b59b825dc9b8a6e958d893dad0d62d2b13`  
		Last Modified: Wed, 25 Jun 2025 19:10:07 GMT  
		Size: 58.2 MB (58196245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2fa52243ccad08598f463d20022392c4e63de6a7fa3389a2d3f13bc5072850`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18747036c5bfd27297ec304b7871a2c0a0cab99bc9cac7dcd22593dc95f704d0`  
		Last Modified: Wed, 25 Jun 2025 19:10:00 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:999ce16d0b42a6156eae74e0a48680ba57dfefa8409ec8cb3140e4abfa0b8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1afb05bba7f7a8f5e78c1e59548ece1fd7da038bb3addbbb866344b023c03`

```dockerfile
```

-	Layers:
	-	`sha256:9849cf691a13b263da46b7691c04aa707880fde9055dd21ca78616d50691794a`  
		Last Modified: Wed, 25 Jun 2025 20:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:b4c6ec3de04e99f6aba4a50701988210b9d0bfbcee4f4715aba2b6f968145ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134179998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e5f59ba3ffbbe22e927ebf4f2cfd1f28d553a63e5803230880f12c7bb9137d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b30f7212c67694cf480811a55ca551c13acaf23308660855c528140f72c862`  
		Last Modified: Fri, 13 Jun 2025 01:20:06 GMT  
		Size: 7.4 MB (7440617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fca8ac4e435f25c24efea81db3a20417fad9d7c421bee5ce9e3b58996c8efa`  
		Last Modified: Fri, 13 Jun 2025 01:20:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca022e9dc78b805cca3f5307b8b48d5e7bc3577dc8795867858d880e84cf287`  
		Last Modified: Wed, 25 Jun 2025 18:35:28 GMT  
		Size: 18.4 MB (18435311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2ef2c93cf96dedc13985ab7a65631522ff852dc69da5389e294a91e6aeb7d`  
		Last Modified: Wed, 25 Jun 2025 18:35:31 GMT  
		Size: 20.3 MB (20282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480796582f656f4a48beb96201b84b9c8c55d7843ec62a9a55ab20042bc3d38`  
		Last Modified: Wed, 25 Jun 2025 18:35:30 GMT  
		Size: 20.0 MB (19973092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c7ab1f2267755535cca8e61a139251da95b003277c353674c60ee99ecdb7b`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8dad6f576c030f89566cbe3b5227f5a3c42c02c2b1558b56bae8abdae25de5`  
		Last Modified: Wed, 25 Jun 2025 18:35:27 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a062d3b7e9d2ff2c5e0b0f827f191ea6e5be018b66198ee69c59abf139046d`  
		Last Modified: Wed, 25 Jun 2025 18:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a13ff228646fe31640f66680c77b8179b59cf030776d4dc27e0b8a4073a1161`  
		Last Modified: Wed, 25 Jun 2025 19:09:40 GMT  
		Size: 6.5 MB (6538132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e439188892f1f8a228ea037911e2843fc2f69b92e2847007cf69bfb07cae8e9`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 86.5 KB (86492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82b72c117f21d49e7e8d6934422e959de7f39d5971cb8bf2bc5a612c6f321b6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5741868cb033a7c74a817afc1bbfc0b66636546ad2b2819fd90b5b72cd7314`  
		Last Modified: Wed, 25 Jun 2025 19:09:44 GMT  
		Size: 58.2 MB (58196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f745e31047d1161b57e77243e0a39cfb9fc008c772fa16ee7c67ed75c9051b`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbf907fef629de9d464812fadbd09c96845cd8dcf8c4c1acf19dbc216347bc6`  
		Last Modified: Wed, 25 Jun 2025 19:09:39 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:5e7ea7e55af96477d6205063362129df645015586d168d3abc5fddf5af1f9756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77876fbab01e5b51149471bea0941cfcebf64d55778d638330e8ec92546e5340`

```dockerfile
```

-	Layers:
	-	`sha256:35d28f9246501c698aa882110ff7cb8d3d1ee99e8454a3b8fac5fa6665d20ca9`  
		Last Modified: Wed, 25 Jun 2025 20:07:35 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:852d19966630687c3ad157b217ace73e93c823aaf34c396f4aaef675bee52a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135648800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b957e61342f7dd8223305f18ccc713082c3ef5c69722449cb8b8fdbeb8319012`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a2c73991ca6ca907adb176cce487de5342c67b9d610999b2711012d6dae3fd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070a2badedc718d9b3896e9dcd97389153b5d537dcaaaf577fe0560b77eb6e2`

```dockerfile
```

-	Layers:
	-	`sha256:364f514ac25163eb6400a49f2a109178e8f6779987fe82a10b5bb1acbf9282bc`  
		Last Modified: Thu, 26 Jun 2025 02:07:41 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:961151cbda8766cc99af45924dff0bbbe5c1cd4495373a695cf1dde042adf75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:4079ca5c6c04c424df4cd0952427103783d7f1d5ee13cf250feb9fa7daf702d3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542396755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd1d4f1571e67132e18d27de3ca1ad05ccf64dc10867dd91a34a3164f66a1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Wed, 25 Jun 2025 18:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 18:00:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 18:00:26 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 18:00:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 18:00:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:39 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 18:00:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 18:00:41 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 18:00:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 18:00:52 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 18:01:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b8ee3e9b4b19ac3cb8209b1fec6595c5c0f0fcabc7a9896a46d0ce1f8120bc`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c2dfd0eecb72a14ba95e5ea944ae4941085237952c6b1093966c4f7bfd81c0`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 413.4 KB (413433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732b2abe01a3c431782a440319afcda808697dceebe6fb33b0927e4755690a9`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c642d396a1d409b25ffd02b82f1d9dc6fa3292f21f7f5a51fa7d42f04c025931`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24e676af11cfd3f615a01c8fdecccf9838fe1ce9428ca1291b1492c3f652244`  
		Last Modified: Wed, 25 Jun 2025 18:04:48 GMT  
		Size: 20.9 MB (20871278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0ce9a47ab92c7c251fc9a4f319bc0a5c505107b9e40d0620cf8f928d0e8770`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5008628017fda828a9b90038aa68ea54ee822ac314c8cb4a176de73899dffe3`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72c88a732462f04bc82cda46e0d5bd6db2cb303a9902366d52b6cd1356c1358`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8648b2be10b75a285f1ad75edba61a2bdab08d39267a0998cf77a02d533c7b70`  
		Last Modified: Wed, 25 Jun 2025 18:04:49 GMT  
		Size: 22.7 MB (22693786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83073c0d9f0f34eb666f0222d2f49f718651544b64e4abe583410895710320a1`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35317ffe0ab3851bf4d623b78b15c97eb3e6af22fba759fd4c70636f41b4732`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4637463d4ffc77ae1c82079a154b8ec12faafaeffe0913a0d09deaf28bb49f7`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac7f531a859530f45f62257febda686a917ec0c545cd18a333d7fe3c0263e1`  
		Last Modified: Wed, 25 Jun 2025 18:04:50 GMT  
		Size: 22.2 MB (22232346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:70e34fc394cc0bbe07afb7936e0a6d10abae07e6343f2adfaf13cba9c0f6be17
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346284808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5b2835fcc7572b7508a52e3098bb05924a789e59baff2cf579969608ce543d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Wed, 25 Jun 2025 17:54:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 17:55:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 17:55:41 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 17:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 17:56:02 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 17:56:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 17:56:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fe415a5d4c4e0bf9f51cfbfd6c53baf78ef30a68f632d510e3173d228ec7e`  
		Last Modified: Wed, 25 Jun 2025 17:56:55 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d732acd5b34fa2dc704a91dde188904e8c977774edfa16f0bfa032200a611831`  
		Last Modified: Wed, 25 Jun 2025 17:56:56 GMT  
		Size: 356.3 KB (356325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb31ba7c382ae188ddfcd0df5bae106d2b1a66e54a578343ffd763ec23ee02c`  
		Last Modified: Wed, 25 Jun 2025 17:56:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacd2505104dc3c0daf2469a31a539880b7e41ee2017eb7b75bd204861800b6e`  
		Last Modified: Wed, 25 Jun 2025 17:56:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76a7d1495c30218a8b02c22b8199ee65ddc9041e1b67ecc868be2b5be8cde68`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 20.8 MB (20827807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ea181f6649206ff19d0147312fda9397ff0be604a29b9a2d5a129111b08fca`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ae454c928c4496c0f562fe3503157fa0d1a06b286d8a04c62641dc1fe604b0`  
		Last Modified: Wed, 25 Jun 2025 17:57:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ee2c6ab911fbbfd12f7eece75e8cd2107544bce17bf4054c509f5172a609c1`  
		Last Modified: Wed, 25 Jun 2025 17:57:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d3fa685524bda12581d5b1c38ad03460b11147adb582f2eb25ba0d40c97d4b`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 22.7 MB (22652434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d02f084c1719a8edce4ef03af5f09ec922f79f2214d443b99ed84aac6fd43`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421d689fa4721f56c6cdbb292a97e67b100810930f43c25e1216000154a1e57a`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ba7fc52773bf998c43237d460a09c65e59e6d4a1bb2e2d58e75cc23013d43`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112a0a68c74b56bf752081ce36f98ad96808d67fd81c0ab24f1744b08db9d9`  
		Last Modified: Wed, 25 Jun 2025 17:57:12 GMT  
		Size: 22.2 MB (22185055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:3a63fe3d9ab8c76984d372685bf69740f4dc4b9f8b136c8144528d2a626e08a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull docker@sha256:70e34fc394cc0bbe07afb7936e0a6d10abae07e6343f2adfaf13cba9c0f6be17
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346284808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5b2835fcc7572b7508a52e3098bb05924a789e59baff2cf579969608ce543d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Wed, 25 Jun 2025 17:54:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 17:55:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 17:55:41 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 17:56:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 17:56:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 17:56:02 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 17:56:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 17:56:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 17:56:12 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 17:56:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fe415a5d4c4e0bf9f51cfbfd6c53baf78ef30a68f632d510e3173d228ec7e`  
		Last Modified: Wed, 25 Jun 2025 17:56:55 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d732acd5b34fa2dc704a91dde188904e8c977774edfa16f0bfa032200a611831`  
		Last Modified: Wed, 25 Jun 2025 17:56:56 GMT  
		Size: 356.3 KB (356325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb31ba7c382ae188ddfcd0df5bae106d2b1a66e54a578343ffd763ec23ee02c`  
		Last Modified: Wed, 25 Jun 2025 17:56:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacd2505104dc3c0daf2469a31a539880b7e41ee2017eb7b75bd204861800b6e`  
		Last Modified: Wed, 25 Jun 2025 17:56:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76a7d1495c30218a8b02c22b8199ee65ddc9041e1b67ecc868be2b5be8cde68`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 20.8 MB (20827807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ea181f6649206ff19d0147312fda9397ff0be604a29b9a2d5a129111b08fca`  
		Last Modified: Wed, 25 Jun 2025 17:57:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ae454c928c4496c0f562fe3503157fa0d1a06b286d8a04c62641dc1fe604b0`  
		Last Modified: Wed, 25 Jun 2025 17:57:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ee2c6ab911fbbfd12f7eece75e8cd2107544bce17bf4054c509f5172a609c1`  
		Last Modified: Wed, 25 Jun 2025 17:57:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d3fa685524bda12581d5b1c38ad03460b11147adb582f2eb25ba0d40c97d4b`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 22.7 MB (22652434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d02f084c1719a8edce4ef03af5f09ec922f79f2214d443b99ed84aac6fd43`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421d689fa4721f56c6cdbb292a97e67b100810930f43c25e1216000154a1e57a`  
		Last Modified: Wed, 25 Jun 2025 17:57:07 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ba7fc52773bf998c43237d460a09c65e59e6d4a1bb2e2d58e75cc23013d43`  
		Last Modified: Wed, 25 Jun 2025 17:57:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112a0a68c74b56bf752081ce36f98ad96808d67fd81c0ab24f1744b08db9d9`  
		Last Modified: Wed, 25 Jun 2025 17:57:12 GMT  
		Size: 22.2 MB (22185055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:3e78e4b3bbd7a8b9663fa3b09411da2139569cccfb6c179bb80cfa3c8b27a535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull docker@sha256:4079ca5c6c04c424df4cd0952427103783d7f1d5ee13cf250feb9fa7daf702d3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3542396755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd1d4f1571e67132e18d27de3ca1ad05ccf64dc10867dd91a34a3164f66a1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Wed, 25 Jun 2025 18:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Jun 2025 18:00:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Jun 2025 18:00:26 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 18:00:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.0.zip
# Wed, 25 Jun 2025 18:00:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:39 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 18:00:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Wed, 25 Jun 2025 18:00:41 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Wed, 25 Jun 2025 18:00:50 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 18:00:51 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-windows-x86_64.exe
# Wed, 25 Jun 2025 18:00:52 GMT
ENV DOCKER_COMPOSE_SHA256=771fee0bad6dadde4ea68d99ec9aefaffcab2574ad70e64b54560e4e139eb804
# Wed, 25 Jun 2025 18:01:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b8ee3e9b4b19ac3cb8209b1fec6595c5c0f0fcabc7a9896a46d0ce1f8120bc`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c2dfd0eecb72a14ba95e5ea944ae4941085237952c6b1093966c4f7bfd81c0`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 413.4 KB (413433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732b2abe01a3c431782a440319afcda808697dceebe6fb33b0927e4755690a9`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c642d396a1d409b25ffd02b82f1d9dc6fa3292f21f7f5a51fa7d42f04c025931`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24e676af11cfd3f615a01c8fdecccf9838fe1ce9428ca1291b1492c3f652244`  
		Last Modified: Wed, 25 Jun 2025 18:04:48 GMT  
		Size: 20.9 MB (20871278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0ce9a47ab92c7c251fc9a4f319bc0a5c505107b9e40d0620cf8f928d0e8770`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5008628017fda828a9b90038aa68ea54ee822ac314c8cb4a176de73899dffe3`  
		Last Modified: Wed, 25 Jun 2025 18:04:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72c88a732462f04bc82cda46e0d5bd6db2cb303a9902366d52b6cd1356c1358`  
		Last Modified: Wed, 25 Jun 2025 18:04:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8648b2be10b75a285f1ad75edba61a2bdab08d39267a0998cf77a02d533c7b70`  
		Last Modified: Wed, 25 Jun 2025 18:04:49 GMT  
		Size: 22.7 MB (22693786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83073c0d9f0f34eb666f0222d2f49f718651544b64e4abe583410895710320a1`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35317ffe0ab3851bf4d623b78b15c97eb3e6af22fba759fd4c70636f41b4732`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4637463d4ffc77ae1c82079a154b8ec12faafaeffe0913a0d09deaf28bb49f7`  
		Last Modified: Wed, 25 Jun 2025 18:04:47 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac7f531a859530f45f62257febda686a917ec0c545cd18a333d7fe3c0263e1`  
		Last Modified: Wed, 25 Jun 2025 18:04:50 GMT  
		Size: 22.2 MB (22232346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

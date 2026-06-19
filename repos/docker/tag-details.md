<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.6`](#docker296)
-	[`docker:29.6-cli`](#docker296-cli)
-	[`docker:29.6-dind`](#docker296-dind)
-	[`docker:29.6-dind-rootless`](#docker296-dind-rootless)
-	[`docker:29.6-windowsservercore`](#docker296-windowsservercore)
-	[`docker:29.6-windowsservercore-ltsc2022`](#docker296-windowsservercore-ltsc2022)
-	[`docker:29.6-windowsservercore-ltsc2025`](#docker296-windowsservercore-ltsc2025)
-	[`docker:29.6.0`](#docker2960)
-	[`docker:29.6.0-alpine3.24`](#docker2960-alpine324)
-	[`docker:29.6.0-cli`](#docker2960-cli)
-	[`docker:29.6.0-cli-alpine3.24`](#docker2960-cli-alpine324)
-	[`docker:29.6.0-dind`](#docker2960-dind)
-	[`docker:29.6.0-dind-alpine3.24`](#docker2960-dind-alpine324)
-	[`docker:29.6.0-dind-rootless`](#docker2960-dind-rootless)
-	[`docker:29.6.0-windowsservercore`](#docker2960-windowsservercore)
-	[`docker:29.6.0-windowsservercore-ltsc2022`](#docker2960-windowsservercore-ltsc2022)
-	[`docker:29.6.0-windowsservercore-ltsc2025`](#docker2960-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:7bb861a04bb42bda1d237fc2cb539f9823c9b666ecfbfdbd3e534ab74c8cb976
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
$ docker pull docker@sha256:ac6b53ddb8d0cf0128662faad22917d149c0dc38ea06d19ee77f73aacac785ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142090227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69223e53412298a32a68f53aa962dfd39ed914c741b78d59180d7c58302a217`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:cc89ce54f24170d3e92dc52ddf8d9451830b8093805cc59dfa9947c7650d39a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01538af45e248b6089d3e5d730527b1c41cd13cf7d80910ac9b146f27f82cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:c0ae1d7e8d6d8a75a26ce2b38b3e844ee22f276b95eab267bd0b820df4c919c2`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:ade95fd5db120a8cc651141edd19e1985b5bbbeed68417c4f3cd090086140969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133959761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029fdfd1ee53c34ae022a0e6263fc4789fdb8c35bb1f4f490f16ec3f8b7b331d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b44148ab836c9c91366a663c6061a36ddfe799dd9268e45c41a601b3b1f431`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 7.3 MB (7304119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa72ae8939b6d7f8167771741034d8b3feffafc7dee6187650c48ec4dfb8915`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 90.7 KB (90713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca459390458d8c58ff2e5207edc2bc3e6aa14bb6b22d18ecb09192b7032b5857`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba84346ee44681dc1558263d926ca540e010ed4e6b89bf5ee521a1a395a2e9c`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 64.4 MB (64387101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc367eb5e023ebb9d901cd1bc05761fc3b4c6bbb9a7e35b9dbbb745452f3eb7`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594760236ac59d6bf3223b8cd2eb39e2bf3813283ce6c018becfe64410510763`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:a6665de2e94a1021005baef734d74c522104963efdcf1abb8e0db44ae2515047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e070c59d6a4b0856e4c75d176a9a7908a60d248472d355f20775de1e2e1ac0`

```dockerfile
```

-	Layers:
	-	`sha256:f2368fab42b393cf0d466f41e00852b69e7784e59567cd5dbc36fa5ce4ec58af`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:b537631d5f543ab42b7f667a07e998ede31530378bd901880715a8907cf941c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132036739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c193a82ef71fae6ae3b84ad0bca9e3bb8008f600afa5267a0648d544626169c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7602c19d7a228c5890f9e450eb603232eb5a6353adbaa4a15cc06ddff3e402c`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 6.6 MB (6598797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782a5e9a7bdd6d57edb34dd51a5bdfcac3a2b9bd0b00a3e441db3adc72ca2b40`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 87.0 KB (86952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404d95285dee929efa81c5cadcd238b650a375ce35e7d3d0db9a65e86f7ceeb`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f35c2d8cc43ef5a75265b9cdad73b51e18dc52b986d5d19a9311305f72d291`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 64.2 MB (64214561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f581417afe910c2785f1dcdf1ca6903e8dbf88996a6832a0c594ac27343dd`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af0ec459c273b37aa99112ce185577250dab1a2fba2ec4372d78c21012c3a4`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:6ac5495160751363965222768f91a62c33f88b805821f09566c756ea0f89f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709f117ecc9ccc4d044249905af964d3b2383f208e8254b0f8344be92f7ff96`

```dockerfile
```

-	Layers:
	-	`sha256:e3d876ca2a6f22002c6742169913b8b8d2a033be3a0bd77425918a4a8100dc2a`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ba62bab587d68bde5ca081d7b76c0c57583694fea8f4c9b03b4c50b6d0090b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131427605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66576e67cfcbbdbb70a9229bb13f120d3e9bf7019c043ee2a46ed3f988d5dc97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:ec3ebf2c6e55a734c801ca16b683e21f6e542e86f120e587d6891043a3678a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e309b21efb00099c4b0e8117b961199f6c14bf6ad7d333f3f6aa5f22205f6`

```dockerfile
```

-	Layers:
	-	`sha256:17a4da9f797340aba5ff851c456be7c7548b83ea148ddb8f68053270198b1fff`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:d14410ab6f87a2b6c14b7150de787cd7b8bb012a8e900966d6d893e9f7fc49b6
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
$ docker pull docker@sha256:42d38593dbad18fa64c2a537dad24c8f51f62e59d720b6f15dc160f98cdb42ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65891586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8be2f46589d0a8adba646f841902a069a14646b93f77d7cae334cb42a9623f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:97f98e71dfc570d767a3ff2c6f972d9ec17cb7ffda8b66dc5db1504a791d9b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793f972b0ceda58860edaa7f31e806d6017912f8622fed7a0e223d4c56cd3680`

```dockerfile
```

-	Layers:
	-	`sha256:03ed415629b8212b0cf83d1845548e7da5ce9c4c8611b9ccf8b3b5566e3e3373`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:4774f847734c7369a47961ba5ff7cfa19ae126288e34c23e3e3fe90c5ee53429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62171834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5633626af9c8e62669a6cd73148a7156f723d65f5e04ccd8fbe78300c07fdcf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:51d1f73886650d7d6c21902bc42c79247e5862a9438c4fabd2ca2afdb2e68791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325a023e2548630400f3bd6e92794f4fc3ef3a321adcf13711e3cb37f6ff759f`

```dockerfile
```

-	Layers:
	-	`sha256:665fc45e241bfbd951df799d4e519ca5c59e6dfe5c9c40a2adb1bd115f43153a`  
		Last Modified: Fri, 19 Jun 2026 00:30:16 GMT  
		Size: 38.2 KB (38220 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:315e8347dfed436b55039950bc959101914bf9551d0c43da4739cf07a735f1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61130424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a10087f5f0d1068b8b124197c7540818e3cad4825c7e952ed37ad2633b06158`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f4ce93e0eea54be2ffdc2d6c385552cc3c51c7cf7959a8e639e9d289ad3132f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03441a94ec0257aead90d4c3c8b53a08d7eea8c09226613813074c1cf7737ff8`

```dockerfile
```

-	Layers:
	-	`sha256:a4fb98d917c44326c783d8f2f693ef34cb380191d80fc046966a52acc480cb8e`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fc3958179f7280a4f91830220d8839a3807975f5ac6e6a4423df0748ac8f884a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b0394024e31d35f42d30c3f31d157cad0169b7b1bc7a4ab33155db987a739f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e8f14ba4dfd7bb9880d48574c63c632841ef2df44a62aced6e86ff27ddd5da52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b5718a9bf51646124ad935e427982a3b74d92485c36c179e2c7d8706e56c85`

```dockerfile
```

-	Layers:
	-	`sha256:badc3ecf86315460f9d2dc4e6cbcd98049e813b2a9765d692ffb50b8e63d0efc`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:7bb861a04bb42bda1d237fc2cb539f9823c9b666ecfbfdbd3e534ab74c8cb976
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
$ docker pull docker@sha256:ac6b53ddb8d0cf0128662faad22917d149c0dc38ea06d19ee77f73aacac785ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142090227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69223e53412298a32a68f53aa962dfd39ed914c741b78d59180d7c58302a217`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:cc89ce54f24170d3e92dc52ddf8d9451830b8093805cc59dfa9947c7650d39a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01538af45e248b6089d3e5d730527b1c41cd13cf7d80910ac9b146f27f82cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:c0ae1d7e8d6d8a75a26ce2b38b3e844ee22f276b95eab267bd0b820df4c919c2`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:ade95fd5db120a8cc651141edd19e1985b5bbbeed68417c4f3cd090086140969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133959761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029fdfd1ee53c34ae022a0e6263fc4789fdb8c35bb1f4f490f16ec3f8b7b331d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b44148ab836c9c91366a663c6061a36ddfe799dd9268e45c41a601b3b1f431`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 7.3 MB (7304119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa72ae8939b6d7f8167771741034d8b3feffafc7dee6187650c48ec4dfb8915`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 90.7 KB (90713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca459390458d8c58ff2e5207edc2bc3e6aa14bb6b22d18ecb09192b7032b5857`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba84346ee44681dc1558263d926ca540e010ed4e6b89bf5ee521a1a395a2e9c`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 64.4 MB (64387101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc367eb5e023ebb9d901cd1bc05761fc3b4c6bbb9a7e35b9dbbb745452f3eb7`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594760236ac59d6bf3223b8cd2eb39e2bf3813283ce6c018becfe64410510763`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a6665de2e94a1021005baef734d74c522104963efdcf1abb8e0db44ae2515047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e070c59d6a4b0856e4c75d176a9a7908a60d248472d355f20775de1e2e1ac0`

```dockerfile
```

-	Layers:
	-	`sha256:f2368fab42b393cf0d466f41e00852b69e7784e59567cd5dbc36fa5ce4ec58af`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:b537631d5f543ab42b7f667a07e998ede31530378bd901880715a8907cf941c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132036739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c193a82ef71fae6ae3b84ad0bca9e3bb8008f600afa5267a0648d544626169c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7602c19d7a228c5890f9e450eb603232eb5a6353adbaa4a15cc06ddff3e402c`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 6.6 MB (6598797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782a5e9a7bdd6d57edb34dd51a5bdfcac3a2b9bd0b00a3e441db3adc72ca2b40`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 87.0 KB (86952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404d95285dee929efa81c5cadcd238b650a375ce35e7d3d0db9a65e86f7ceeb`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f35c2d8cc43ef5a75265b9cdad73b51e18dc52b986d5d19a9311305f72d291`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 64.2 MB (64214561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f581417afe910c2785f1dcdf1ca6903e8dbf88996a6832a0c594ac27343dd`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af0ec459c273b37aa99112ce185577250dab1a2fba2ec4372d78c21012c3a4`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6ac5495160751363965222768f91a62c33f88b805821f09566c756ea0f89f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709f117ecc9ccc4d044249905af964d3b2383f208e8254b0f8344be92f7ff96`

```dockerfile
```

-	Layers:
	-	`sha256:e3d876ca2a6f22002c6742169913b8b8d2a033be3a0bd77425918a4a8100dc2a`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ba62bab587d68bde5ca081d7b76c0c57583694fea8f4c9b03b4c50b6d0090b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131427605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66576e67cfcbbdbb70a9229bb13f120d3e9bf7019c043ee2a46ed3f988d5dc97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ec3ebf2c6e55a734c801ca16b683e21f6e542e86f120e587d6891043a3678a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e309b21efb00099c4b0e8117b961199f6c14bf6ad7d333f3f6aa5f22205f6`

```dockerfile
```

-	Layers:
	-	`sha256:17a4da9f797340aba5ff851c456be7c7548b83ea148ddb8f68053270198b1fff`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:d6afe68d2a7648617e95a8f17a8ac59cbc35cc2d8cfe22c40d387e36727386da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d42697e117a63ffb0ca65d43ee4f1d0d40c27a10cb692c830c4c59e3207f88f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157665817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88551c3e8cf1690efd08ab0dcd8d786bfce8a46c19141fb5e0e07672372d3aa5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
# Fri, 19 Jun 2026 02:10:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 19 Jun 2026 02:10:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 19 Jun 2026 02:10:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419e3b36c5c7496ffede1a8cbe30d8067fe2a5882703d9b69bd1ea5b5fc522f8`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 3.5 MB (3470940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2608c2629944dcc1a47baf9e43935062075d2c74c18fe59c2bd5391d889a4182`  
		Last Modified: Fri, 19 Jun 2026 02:10:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bb08eaebb42a68ad5c8e1a6bcceeaf94f79064917892f9fad9bdd363b3c201`  
		Last Modified: Fri, 19 Jun 2026 02:10:57 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5954c8a3bab51d96ff16b24c7784de623b3114e06e36081dbca85a35f77fea21`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 12.1 MB (12103310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf559b90eb3bd3c881831664baf02d8e6f739c11e019f4e18d0317a47372b802`  
		Last Modified: Fri, 19 Jun 2026 02:10:59 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:012bcc9495430f4516d5308bb6e20ae9b7ea8b94bdaea59d2ab72e84839bcab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084774071601e6a0ae2642841c71471664136714a3a954b32ac2464e5c40865b`

```dockerfile
```

-	Layers:
	-	`sha256:9f4cb30c1725e4d0baad7606e01a9c9a36495634a66b1b174ea5d08eb35e5d4b`  
		Last Modified: Fri, 19 Jun 2026 02:10:57 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5bbfc206e4b89e7798cddd64d8a04ffd22d286db582c7ad606682b52ed4737f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146114227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975eb110b97983cdfd78076835d60eadbc7725cf10571cfb7def7afc2edc29f1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
# Fri, 19 Jun 2026 02:10:52 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 19 Jun 2026 02:10:53 GMT
USER rootless
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b85916ff55f8ce2c8da67e7772a25474b355a1dd493f214d41d43253d1548b`  
		Last Modified: Fri, 19 Jun 2026 02:11:00 GMT  
		Size: 3.4 MB (3448189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0bc425a243c0c3eeab80b3e48cf1ea6ec21ccd16a312d98af2f927eb121c35`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5446d512f11d6265cce1ca159d2a482006f4877affb531aef47ef80a551bcc8`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6709844d97a0d426c04590edab3343d70dac7258c494d66b8cf6d7be8c3fe6aa`  
		Last Modified: Fri, 19 Jun 2026 02:11:01 GMT  
		Size: 11.2 MB (11237093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee17a95a048e81c0024fe1c7ba0070d5da1d52476f556326583db6ec29ce5e0`  
		Last Modified: Fri, 19 Jun 2026 02:11:01 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2c45bfb44aa0b61299433e6020d94ac958002fdbcfaaaa025ba91ab1f9c79285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e53d33599a433f08a1651bf641f69073d3a0bdf5afd3d11bb53f9bc8a8a144`

```dockerfile
```

-	Layers:
	-	`sha256:7eb9bc6866e8e0ecd67588973ad4555300490d051e2c2b97238eff97115164f5`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:33ca0ba2ef616adbccf6ec29dbe41037f05ec7b2ff0591eb8191e2bcea9f2d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:3c679d372ae52d1c28c9ab6ebced51a5fc87a64a25d54affae466fb1ae939e6d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335822962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd42ca38e16fd99dae655e21faf8655cb770ec144d9e7dd79d228f01e3d6a62`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 19 Jun 2026 00:32:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:33:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:33:27 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:33:29 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:33:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:46 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:33:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:33:59 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd84ed1f36f4efc3b209c9830da5ce867308531f8850dee14d52abb78c24ef35`  
		Last Modified: Fri, 19 Jun 2026 00:34:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc70eeb4f52ac6a7a7d7219a5aab349b6d1f40aee83507f35f61f570d6946c0`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 407.0 KB (407033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff31ec88e5ceae0d2116513bb8fac8ebf6f8217a0ff82da620022665db87ace`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a63cc16cd2e92c1ae24ececf097f2aa9b42a34e5f5aaa2856f8fba9f8eba49`  
		Last Modified: Fri, 19 Jun 2026 00:34:15 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c51f0c0352a67c5a6d50ec07cdb8f4c25155da43c6ef50149ba4cd148690e9d`  
		Last Modified: Fri, 19 Jun 2026 00:34:18 GMT  
		Size: 20.2 MB (20164255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d47d97257144bf00e368b0b0e424c30f0e617ba8809da54e09ff0d7510ec2`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f4b710350fc80b3707afebe6c639d0a528fcf63e728e7dc7268c605ec36b4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe83587f120b40642d24d410c04f1fe3b06e9269af6636fe95bc3fe76a4d5f4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa274e151272e3ce6c4f4bef2852f2d7ccd285bc4070a087ee737ab8edb812`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 24.0 MB (23974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce95d86829e5292395cf5c68519a8dbeac2dc78a393c768a3069f74f3320e21`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5901d08fde069f52ef9edb45aa9eec15b39e7d34e50c0096956fee163bf36ba8`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78920a4746cf58101f91230b8c0454dafe8ae966df0bcc9735018718e86f69`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36599a24e8dc3e1d8c2d3f0b9e4484ce5dcaa28688b7016a1298b37d7dcb9d8`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 12.1 MB (12122720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:1ceb80b203fc35f1a449bada44bec0ca9cf59a57d893543b8bf7713b770790b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188772660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528c58692e87fbd65e69ca069cfa499808ef51d4652a2999dd5f0536716a1951`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 19 Jun 2026 00:32:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:34:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:34:02 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:34:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:34:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:24 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:34:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:34:26 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:34:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:34:37 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef8125c4e3ba69e4c1b5648bc9e4c51f4f72cd8f7933f46264e122474c534fb`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14a32fee7fc61f8677fdf1f6aaeecd31ff9e20213d1e59cc1f224fc9db8ba53`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 500.8 KB (500768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a6748886801cffcbd40fc56cd739c7893abb9fe2e3ccde48830cf67c53b8`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54be8eb6ae637d7d441fb62bc41ebcbb203d452885a7549652058b22f099c1bd`  
		Last Modified: Fri, 19 Jun 2026 00:34:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6313b440ac970bf7c9d7042bc1a22e367e4acd507b6893cc0479aa3017641d6`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 20.1 MB (20116805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95422775683da39734a4b00798b9565ca9cbf9cd513769ce5c3e806615e2e661`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601dd0e3e31c052c9c89015191a50d2be09baae731765c3adec0afbf9a0f9317`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1255da46d16e32ef90b88172eb889057ec9d997c2eee79e2419090b2f01baa`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5379064dfc9db6e4b3cf409673d41f43552241f3e1acc5eaefd1bb0124281251`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 23.9 MB (23938202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a376f34b936040b15a1dc7cf7baac58bd29dcb2ac1c56876126b7f972b33df`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d50d2853e68cfa1771416ecd51e8ce0c013503da7627107837e7d626911197f`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e5e5fc4cdaaf27fcbb09bc4cc565a3e45e7a2972417de65cbb139832b77d57`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf0b25cc396df62980d6882d986ced7bfbae4595d5e5f01de0d164e46742b14`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 12.1 MB (12079646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:10552617643580c1b4a18cb25bcf958d7a793879b1d3d259e868aa1ca69d1084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:1ceb80b203fc35f1a449bada44bec0ca9cf59a57d893543b8bf7713b770790b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188772660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528c58692e87fbd65e69ca069cfa499808ef51d4652a2999dd5f0536716a1951`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 19 Jun 2026 00:32:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:34:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:34:02 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:34:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:34:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:24 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:34:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:34:26 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:34:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:34:37 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef8125c4e3ba69e4c1b5648bc9e4c51f4f72cd8f7933f46264e122474c534fb`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14a32fee7fc61f8677fdf1f6aaeecd31ff9e20213d1e59cc1f224fc9db8ba53`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 500.8 KB (500768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a6748886801cffcbd40fc56cd739c7893abb9fe2e3ccde48830cf67c53b8`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54be8eb6ae637d7d441fb62bc41ebcbb203d452885a7549652058b22f099c1bd`  
		Last Modified: Fri, 19 Jun 2026 00:34:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6313b440ac970bf7c9d7042bc1a22e367e4acd507b6893cc0479aa3017641d6`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 20.1 MB (20116805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95422775683da39734a4b00798b9565ca9cbf9cd513769ce5c3e806615e2e661`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601dd0e3e31c052c9c89015191a50d2be09baae731765c3adec0afbf9a0f9317`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1255da46d16e32ef90b88172eb889057ec9d997c2eee79e2419090b2f01baa`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5379064dfc9db6e4b3cf409673d41f43552241f3e1acc5eaefd1bb0124281251`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 23.9 MB (23938202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a376f34b936040b15a1dc7cf7baac58bd29dcb2ac1c56876126b7f972b33df`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d50d2853e68cfa1771416ecd51e8ce0c013503da7627107837e7d626911197f`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e5e5fc4cdaaf27fcbb09bc4cc565a3e45e7a2972417de65cbb139832b77d57`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf0b25cc396df62980d6882d986ced7bfbae4595d5e5f01de0d164e46742b14`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 12.1 MB (12079646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:72eb56ff73ff4197d65d10e826964030c0c99de084a5a2ed5b70affbda71f964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:3c679d372ae52d1c28c9ab6ebced51a5fc87a64a25d54affae466fb1ae939e6d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335822962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd42ca38e16fd99dae655e21faf8655cb770ec144d9e7dd79d228f01e3d6a62`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 19 Jun 2026 00:32:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:33:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:33:27 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:33:29 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:33:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:46 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:33:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:33:59 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd84ed1f36f4efc3b209c9830da5ce867308531f8850dee14d52abb78c24ef35`  
		Last Modified: Fri, 19 Jun 2026 00:34:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc70eeb4f52ac6a7a7d7219a5aab349b6d1f40aee83507f35f61f570d6946c0`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 407.0 KB (407033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff31ec88e5ceae0d2116513bb8fac8ebf6f8217a0ff82da620022665db87ace`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a63cc16cd2e92c1ae24ececf097f2aa9b42a34e5f5aaa2856f8fba9f8eba49`  
		Last Modified: Fri, 19 Jun 2026 00:34:15 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c51f0c0352a67c5a6d50ec07cdb8f4c25155da43c6ef50149ba4cd148690e9d`  
		Last Modified: Fri, 19 Jun 2026 00:34:18 GMT  
		Size: 20.2 MB (20164255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d47d97257144bf00e368b0b0e424c30f0e617ba8809da54e09ff0d7510ec2`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f4b710350fc80b3707afebe6c639d0a528fcf63e728e7dc7268c605ec36b4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe83587f120b40642d24d410c04f1fe3b06e9269af6636fe95bc3fe76a4d5f4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa274e151272e3ce6c4f4bef2852f2d7ccd285bc4070a087ee737ab8edb812`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 24.0 MB (23974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce95d86829e5292395cf5c68519a8dbeac2dc78a393c768a3069f74f3320e21`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5901d08fde069f52ef9edb45aa9eec15b39e7d34e50c0096956fee163bf36ba8`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78920a4746cf58101f91230b8c0454dafe8ae966df0bcc9735018718e86f69`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36599a24e8dc3e1d8c2d3f0b9e4484ce5dcaa28688b7016a1298b37d7dcb9d8`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 12.1 MB (12122720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.6`

```console
$ docker pull docker@sha256:7bb861a04bb42bda1d237fc2cb539f9823c9b666ecfbfdbd3e534ab74c8cb976
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

### `docker:29.6` - linux; amd64

```console
$ docker pull docker@sha256:ac6b53ddb8d0cf0128662faad22917d149c0dc38ea06d19ee77f73aacac785ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142090227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69223e53412298a32a68f53aa962dfd39ed914c741b78d59180d7c58302a217`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6` - unknown; unknown

```console
$ docker pull docker@sha256:cc89ce54f24170d3e92dc52ddf8d9451830b8093805cc59dfa9947c7650d39a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01538af45e248b6089d3e5d730527b1c41cd13cf7d80910ac9b146f27f82cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:c0ae1d7e8d6d8a75a26ce2b38b3e844ee22f276b95eab267bd0b820df4c919c2`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6` - linux; arm variant v6

```console
$ docker pull docker@sha256:ade95fd5db120a8cc651141edd19e1985b5bbbeed68417c4f3cd090086140969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133959761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029fdfd1ee53c34ae022a0e6263fc4789fdb8c35bb1f4f490f16ec3f8b7b331d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b44148ab836c9c91366a663c6061a36ddfe799dd9268e45c41a601b3b1f431`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 7.3 MB (7304119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa72ae8939b6d7f8167771741034d8b3feffafc7dee6187650c48ec4dfb8915`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 90.7 KB (90713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca459390458d8c58ff2e5207edc2bc3e6aa14bb6b22d18ecb09192b7032b5857`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba84346ee44681dc1558263d926ca540e010ed4e6b89bf5ee521a1a395a2e9c`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 64.4 MB (64387101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc367eb5e023ebb9d901cd1bc05761fc3b4c6bbb9a7e35b9dbbb745452f3eb7`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594760236ac59d6bf3223b8cd2eb39e2bf3813283ce6c018becfe64410510763`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6` - unknown; unknown

```console
$ docker pull docker@sha256:a6665de2e94a1021005baef734d74c522104963efdcf1abb8e0db44ae2515047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e070c59d6a4b0856e4c75d176a9a7908a60d248472d355f20775de1e2e1ac0`

```dockerfile
```

-	Layers:
	-	`sha256:f2368fab42b393cf0d466f41e00852b69e7784e59567cd5dbc36fa5ce4ec58af`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6` - linux; arm variant v7

```console
$ docker pull docker@sha256:b537631d5f543ab42b7f667a07e998ede31530378bd901880715a8907cf941c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132036739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c193a82ef71fae6ae3b84ad0bca9e3bb8008f600afa5267a0648d544626169c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7602c19d7a228c5890f9e450eb603232eb5a6353adbaa4a15cc06ddff3e402c`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 6.6 MB (6598797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782a5e9a7bdd6d57edb34dd51a5bdfcac3a2b9bd0b00a3e441db3adc72ca2b40`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 87.0 KB (86952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404d95285dee929efa81c5cadcd238b650a375ce35e7d3d0db9a65e86f7ceeb`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f35c2d8cc43ef5a75265b9cdad73b51e18dc52b986d5d19a9311305f72d291`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 64.2 MB (64214561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f581417afe910c2785f1dcdf1ca6903e8dbf88996a6832a0c594ac27343dd`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af0ec459c273b37aa99112ce185577250dab1a2fba2ec4372d78c21012c3a4`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6` - unknown; unknown

```console
$ docker pull docker@sha256:6ac5495160751363965222768f91a62c33f88b805821f09566c756ea0f89f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709f117ecc9ccc4d044249905af964d3b2383f208e8254b0f8344be92f7ff96`

```dockerfile
```

-	Layers:
	-	`sha256:e3d876ca2a6f22002c6742169913b8b8d2a033be3a0bd77425918a4a8100dc2a`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ba62bab587d68bde5ca081d7b76c0c57583694fea8f4c9b03b4c50b6d0090b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131427605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66576e67cfcbbdbb70a9229bb13f120d3e9bf7019c043ee2a46ed3f988d5dc97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6` - unknown; unknown

```console
$ docker pull docker@sha256:ec3ebf2c6e55a734c801ca16b683e21f6e542e86f120e587d6891043a3678a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e309b21efb00099c4b0e8117b961199f6c14bf6ad7d333f3f6aa5f22205f6`

```dockerfile
```

-	Layers:
	-	`sha256:17a4da9f797340aba5ff851c456be7c7548b83ea148ddb8f68053270198b1fff`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.6-cli`

```console
$ docker pull docker@sha256:d14410ab6f87a2b6c14b7150de787cd7b8bb012a8e900966d6d893e9f7fc49b6
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

### `docker:29.6-cli` - linux; amd64

```console
$ docker pull docker@sha256:42d38593dbad18fa64c2a537dad24c8f51f62e59d720b6f15dc160f98cdb42ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65891586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8be2f46589d0a8adba646f841902a069a14646b93f77d7cae334cb42a9623f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6-cli` - unknown; unknown

```console
$ docker pull docker@sha256:97f98e71dfc570d767a3ff2c6f972d9ec17cb7ffda8b66dc5db1504a791d9b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793f972b0ceda58860edaa7f31e806d6017912f8622fed7a0e223d4c56cd3680`

```dockerfile
```

-	Layers:
	-	`sha256:03ed415629b8212b0cf83d1845548e7da5ce9c4c8611b9ccf8b3b5566e3e3373`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:4774f847734c7369a47961ba5ff7cfa19ae126288e34c23e3e3fe90c5ee53429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62171834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5633626af9c8e62669a6cd73148a7156f723d65f5e04ccd8fbe78300c07fdcf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6-cli` - unknown; unknown

```console
$ docker pull docker@sha256:51d1f73886650d7d6c21902bc42c79247e5862a9438c4fabd2ca2afdb2e68791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325a023e2548630400f3bd6e92794f4fc3ef3a321adcf13711e3cb37f6ff759f`

```dockerfile
```

-	Layers:
	-	`sha256:665fc45e241bfbd951df799d4e519ca5c59e6dfe5c9c40a2adb1bd115f43153a`  
		Last Modified: Fri, 19 Jun 2026 00:30:16 GMT  
		Size: 38.2 KB (38220 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:315e8347dfed436b55039950bc959101914bf9551d0c43da4739cf07a735f1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61130424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a10087f5f0d1068b8b124197c7540818e3cad4825c7e952ed37ad2633b06158`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f4ce93e0eea54be2ffdc2d6c385552cc3c51c7cf7959a8e639e9d289ad3132f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03441a94ec0257aead90d4c3c8b53a08d7eea8c09226613813074c1cf7737ff8`

```dockerfile
```

-	Layers:
	-	`sha256:a4fb98d917c44326c783d8f2f693ef34cb380191d80fc046966a52acc480cb8e`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fc3958179f7280a4f91830220d8839a3807975f5ac6e6a4423df0748ac8f884a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b0394024e31d35f42d30c3f31d157cad0169b7b1bc7a4ab33155db987a739f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e8f14ba4dfd7bb9880d48574c63c632841ef2df44a62aced6e86ff27ddd5da52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b5718a9bf51646124ad935e427982a3b74d92485c36c179e2c7d8706e56c85`

```dockerfile
```

-	Layers:
	-	`sha256:badc3ecf86315460f9d2dc4e6cbcd98049e813b2a9765d692ffb50b8e63d0efc`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.6-dind`

```console
$ docker pull docker@sha256:7bb861a04bb42bda1d237fc2cb539f9823c9b666ecfbfdbd3e534ab74c8cb976
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

### `docker:29.6-dind` - linux; amd64

```console
$ docker pull docker@sha256:ac6b53ddb8d0cf0128662faad22917d149c0dc38ea06d19ee77f73aacac785ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142090227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69223e53412298a32a68f53aa962dfd39ed914c741b78d59180d7c58302a217`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6-dind` - unknown; unknown

```console
$ docker pull docker@sha256:cc89ce54f24170d3e92dc52ddf8d9451830b8093805cc59dfa9947c7650d39a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01538af45e248b6089d3e5d730527b1c41cd13cf7d80910ac9b146f27f82cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:c0ae1d7e8d6d8a75a26ce2b38b3e844ee22f276b95eab267bd0b820df4c919c2`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:ade95fd5db120a8cc651141edd19e1985b5bbbeed68417c4f3cd090086140969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133959761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029fdfd1ee53c34ae022a0e6263fc4789fdb8c35bb1f4f490f16ec3f8b7b331d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b44148ab836c9c91366a663c6061a36ddfe799dd9268e45c41a601b3b1f431`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 7.3 MB (7304119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa72ae8939b6d7f8167771741034d8b3feffafc7dee6187650c48ec4dfb8915`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 90.7 KB (90713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca459390458d8c58ff2e5207edc2bc3e6aa14bb6b22d18ecb09192b7032b5857`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba84346ee44681dc1558263d926ca540e010ed4e6b89bf5ee521a1a395a2e9c`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 64.4 MB (64387101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc367eb5e023ebb9d901cd1bc05761fc3b4c6bbb9a7e35b9dbbb745452f3eb7`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594760236ac59d6bf3223b8cd2eb39e2bf3813283ce6c018becfe64410510763`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a6665de2e94a1021005baef734d74c522104963efdcf1abb8e0db44ae2515047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e070c59d6a4b0856e4c75d176a9a7908a60d248472d355f20775de1e2e1ac0`

```dockerfile
```

-	Layers:
	-	`sha256:f2368fab42b393cf0d466f41e00852b69e7784e59567cd5dbc36fa5ce4ec58af`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:b537631d5f543ab42b7f667a07e998ede31530378bd901880715a8907cf941c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132036739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c193a82ef71fae6ae3b84ad0bca9e3bb8008f600afa5267a0648d544626169c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7602c19d7a228c5890f9e450eb603232eb5a6353adbaa4a15cc06ddff3e402c`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 6.6 MB (6598797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782a5e9a7bdd6d57edb34dd51a5bdfcac3a2b9bd0b00a3e441db3adc72ca2b40`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 87.0 KB (86952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404d95285dee929efa81c5cadcd238b650a375ce35e7d3d0db9a65e86f7ceeb`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f35c2d8cc43ef5a75265b9cdad73b51e18dc52b986d5d19a9311305f72d291`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 64.2 MB (64214561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f581417afe910c2785f1dcdf1ca6903e8dbf88996a6832a0c594ac27343dd`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af0ec459c273b37aa99112ce185577250dab1a2fba2ec4372d78c21012c3a4`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6ac5495160751363965222768f91a62c33f88b805821f09566c756ea0f89f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709f117ecc9ccc4d044249905af964d3b2383f208e8254b0f8344be92f7ff96`

```dockerfile
```

-	Layers:
	-	`sha256:e3d876ca2a6f22002c6742169913b8b8d2a033be3a0bd77425918a4a8100dc2a`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ba62bab587d68bde5ca081d7b76c0c57583694fea8f4c9b03b4c50b6d0090b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131427605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66576e67cfcbbdbb70a9229bb13f120d3e9bf7019c043ee2a46ed3f988d5dc97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ec3ebf2c6e55a734c801ca16b683e21f6e542e86f120e587d6891043a3678a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e309b21efb00099c4b0e8117b961199f6c14bf6ad7d333f3f6aa5f22205f6`

```dockerfile
```

-	Layers:
	-	`sha256:17a4da9f797340aba5ff851c456be7c7548b83ea148ddb8f68053270198b1fff`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.6-dind-rootless`

```console
$ docker pull docker@sha256:d6afe68d2a7648617e95a8f17a8ac59cbc35cc2d8cfe22c40d387e36727386da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.6-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d42697e117a63ffb0ca65d43ee4f1d0d40c27a10cb692c830c4c59e3207f88f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157665817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88551c3e8cf1690efd08ab0dcd8d786bfce8a46c19141fb5e0e07672372d3aa5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
# Fri, 19 Jun 2026 02:10:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 19 Jun 2026 02:10:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 19 Jun 2026 02:10:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419e3b36c5c7496ffede1a8cbe30d8067fe2a5882703d9b69bd1ea5b5fc522f8`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 3.5 MB (3470940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2608c2629944dcc1a47baf9e43935062075d2c74c18fe59c2bd5391d889a4182`  
		Last Modified: Fri, 19 Jun 2026 02:10:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bb08eaebb42a68ad5c8e1a6bcceeaf94f79064917892f9fad9bdd363b3c201`  
		Last Modified: Fri, 19 Jun 2026 02:10:57 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5954c8a3bab51d96ff16b24c7784de623b3114e06e36081dbca85a35f77fea21`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 12.1 MB (12103310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf559b90eb3bd3c881831664baf02d8e6f739c11e019f4e18d0317a47372b802`  
		Last Modified: Fri, 19 Jun 2026 02:10:59 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:012bcc9495430f4516d5308bb6e20ae9b7ea8b94bdaea59d2ab72e84839bcab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084774071601e6a0ae2642841c71471664136714a3a954b32ac2464e5c40865b`

```dockerfile
```

-	Layers:
	-	`sha256:9f4cb30c1725e4d0baad7606e01a9c9a36495634a66b1b174ea5d08eb35e5d4b`  
		Last Modified: Fri, 19 Jun 2026 02:10:57 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5bbfc206e4b89e7798cddd64d8a04ffd22d286db582c7ad606682b52ed4737f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146114227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975eb110b97983cdfd78076835d60eadbc7725cf10571cfb7def7afc2edc29f1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
# Fri, 19 Jun 2026 02:10:52 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 19 Jun 2026 02:10:53 GMT
USER rootless
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b85916ff55f8ce2c8da67e7772a25474b355a1dd493f214d41d43253d1548b`  
		Last Modified: Fri, 19 Jun 2026 02:11:00 GMT  
		Size: 3.4 MB (3448189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0bc425a243c0c3eeab80b3e48cf1ea6ec21ccd16a312d98af2f927eb121c35`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5446d512f11d6265cce1ca159d2a482006f4877affb531aef47ef80a551bcc8`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6709844d97a0d426c04590edab3343d70dac7258c494d66b8cf6d7be8c3fe6aa`  
		Last Modified: Fri, 19 Jun 2026 02:11:01 GMT  
		Size: 11.2 MB (11237093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee17a95a048e81c0024fe1c7ba0070d5da1d52476f556326583db6ec29ce5e0`  
		Last Modified: Fri, 19 Jun 2026 02:11:01 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2c45bfb44aa0b61299433e6020d94ac958002fdbcfaaaa025ba91ab1f9c79285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e53d33599a433f08a1651bf641f69073d3a0bdf5afd3d11bb53f9bc8a8a144`

```dockerfile
```

-	Layers:
	-	`sha256:7eb9bc6866e8e0ecd67588973ad4555300490d051e2c2b97238eff97115164f5`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.6-windowsservercore`

```console
$ docker pull docker@sha256:33ca0ba2ef616adbccf6ec29dbe41037f05ec7b2ff0591eb8191e2bcea9f2d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `docker:29.6-windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:3c679d372ae52d1c28c9ab6ebced51a5fc87a64a25d54affae466fb1ae939e6d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335822962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd42ca38e16fd99dae655e21faf8655cb770ec144d9e7dd79d228f01e3d6a62`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 19 Jun 2026 00:32:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:33:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:33:27 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:33:29 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:33:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:46 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:33:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:33:59 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd84ed1f36f4efc3b209c9830da5ce867308531f8850dee14d52abb78c24ef35`  
		Last Modified: Fri, 19 Jun 2026 00:34:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc70eeb4f52ac6a7a7d7219a5aab349b6d1f40aee83507f35f61f570d6946c0`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 407.0 KB (407033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff31ec88e5ceae0d2116513bb8fac8ebf6f8217a0ff82da620022665db87ace`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a63cc16cd2e92c1ae24ececf097f2aa9b42a34e5f5aaa2856f8fba9f8eba49`  
		Last Modified: Fri, 19 Jun 2026 00:34:15 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c51f0c0352a67c5a6d50ec07cdb8f4c25155da43c6ef50149ba4cd148690e9d`  
		Last Modified: Fri, 19 Jun 2026 00:34:18 GMT  
		Size: 20.2 MB (20164255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d47d97257144bf00e368b0b0e424c30f0e617ba8809da54e09ff0d7510ec2`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f4b710350fc80b3707afebe6c639d0a528fcf63e728e7dc7268c605ec36b4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe83587f120b40642d24d410c04f1fe3b06e9269af6636fe95bc3fe76a4d5f4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa274e151272e3ce6c4f4bef2852f2d7ccd285bc4070a087ee737ab8edb812`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 24.0 MB (23974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce95d86829e5292395cf5c68519a8dbeac2dc78a393c768a3069f74f3320e21`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5901d08fde069f52ef9edb45aa9eec15b39e7d34e50c0096956fee163bf36ba8`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78920a4746cf58101f91230b8c0454dafe8ae966df0bcc9735018718e86f69`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36599a24e8dc3e1d8c2d3f0b9e4484ce5dcaa28688b7016a1298b37d7dcb9d8`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 12.1 MB (12122720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.6-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:1ceb80b203fc35f1a449bada44bec0ca9cf59a57d893543b8bf7713b770790b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188772660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528c58692e87fbd65e69ca069cfa499808ef51d4652a2999dd5f0536716a1951`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 19 Jun 2026 00:32:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:34:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:34:02 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:34:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:34:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:24 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:34:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:34:26 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:34:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:34:37 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef8125c4e3ba69e4c1b5648bc9e4c51f4f72cd8f7933f46264e122474c534fb`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14a32fee7fc61f8677fdf1f6aaeecd31ff9e20213d1e59cc1f224fc9db8ba53`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 500.8 KB (500768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a6748886801cffcbd40fc56cd739c7893abb9fe2e3ccde48830cf67c53b8`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54be8eb6ae637d7d441fb62bc41ebcbb203d452885a7549652058b22f099c1bd`  
		Last Modified: Fri, 19 Jun 2026 00:34:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6313b440ac970bf7c9d7042bc1a22e367e4acd507b6893cc0479aa3017641d6`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 20.1 MB (20116805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95422775683da39734a4b00798b9565ca9cbf9cd513769ce5c3e806615e2e661`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601dd0e3e31c052c9c89015191a50d2be09baae731765c3adec0afbf9a0f9317`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1255da46d16e32ef90b88172eb889057ec9d997c2eee79e2419090b2f01baa`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5379064dfc9db6e4b3cf409673d41f43552241f3e1acc5eaefd1bb0124281251`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 23.9 MB (23938202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a376f34b936040b15a1dc7cf7baac58bd29dcb2ac1c56876126b7f972b33df`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d50d2853e68cfa1771416ecd51e8ce0c013503da7627107837e7d626911197f`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e5e5fc4cdaaf27fcbb09bc4cc565a3e45e7a2972417de65cbb139832b77d57`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf0b25cc396df62980d6882d986ced7bfbae4595d5e5f01de0d164e46742b14`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 12.1 MB (12079646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.6-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:10552617643580c1b4a18cb25bcf958d7a793879b1d3d259e868aa1ca69d1084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `docker:29.6-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:1ceb80b203fc35f1a449bada44bec0ca9cf59a57d893543b8bf7713b770790b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188772660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528c58692e87fbd65e69ca069cfa499808ef51d4652a2999dd5f0536716a1951`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 19 Jun 2026 00:32:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:34:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:34:02 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:34:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:34:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:24 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:34:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:34:26 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:34:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:34:37 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef8125c4e3ba69e4c1b5648bc9e4c51f4f72cd8f7933f46264e122474c534fb`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14a32fee7fc61f8677fdf1f6aaeecd31ff9e20213d1e59cc1f224fc9db8ba53`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 500.8 KB (500768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a6748886801cffcbd40fc56cd739c7893abb9fe2e3ccde48830cf67c53b8`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54be8eb6ae637d7d441fb62bc41ebcbb203d452885a7549652058b22f099c1bd`  
		Last Modified: Fri, 19 Jun 2026 00:34:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6313b440ac970bf7c9d7042bc1a22e367e4acd507b6893cc0479aa3017641d6`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 20.1 MB (20116805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95422775683da39734a4b00798b9565ca9cbf9cd513769ce5c3e806615e2e661`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601dd0e3e31c052c9c89015191a50d2be09baae731765c3adec0afbf9a0f9317`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1255da46d16e32ef90b88172eb889057ec9d997c2eee79e2419090b2f01baa`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5379064dfc9db6e4b3cf409673d41f43552241f3e1acc5eaefd1bb0124281251`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 23.9 MB (23938202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a376f34b936040b15a1dc7cf7baac58bd29dcb2ac1c56876126b7f972b33df`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d50d2853e68cfa1771416ecd51e8ce0c013503da7627107837e7d626911197f`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e5e5fc4cdaaf27fcbb09bc4cc565a3e45e7a2972417de65cbb139832b77d57`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf0b25cc396df62980d6882d986ced7bfbae4595d5e5f01de0d164e46742b14`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 12.1 MB (12079646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.6-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:72eb56ff73ff4197d65d10e826964030c0c99de084a5a2ed5b70affbda71f964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `docker:29.6-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:3c679d372ae52d1c28c9ab6ebced51a5fc87a64a25d54affae466fb1ae939e6d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335822962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd42ca38e16fd99dae655e21faf8655cb770ec144d9e7dd79d228f01e3d6a62`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 19 Jun 2026 00:32:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:33:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:33:27 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:33:29 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:33:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:46 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:33:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:33:59 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd84ed1f36f4efc3b209c9830da5ce867308531f8850dee14d52abb78c24ef35`  
		Last Modified: Fri, 19 Jun 2026 00:34:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc70eeb4f52ac6a7a7d7219a5aab349b6d1f40aee83507f35f61f570d6946c0`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 407.0 KB (407033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff31ec88e5ceae0d2116513bb8fac8ebf6f8217a0ff82da620022665db87ace`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a63cc16cd2e92c1ae24ececf097f2aa9b42a34e5f5aaa2856f8fba9f8eba49`  
		Last Modified: Fri, 19 Jun 2026 00:34:15 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c51f0c0352a67c5a6d50ec07cdb8f4c25155da43c6ef50149ba4cd148690e9d`  
		Last Modified: Fri, 19 Jun 2026 00:34:18 GMT  
		Size: 20.2 MB (20164255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d47d97257144bf00e368b0b0e424c30f0e617ba8809da54e09ff0d7510ec2`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f4b710350fc80b3707afebe6c639d0a528fcf63e728e7dc7268c605ec36b4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe83587f120b40642d24d410c04f1fe3b06e9269af6636fe95bc3fe76a4d5f4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa274e151272e3ce6c4f4bef2852f2d7ccd285bc4070a087ee737ab8edb812`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 24.0 MB (23974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce95d86829e5292395cf5c68519a8dbeac2dc78a393c768a3069f74f3320e21`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5901d08fde069f52ef9edb45aa9eec15b39e7d34e50c0096956fee163bf36ba8`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78920a4746cf58101f91230b8c0454dafe8ae966df0bcc9735018718e86f69`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36599a24e8dc3e1d8c2d3f0b9e4484ce5dcaa28688b7016a1298b37d7dcb9d8`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 12.1 MB (12122720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.6.0`

```console
$ docker pull docker@sha256:7bb861a04bb42bda1d237fc2cb539f9823c9b666ecfbfdbd3e534ab74c8cb976
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

### `docker:29.6.0` - linux; amd64

```console
$ docker pull docker@sha256:ac6b53ddb8d0cf0128662faad22917d149c0dc38ea06d19ee77f73aacac785ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142090227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69223e53412298a32a68f53aa962dfd39ed914c741b78d59180d7c58302a217`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0` - unknown; unknown

```console
$ docker pull docker@sha256:cc89ce54f24170d3e92dc52ddf8d9451830b8093805cc59dfa9947c7650d39a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01538af45e248b6089d3e5d730527b1c41cd13cf7d80910ac9b146f27f82cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:c0ae1d7e8d6d8a75a26ce2b38b3e844ee22f276b95eab267bd0b820df4c919c2`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:ade95fd5db120a8cc651141edd19e1985b5bbbeed68417c4f3cd090086140969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133959761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029fdfd1ee53c34ae022a0e6263fc4789fdb8c35bb1f4f490f16ec3f8b7b331d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b44148ab836c9c91366a663c6061a36ddfe799dd9268e45c41a601b3b1f431`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 7.3 MB (7304119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa72ae8939b6d7f8167771741034d8b3feffafc7dee6187650c48ec4dfb8915`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 90.7 KB (90713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca459390458d8c58ff2e5207edc2bc3e6aa14bb6b22d18ecb09192b7032b5857`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba84346ee44681dc1558263d926ca540e010ed4e6b89bf5ee521a1a395a2e9c`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 64.4 MB (64387101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc367eb5e023ebb9d901cd1bc05761fc3b4c6bbb9a7e35b9dbbb745452f3eb7`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594760236ac59d6bf3223b8cd2eb39e2bf3813283ce6c018becfe64410510763`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0` - unknown; unknown

```console
$ docker pull docker@sha256:a6665de2e94a1021005baef734d74c522104963efdcf1abb8e0db44ae2515047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e070c59d6a4b0856e4c75d176a9a7908a60d248472d355f20775de1e2e1ac0`

```dockerfile
```

-	Layers:
	-	`sha256:f2368fab42b393cf0d466f41e00852b69e7784e59567cd5dbc36fa5ce4ec58af`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:b537631d5f543ab42b7f667a07e998ede31530378bd901880715a8907cf941c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132036739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c193a82ef71fae6ae3b84ad0bca9e3bb8008f600afa5267a0648d544626169c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7602c19d7a228c5890f9e450eb603232eb5a6353adbaa4a15cc06ddff3e402c`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 6.6 MB (6598797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782a5e9a7bdd6d57edb34dd51a5bdfcac3a2b9bd0b00a3e441db3adc72ca2b40`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 87.0 KB (86952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404d95285dee929efa81c5cadcd238b650a375ce35e7d3d0db9a65e86f7ceeb`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f35c2d8cc43ef5a75265b9cdad73b51e18dc52b986d5d19a9311305f72d291`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 64.2 MB (64214561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f581417afe910c2785f1dcdf1ca6903e8dbf88996a6832a0c594ac27343dd`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af0ec459c273b37aa99112ce185577250dab1a2fba2ec4372d78c21012c3a4`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0` - unknown; unknown

```console
$ docker pull docker@sha256:6ac5495160751363965222768f91a62c33f88b805821f09566c756ea0f89f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709f117ecc9ccc4d044249905af964d3b2383f208e8254b0f8344be92f7ff96`

```dockerfile
```

-	Layers:
	-	`sha256:e3d876ca2a6f22002c6742169913b8b8d2a033be3a0bd77425918a4a8100dc2a`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ba62bab587d68bde5ca081d7b76c0c57583694fea8f4c9b03b4c50b6d0090b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131427605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66576e67cfcbbdbb70a9229bb13f120d3e9bf7019c043ee2a46ed3f988d5dc97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0` - unknown; unknown

```console
$ docker pull docker@sha256:ec3ebf2c6e55a734c801ca16b683e21f6e542e86f120e587d6891043a3678a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e309b21efb00099c4b0e8117b961199f6c14bf6ad7d333f3f6aa5f22205f6`

```dockerfile
```

-	Layers:
	-	`sha256:17a4da9f797340aba5ff851c456be7c7548b83ea148ddb8f68053270198b1fff`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.6.0-alpine3.24`

```console
$ docker pull docker@sha256:7bb861a04bb42bda1d237fc2cb539f9823c9b666ecfbfdbd3e534ab74c8cb976
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

### `docker:29.6.0-alpine3.24` - linux; amd64

```console
$ docker pull docker@sha256:ac6b53ddb8d0cf0128662faad22917d149c0dc38ea06d19ee77f73aacac785ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142090227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69223e53412298a32a68f53aa962dfd39ed914c741b78d59180d7c58302a217`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-alpine3.24` - unknown; unknown

```console
$ docker pull docker@sha256:cc89ce54f24170d3e92dc52ddf8d9451830b8093805cc59dfa9947c7650d39a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01538af45e248b6089d3e5d730527b1c41cd13cf7d80910ac9b146f27f82cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:c0ae1d7e8d6d8a75a26ce2b38b3e844ee22f276b95eab267bd0b820df4c919c2`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-alpine3.24` - linux; arm variant v6

```console
$ docker pull docker@sha256:ade95fd5db120a8cc651141edd19e1985b5bbbeed68417c4f3cd090086140969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133959761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029fdfd1ee53c34ae022a0e6263fc4789fdb8c35bb1f4f490f16ec3f8b7b331d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b44148ab836c9c91366a663c6061a36ddfe799dd9268e45c41a601b3b1f431`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 7.3 MB (7304119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa72ae8939b6d7f8167771741034d8b3feffafc7dee6187650c48ec4dfb8915`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 90.7 KB (90713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca459390458d8c58ff2e5207edc2bc3e6aa14bb6b22d18ecb09192b7032b5857`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba84346ee44681dc1558263d926ca540e010ed4e6b89bf5ee521a1a395a2e9c`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 64.4 MB (64387101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc367eb5e023ebb9d901cd1bc05761fc3b4c6bbb9a7e35b9dbbb745452f3eb7`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594760236ac59d6bf3223b8cd2eb39e2bf3813283ce6c018becfe64410510763`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-alpine3.24` - unknown; unknown

```console
$ docker pull docker@sha256:a6665de2e94a1021005baef734d74c522104963efdcf1abb8e0db44ae2515047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e070c59d6a4b0856e4c75d176a9a7908a60d248472d355f20775de1e2e1ac0`

```dockerfile
```

-	Layers:
	-	`sha256:f2368fab42b393cf0d466f41e00852b69e7784e59567cd5dbc36fa5ce4ec58af`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-alpine3.24` - linux; arm variant v7

```console
$ docker pull docker@sha256:b537631d5f543ab42b7f667a07e998ede31530378bd901880715a8907cf941c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132036739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c193a82ef71fae6ae3b84ad0bca9e3bb8008f600afa5267a0648d544626169c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7602c19d7a228c5890f9e450eb603232eb5a6353adbaa4a15cc06ddff3e402c`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 6.6 MB (6598797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782a5e9a7bdd6d57edb34dd51a5bdfcac3a2b9bd0b00a3e441db3adc72ca2b40`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 87.0 KB (86952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404d95285dee929efa81c5cadcd238b650a375ce35e7d3d0db9a65e86f7ceeb`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f35c2d8cc43ef5a75265b9cdad73b51e18dc52b986d5d19a9311305f72d291`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 64.2 MB (64214561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f581417afe910c2785f1dcdf1ca6903e8dbf88996a6832a0c594ac27343dd`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af0ec459c273b37aa99112ce185577250dab1a2fba2ec4372d78c21012c3a4`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-alpine3.24` - unknown; unknown

```console
$ docker pull docker@sha256:6ac5495160751363965222768f91a62c33f88b805821f09566c756ea0f89f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709f117ecc9ccc4d044249905af964d3b2383f208e8254b0f8344be92f7ff96`

```dockerfile
```

-	Layers:
	-	`sha256:e3d876ca2a6f22002c6742169913b8b8d2a033be3a0bd77425918a4a8100dc2a`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ba62bab587d68bde5ca081d7b76c0c57583694fea8f4c9b03b4c50b6d0090b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131427605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66576e67cfcbbdbb70a9229bb13f120d3e9bf7019c043ee2a46ed3f988d5dc97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-alpine3.24` - unknown; unknown

```console
$ docker pull docker@sha256:ec3ebf2c6e55a734c801ca16b683e21f6e542e86f120e587d6891043a3678a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e309b21efb00099c4b0e8117b961199f6c14bf6ad7d333f3f6aa5f22205f6`

```dockerfile
```

-	Layers:
	-	`sha256:17a4da9f797340aba5ff851c456be7c7548b83ea148ddb8f68053270198b1fff`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.6.0-cli`

```console
$ docker pull docker@sha256:d14410ab6f87a2b6c14b7150de787cd7b8bb012a8e900966d6d893e9f7fc49b6
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

### `docker:29.6.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:42d38593dbad18fa64c2a537dad24c8f51f62e59d720b6f15dc160f98cdb42ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65891586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8be2f46589d0a8adba646f841902a069a14646b93f77d7cae334cb42a9623f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:97f98e71dfc570d767a3ff2c6f972d9ec17cb7ffda8b66dc5db1504a791d9b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793f972b0ceda58860edaa7f31e806d6017912f8622fed7a0e223d4c56cd3680`

```dockerfile
```

-	Layers:
	-	`sha256:03ed415629b8212b0cf83d1845548e7da5ce9c4c8611b9ccf8b3b5566e3e3373`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:4774f847734c7369a47961ba5ff7cfa19ae126288e34c23e3e3fe90c5ee53429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62171834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5633626af9c8e62669a6cd73148a7156f723d65f5e04ccd8fbe78300c07fdcf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:51d1f73886650d7d6c21902bc42c79247e5862a9438c4fabd2ca2afdb2e68791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325a023e2548630400f3bd6e92794f4fc3ef3a321adcf13711e3cb37f6ff759f`

```dockerfile
```

-	Layers:
	-	`sha256:665fc45e241bfbd951df799d4e519ca5c59e6dfe5c9c40a2adb1bd115f43153a`  
		Last Modified: Fri, 19 Jun 2026 00:30:16 GMT  
		Size: 38.2 KB (38220 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:315e8347dfed436b55039950bc959101914bf9551d0c43da4739cf07a735f1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61130424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a10087f5f0d1068b8b124197c7540818e3cad4825c7e952ed37ad2633b06158`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f4ce93e0eea54be2ffdc2d6c385552cc3c51c7cf7959a8e639e9d289ad3132f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03441a94ec0257aead90d4c3c8b53a08d7eea8c09226613813074c1cf7737ff8`

```dockerfile
```

-	Layers:
	-	`sha256:a4fb98d917c44326c783d8f2f693ef34cb380191d80fc046966a52acc480cb8e`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fc3958179f7280a4f91830220d8839a3807975f5ac6e6a4423df0748ac8f884a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b0394024e31d35f42d30c3f31d157cad0169b7b1bc7a4ab33155db987a739f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e8f14ba4dfd7bb9880d48574c63c632841ef2df44a62aced6e86ff27ddd5da52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b5718a9bf51646124ad935e427982a3b74d92485c36c179e2c7d8706e56c85`

```dockerfile
```

-	Layers:
	-	`sha256:badc3ecf86315460f9d2dc4e6cbcd98049e813b2a9765d692ffb50b8e63d0efc`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.6.0-cli-alpine3.24`

```console
$ docker pull docker@sha256:d14410ab6f87a2b6c14b7150de787cd7b8bb012a8e900966d6d893e9f7fc49b6
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

### `docker:29.6.0-cli-alpine3.24` - linux; amd64

```console
$ docker pull docker@sha256:42d38593dbad18fa64c2a537dad24c8f51f62e59d720b6f15dc160f98cdb42ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65891586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8be2f46589d0a8adba646f841902a069a14646b93f77d7cae334cb42a9623f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-cli-alpine3.24` - unknown; unknown

```console
$ docker pull docker@sha256:97f98e71dfc570d767a3ff2c6f972d9ec17cb7ffda8b66dc5db1504a791d9b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793f972b0ceda58860edaa7f31e806d6017912f8622fed7a0e223d4c56cd3680`

```dockerfile
```

-	Layers:
	-	`sha256:03ed415629b8212b0cf83d1845548e7da5ce9c4c8611b9ccf8b3b5566e3e3373`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-cli-alpine3.24` - linux; arm variant v6

```console
$ docker pull docker@sha256:4774f847734c7369a47961ba5ff7cfa19ae126288e34c23e3e3fe90c5ee53429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62171834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5633626af9c8e62669a6cd73148a7156f723d65f5e04ccd8fbe78300c07fdcf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-cli-alpine3.24` - unknown; unknown

```console
$ docker pull docker@sha256:51d1f73886650d7d6c21902bc42c79247e5862a9438c4fabd2ca2afdb2e68791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325a023e2548630400f3bd6e92794f4fc3ef3a321adcf13711e3cb37f6ff759f`

```dockerfile
```

-	Layers:
	-	`sha256:665fc45e241bfbd951df799d4e519ca5c59e6dfe5c9c40a2adb1bd115f43153a`  
		Last Modified: Fri, 19 Jun 2026 00:30:16 GMT  
		Size: 38.2 KB (38220 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-cli-alpine3.24` - linux; arm variant v7

```console
$ docker pull docker@sha256:315e8347dfed436b55039950bc959101914bf9551d0c43da4739cf07a735f1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61130424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a10087f5f0d1068b8b124197c7540818e3cad4825c7e952ed37ad2633b06158`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-cli-alpine3.24` - unknown; unknown

```console
$ docker pull docker@sha256:f4ce93e0eea54be2ffdc2d6c385552cc3c51c7cf7959a8e639e9d289ad3132f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03441a94ec0257aead90d4c3c8b53a08d7eea8c09226613813074c1cf7737ff8`

```dockerfile
```

-	Layers:
	-	`sha256:a4fb98d917c44326c783d8f2f693ef34cb380191d80fc046966a52acc480cb8e`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-cli-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fc3958179f7280a4f91830220d8839a3807975f5ac6e6a4423df0748ac8f884a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b0394024e31d35f42d30c3f31d157cad0169b7b1bc7a4ab33155db987a739f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-cli-alpine3.24` - unknown; unknown

```console
$ docker pull docker@sha256:e8f14ba4dfd7bb9880d48574c63c632841ef2df44a62aced6e86ff27ddd5da52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b5718a9bf51646124ad935e427982a3b74d92485c36c179e2c7d8706e56c85`

```dockerfile
```

-	Layers:
	-	`sha256:badc3ecf86315460f9d2dc4e6cbcd98049e813b2a9765d692ffb50b8e63d0efc`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.6.0-dind`

```console
$ docker pull docker@sha256:7bb861a04bb42bda1d237fc2cb539f9823c9b666ecfbfdbd3e534ab74c8cb976
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

### `docker:29.6.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:ac6b53ddb8d0cf0128662faad22917d149c0dc38ea06d19ee77f73aacac785ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142090227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69223e53412298a32a68f53aa962dfd39ed914c741b78d59180d7c58302a217`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:cc89ce54f24170d3e92dc52ddf8d9451830b8093805cc59dfa9947c7650d39a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01538af45e248b6089d3e5d730527b1c41cd13cf7d80910ac9b146f27f82cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:c0ae1d7e8d6d8a75a26ce2b38b3e844ee22f276b95eab267bd0b820df4c919c2`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:ade95fd5db120a8cc651141edd19e1985b5bbbeed68417c4f3cd090086140969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133959761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029fdfd1ee53c34ae022a0e6263fc4789fdb8c35bb1f4f490f16ec3f8b7b331d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b44148ab836c9c91366a663c6061a36ddfe799dd9268e45c41a601b3b1f431`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 7.3 MB (7304119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa72ae8939b6d7f8167771741034d8b3feffafc7dee6187650c48ec4dfb8915`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 90.7 KB (90713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca459390458d8c58ff2e5207edc2bc3e6aa14bb6b22d18ecb09192b7032b5857`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba84346ee44681dc1558263d926ca540e010ed4e6b89bf5ee521a1a395a2e9c`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 64.4 MB (64387101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc367eb5e023ebb9d901cd1bc05761fc3b4c6bbb9a7e35b9dbbb745452f3eb7`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594760236ac59d6bf3223b8cd2eb39e2bf3813283ce6c018becfe64410510763`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a6665de2e94a1021005baef734d74c522104963efdcf1abb8e0db44ae2515047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e070c59d6a4b0856e4c75d176a9a7908a60d248472d355f20775de1e2e1ac0`

```dockerfile
```

-	Layers:
	-	`sha256:f2368fab42b393cf0d466f41e00852b69e7784e59567cd5dbc36fa5ce4ec58af`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:b537631d5f543ab42b7f667a07e998ede31530378bd901880715a8907cf941c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132036739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c193a82ef71fae6ae3b84ad0bca9e3bb8008f600afa5267a0648d544626169c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7602c19d7a228c5890f9e450eb603232eb5a6353adbaa4a15cc06ddff3e402c`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 6.6 MB (6598797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782a5e9a7bdd6d57edb34dd51a5bdfcac3a2b9bd0b00a3e441db3adc72ca2b40`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 87.0 KB (86952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404d95285dee929efa81c5cadcd238b650a375ce35e7d3d0db9a65e86f7ceeb`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f35c2d8cc43ef5a75265b9cdad73b51e18dc52b986d5d19a9311305f72d291`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 64.2 MB (64214561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f581417afe910c2785f1dcdf1ca6903e8dbf88996a6832a0c594ac27343dd`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af0ec459c273b37aa99112ce185577250dab1a2fba2ec4372d78c21012c3a4`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6ac5495160751363965222768f91a62c33f88b805821f09566c756ea0f89f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709f117ecc9ccc4d044249905af964d3b2383f208e8254b0f8344be92f7ff96`

```dockerfile
```

-	Layers:
	-	`sha256:e3d876ca2a6f22002c6742169913b8b8d2a033be3a0bd77425918a4a8100dc2a`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ba62bab587d68bde5ca081d7b76c0c57583694fea8f4c9b03b4c50b6d0090b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131427605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66576e67cfcbbdbb70a9229bb13f120d3e9bf7019c043ee2a46ed3f988d5dc97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ec3ebf2c6e55a734c801ca16b683e21f6e542e86f120e587d6891043a3678a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e309b21efb00099c4b0e8117b961199f6c14bf6ad7d333f3f6aa5f22205f6`

```dockerfile
```

-	Layers:
	-	`sha256:17a4da9f797340aba5ff851c456be7c7548b83ea148ddb8f68053270198b1fff`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.6.0-dind-alpine3.24`

```console
$ docker pull docker@sha256:7bb861a04bb42bda1d237fc2cb539f9823c9b666ecfbfdbd3e534ab74c8cb976
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

### `docker:29.6.0-dind-alpine3.24` - linux; amd64

```console
$ docker pull docker@sha256:ac6b53ddb8d0cf0128662faad22917d149c0dc38ea06d19ee77f73aacac785ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142090227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69223e53412298a32a68f53aa962dfd39ed914c741b78d59180d7c58302a217`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-dind-alpine3.24` - unknown; unknown

```console
$ docker pull docker@sha256:cc89ce54f24170d3e92dc52ddf8d9451830b8093805cc59dfa9947c7650d39a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01538af45e248b6089d3e5d730527b1c41cd13cf7d80910ac9b146f27f82cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:c0ae1d7e8d6d8a75a26ce2b38b3e844ee22f276b95eab267bd0b820df4c919c2`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-dind-alpine3.24` - linux; arm variant v6

```console
$ docker pull docker@sha256:ade95fd5db120a8cc651141edd19e1985b5bbbeed68417c4f3cd090086140969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133959761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029fdfd1ee53c34ae022a0e6263fc4789fdb8c35bb1f4f490f16ec3f8b7b331d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b44148ab836c9c91366a663c6061a36ddfe799dd9268e45c41a601b3b1f431`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 7.3 MB (7304119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa72ae8939b6d7f8167771741034d8b3feffafc7dee6187650c48ec4dfb8915`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 90.7 KB (90713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca459390458d8c58ff2e5207edc2bc3e6aa14bb6b22d18ecb09192b7032b5857`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba84346ee44681dc1558263d926ca540e010ed4e6b89bf5ee521a1a395a2e9c`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 64.4 MB (64387101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc367eb5e023ebb9d901cd1bc05761fc3b4c6bbb9a7e35b9dbbb745452f3eb7`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594760236ac59d6bf3223b8cd2eb39e2bf3813283ce6c018becfe64410510763`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-dind-alpine3.24` - unknown; unknown

```console
$ docker pull docker@sha256:a6665de2e94a1021005baef734d74c522104963efdcf1abb8e0db44ae2515047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e070c59d6a4b0856e4c75d176a9a7908a60d248472d355f20775de1e2e1ac0`

```dockerfile
```

-	Layers:
	-	`sha256:f2368fab42b393cf0d466f41e00852b69e7784e59567cd5dbc36fa5ce4ec58af`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-dind-alpine3.24` - linux; arm variant v7

```console
$ docker pull docker@sha256:b537631d5f543ab42b7f667a07e998ede31530378bd901880715a8907cf941c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132036739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c193a82ef71fae6ae3b84ad0bca9e3bb8008f600afa5267a0648d544626169c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7602c19d7a228c5890f9e450eb603232eb5a6353adbaa4a15cc06ddff3e402c`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 6.6 MB (6598797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782a5e9a7bdd6d57edb34dd51a5bdfcac3a2b9bd0b00a3e441db3adc72ca2b40`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 87.0 KB (86952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404d95285dee929efa81c5cadcd238b650a375ce35e7d3d0db9a65e86f7ceeb`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f35c2d8cc43ef5a75265b9cdad73b51e18dc52b986d5d19a9311305f72d291`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 64.2 MB (64214561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f581417afe910c2785f1dcdf1ca6903e8dbf88996a6832a0c594ac27343dd`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af0ec459c273b37aa99112ce185577250dab1a2fba2ec4372d78c21012c3a4`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-dind-alpine3.24` - unknown; unknown

```console
$ docker pull docker@sha256:6ac5495160751363965222768f91a62c33f88b805821f09566c756ea0f89f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709f117ecc9ccc4d044249905af964d3b2383f208e8254b0f8344be92f7ff96`

```dockerfile
```

-	Layers:
	-	`sha256:e3d876ca2a6f22002c6742169913b8b8d2a033be3a0bd77425918a4a8100dc2a`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-dind-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ba62bab587d68bde5ca081d7b76c0c57583694fea8f4c9b03b4c50b6d0090b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131427605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66576e67cfcbbdbb70a9229bb13f120d3e9bf7019c043ee2a46ed3f988d5dc97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-dind-alpine3.24` - unknown; unknown

```console
$ docker pull docker@sha256:ec3ebf2c6e55a734c801ca16b683e21f6e542e86f120e587d6891043a3678a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e309b21efb00099c4b0e8117b961199f6c14bf6ad7d333f3f6aa5f22205f6`

```dockerfile
```

-	Layers:
	-	`sha256:17a4da9f797340aba5ff851c456be7c7548b83ea148ddb8f68053270198b1fff`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.6.0-dind-rootless`

```console
$ docker pull docker@sha256:d6afe68d2a7648617e95a8f17a8ac59cbc35cc2d8cfe22c40d387e36727386da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.6.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d42697e117a63ffb0ca65d43ee4f1d0d40c27a10cb692c830c4c59e3207f88f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157665817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88551c3e8cf1690efd08ab0dcd8d786bfce8a46c19141fb5e0e07672372d3aa5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
# Fri, 19 Jun 2026 02:10:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 19 Jun 2026 02:10:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 19 Jun 2026 02:10:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419e3b36c5c7496ffede1a8cbe30d8067fe2a5882703d9b69bd1ea5b5fc522f8`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 3.5 MB (3470940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2608c2629944dcc1a47baf9e43935062075d2c74c18fe59c2bd5391d889a4182`  
		Last Modified: Fri, 19 Jun 2026 02:10:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bb08eaebb42a68ad5c8e1a6bcceeaf94f79064917892f9fad9bdd363b3c201`  
		Last Modified: Fri, 19 Jun 2026 02:10:57 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5954c8a3bab51d96ff16b24c7784de623b3114e06e36081dbca85a35f77fea21`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 12.1 MB (12103310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf559b90eb3bd3c881831664baf02d8e6f739c11e019f4e18d0317a47372b802`  
		Last Modified: Fri, 19 Jun 2026 02:10:59 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:012bcc9495430f4516d5308bb6e20ae9b7ea8b94bdaea59d2ab72e84839bcab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084774071601e6a0ae2642841c71471664136714a3a954b32ac2464e5c40865b`

```dockerfile
```

-	Layers:
	-	`sha256:9f4cb30c1725e4d0baad7606e01a9c9a36495634a66b1b174ea5d08eb35e5d4b`  
		Last Modified: Fri, 19 Jun 2026 02:10:57 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.6.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5bbfc206e4b89e7798cddd64d8a04ffd22d286db582c7ad606682b52ed4737f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146114227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975eb110b97983cdfd78076835d60eadbc7725cf10571cfb7def7afc2edc29f1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
# Fri, 19 Jun 2026 02:10:52 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 19 Jun 2026 02:10:53 GMT
USER rootless
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b85916ff55f8ce2c8da67e7772a25474b355a1dd493f214d41d43253d1548b`  
		Last Modified: Fri, 19 Jun 2026 02:11:00 GMT  
		Size: 3.4 MB (3448189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0bc425a243c0c3eeab80b3e48cf1ea6ec21ccd16a312d98af2f927eb121c35`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5446d512f11d6265cce1ca159d2a482006f4877affb531aef47ef80a551bcc8`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6709844d97a0d426c04590edab3343d70dac7258c494d66b8cf6d7be8c3fe6aa`  
		Last Modified: Fri, 19 Jun 2026 02:11:01 GMT  
		Size: 11.2 MB (11237093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee17a95a048e81c0024fe1c7ba0070d5da1d52476f556326583db6ec29ce5e0`  
		Last Modified: Fri, 19 Jun 2026 02:11:01 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.6.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2c45bfb44aa0b61299433e6020d94ac958002fdbcfaaaa025ba91ab1f9c79285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e53d33599a433f08a1651bf641f69073d3a0bdf5afd3d11bb53f9bc8a8a144`

```dockerfile
```

-	Layers:
	-	`sha256:7eb9bc6866e8e0ecd67588973ad4555300490d051e2c2b97238eff97115164f5`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.6.0-windowsservercore`

```console
$ docker pull docker@sha256:33ca0ba2ef616adbccf6ec29dbe41037f05ec7b2ff0591eb8191e2bcea9f2d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `docker:29.6.0-windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:3c679d372ae52d1c28c9ab6ebced51a5fc87a64a25d54affae466fb1ae939e6d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335822962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd42ca38e16fd99dae655e21faf8655cb770ec144d9e7dd79d228f01e3d6a62`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 19 Jun 2026 00:32:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:33:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:33:27 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:33:29 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:33:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:46 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:33:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:33:59 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd84ed1f36f4efc3b209c9830da5ce867308531f8850dee14d52abb78c24ef35`  
		Last Modified: Fri, 19 Jun 2026 00:34:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc70eeb4f52ac6a7a7d7219a5aab349b6d1f40aee83507f35f61f570d6946c0`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 407.0 KB (407033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff31ec88e5ceae0d2116513bb8fac8ebf6f8217a0ff82da620022665db87ace`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a63cc16cd2e92c1ae24ececf097f2aa9b42a34e5f5aaa2856f8fba9f8eba49`  
		Last Modified: Fri, 19 Jun 2026 00:34:15 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c51f0c0352a67c5a6d50ec07cdb8f4c25155da43c6ef50149ba4cd148690e9d`  
		Last Modified: Fri, 19 Jun 2026 00:34:18 GMT  
		Size: 20.2 MB (20164255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d47d97257144bf00e368b0b0e424c30f0e617ba8809da54e09ff0d7510ec2`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f4b710350fc80b3707afebe6c639d0a528fcf63e728e7dc7268c605ec36b4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe83587f120b40642d24d410c04f1fe3b06e9269af6636fe95bc3fe76a4d5f4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa274e151272e3ce6c4f4bef2852f2d7ccd285bc4070a087ee737ab8edb812`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 24.0 MB (23974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce95d86829e5292395cf5c68519a8dbeac2dc78a393c768a3069f74f3320e21`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5901d08fde069f52ef9edb45aa9eec15b39e7d34e50c0096956fee163bf36ba8`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78920a4746cf58101f91230b8c0454dafe8ae966df0bcc9735018718e86f69`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36599a24e8dc3e1d8c2d3f0b9e4484ce5dcaa28688b7016a1298b37d7dcb9d8`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 12.1 MB (12122720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.6.0-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:1ceb80b203fc35f1a449bada44bec0ca9cf59a57d893543b8bf7713b770790b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188772660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528c58692e87fbd65e69ca069cfa499808ef51d4652a2999dd5f0536716a1951`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 19 Jun 2026 00:32:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:34:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:34:02 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:34:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:34:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:24 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:34:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:34:26 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:34:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:34:37 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef8125c4e3ba69e4c1b5648bc9e4c51f4f72cd8f7933f46264e122474c534fb`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14a32fee7fc61f8677fdf1f6aaeecd31ff9e20213d1e59cc1f224fc9db8ba53`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 500.8 KB (500768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a6748886801cffcbd40fc56cd739c7893abb9fe2e3ccde48830cf67c53b8`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54be8eb6ae637d7d441fb62bc41ebcbb203d452885a7549652058b22f099c1bd`  
		Last Modified: Fri, 19 Jun 2026 00:34:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6313b440ac970bf7c9d7042bc1a22e367e4acd507b6893cc0479aa3017641d6`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 20.1 MB (20116805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95422775683da39734a4b00798b9565ca9cbf9cd513769ce5c3e806615e2e661`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601dd0e3e31c052c9c89015191a50d2be09baae731765c3adec0afbf9a0f9317`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1255da46d16e32ef90b88172eb889057ec9d997c2eee79e2419090b2f01baa`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5379064dfc9db6e4b3cf409673d41f43552241f3e1acc5eaefd1bb0124281251`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 23.9 MB (23938202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a376f34b936040b15a1dc7cf7baac58bd29dcb2ac1c56876126b7f972b33df`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d50d2853e68cfa1771416ecd51e8ce0c013503da7627107837e7d626911197f`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e5e5fc4cdaaf27fcbb09bc4cc565a3e45e7a2972417de65cbb139832b77d57`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf0b25cc396df62980d6882d986ced7bfbae4595d5e5f01de0d164e46742b14`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 12.1 MB (12079646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.6.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:10552617643580c1b4a18cb25bcf958d7a793879b1d3d259e868aa1ca69d1084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `docker:29.6.0-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:1ceb80b203fc35f1a449bada44bec0ca9cf59a57d893543b8bf7713b770790b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188772660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528c58692e87fbd65e69ca069cfa499808ef51d4652a2999dd5f0536716a1951`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 19 Jun 2026 00:32:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:34:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:34:02 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:34:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:34:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:24 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:34:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:34:26 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:34:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:34:37 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef8125c4e3ba69e4c1b5648bc9e4c51f4f72cd8f7933f46264e122474c534fb`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14a32fee7fc61f8677fdf1f6aaeecd31ff9e20213d1e59cc1f224fc9db8ba53`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 500.8 KB (500768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a6748886801cffcbd40fc56cd739c7893abb9fe2e3ccde48830cf67c53b8`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54be8eb6ae637d7d441fb62bc41ebcbb203d452885a7549652058b22f099c1bd`  
		Last Modified: Fri, 19 Jun 2026 00:34:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6313b440ac970bf7c9d7042bc1a22e367e4acd507b6893cc0479aa3017641d6`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 20.1 MB (20116805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95422775683da39734a4b00798b9565ca9cbf9cd513769ce5c3e806615e2e661`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601dd0e3e31c052c9c89015191a50d2be09baae731765c3adec0afbf9a0f9317`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1255da46d16e32ef90b88172eb889057ec9d997c2eee79e2419090b2f01baa`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5379064dfc9db6e4b3cf409673d41f43552241f3e1acc5eaefd1bb0124281251`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 23.9 MB (23938202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a376f34b936040b15a1dc7cf7baac58bd29dcb2ac1c56876126b7f972b33df`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d50d2853e68cfa1771416ecd51e8ce0c013503da7627107837e7d626911197f`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e5e5fc4cdaaf27fcbb09bc4cc565a3e45e7a2972417de65cbb139832b77d57`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf0b25cc396df62980d6882d986ced7bfbae4595d5e5f01de0d164e46742b14`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 12.1 MB (12079646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.6.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:72eb56ff73ff4197d65d10e826964030c0c99de084a5a2ed5b70affbda71f964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `docker:29.6.0-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:3c679d372ae52d1c28c9ab6ebced51a5fc87a64a25d54affae466fb1ae939e6d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335822962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd42ca38e16fd99dae655e21faf8655cb770ec144d9e7dd79d228f01e3d6a62`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 19 Jun 2026 00:32:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:33:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:33:27 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:33:29 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:33:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:46 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:33:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:33:59 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd84ed1f36f4efc3b209c9830da5ce867308531f8850dee14d52abb78c24ef35`  
		Last Modified: Fri, 19 Jun 2026 00:34:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc70eeb4f52ac6a7a7d7219a5aab349b6d1f40aee83507f35f61f570d6946c0`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 407.0 KB (407033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff31ec88e5ceae0d2116513bb8fac8ebf6f8217a0ff82da620022665db87ace`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a63cc16cd2e92c1ae24ececf097f2aa9b42a34e5f5aaa2856f8fba9f8eba49`  
		Last Modified: Fri, 19 Jun 2026 00:34:15 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c51f0c0352a67c5a6d50ec07cdb8f4c25155da43c6ef50149ba4cd148690e9d`  
		Last Modified: Fri, 19 Jun 2026 00:34:18 GMT  
		Size: 20.2 MB (20164255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d47d97257144bf00e368b0b0e424c30f0e617ba8809da54e09ff0d7510ec2`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f4b710350fc80b3707afebe6c639d0a528fcf63e728e7dc7268c605ec36b4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe83587f120b40642d24d410c04f1fe3b06e9269af6636fe95bc3fe76a4d5f4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa274e151272e3ce6c4f4bef2852f2d7ccd285bc4070a087ee737ab8edb812`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 24.0 MB (23974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce95d86829e5292395cf5c68519a8dbeac2dc78a393c768a3069f74f3320e21`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5901d08fde069f52ef9edb45aa9eec15b39e7d34e50c0096956fee163bf36ba8`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78920a4746cf58101f91230b8c0454dafe8ae966df0bcc9735018718e86f69`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36599a24e8dc3e1d8c2d3f0b9e4484ce5dcaa28688b7016a1298b37d7dcb9d8`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 12.1 MB (12122720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:d14410ab6f87a2b6c14b7150de787cd7b8bb012a8e900966d6d893e9f7fc49b6
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
$ docker pull docker@sha256:42d38593dbad18fa64c2a537dad24c8f51f62e59d720b6f15dc160f98cdb42ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65891586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8be2f46589d0a8adba646f841902a069a14646b93f77d7cae334cb42a9623f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:97f98e71dfc570d767a3ff2c6f972d9ec17cb7ffda8b66dc5db1504a791d9b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793f972b0ceda58860edaa7f31e806d6017912f8622fed7a0e223d4c56cd3680`

```dockerfile
```

-	Layers:
	-	`sha256:03ed415629b8212b0cf83d1845548e7da5ce9c4c8611b9ccf8b3b5566e3e3373`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:4774f847734c7369a47961ba5ff7cfa19ae126288e34c23e3e3fe90c5ee53429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62171834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5633626af9c8e62669a6cd73148a7156f723d65f5e04ccd8fbe78300c07fdcf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:51d1f73886650d7d6c21902bc42c79247e5862a9438c4fabd2ca2afdb2e68791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325a023e2548630400f3bd6e92794f4fc3ef3a321adcf13711e3cb37f6ff759f`

```dockerfile
```

-	Layers:
	-	`sha256:665fc45e241bfbd951df799d4e519ca5c59e6dfe5c9c40a2adb1bd115f43153a`  
		Last Modified: Fri, 19 Jun 2026 00:30:16 GMT  
		Size: 38.2 KB (38220 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:315e8347dfed436b55039950bc959101914bf9551d0c43da4739cf07a735f1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61130424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a10087f5f0d1068b8b124197c7540818e3cad4825c7e952ed37ad2633b06158`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:f4ce93e0eea54be2ffdc2d6c385552cc3c51c7cf7959a8e639e9d289ad3132f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03441a94ec0257aead90d4c3c8b53a08d7eea8c09226613813074c1cf7737ff8`

```dockerfile
```

-	Layers:
	-	`sha256:a4fb98d917c44326c783d8f2f693ef34cb380191d80fc046966a52acc480cb8e`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fc3958179f7280a4f91830220d8839a3807975f5ac6e6a4423df0748ac8f884a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61522873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b0394024e31d35f42d30c3f31d157cad0169b7b1bc7a4ab33155db987a739f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e8f14ba4dfd7bb9880d48574c63c632841ef2df44a62aced6e86ff27ddd5da52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b5718a9bf51646124ad935e427982a3b74d92485c36c179e2c7d8706e56c85`

```dockerfile
```

-	Layers:
	-	`sha256:badc3ecf86315460f9d2dc4e6cbcd98049e813b2a9765d692ffb50b8e63d0efc`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:7bb861a04bb42bda1d237fc2cb539f9823c9b666ecfbfdbd3e534ab74c8cb976
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
$ docker pull docker@sha256:ac6b53ddb8d0cf0128662faad22917d149c0dc38ea06d19ee77f73aacac785ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142090227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69223e53412298a32a68f53aa962dfd39ed914c741b78d59180d7c58302a217`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:cc89ce54f24170d3e92dc52ddf8d9451830b8093805cc59dfa9947c7650d39a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01538af45e248b6089d3e5d730527b1c41cd13cf7d80910ac9b146f27f82cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:c0ae1d7e8d6d8a75a26ce2b38b3e844ee22f276b95eab267bd0b820df4c919c2`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:ade95fd5db120a8cc651141edd19e1985b5bbbeed68417c4f3cd090086140969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133959761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029fdfd1ee53c34ae022a0e6263fc4789fdb8c35bb1f4f490f16ec3f8b7b331d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b44148ab836c9c91366a663c6061a36ddfe799dd9268e45c41a601b3b1f431`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 7.3 MB (7304119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa72ae8939b6d7f8167771741034d8b3feffafc7dee6187650c48ec4dfb8915`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 90.7 KB (90713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca459390458d8c58ff2e5207edc2bc3e6aa14bb6b22d18ecb09192b7032b5857`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba84346ee44681dc1558263d926ca540e010ed4e6b89bf5ee521a1a395a2e9c`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 64.4 MB (64387101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc367eb5e023ebb9d901cd1bc05761fc3b4c6bbb9a7e35b9dbbb745452f3eb7`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594760236ac59d6bf3223b8cd2eb39e2bf3813283ce6c018becfe64410510763`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a6665de2e94a1021005baef734d74c522104963efdcf1abb8e0db44ae2515047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e070c59d6a4b0856e4c75d176a9a7908a60d248472d355f20775de1e2e1ac0`

```dockerfile
```

-	Layers:
	-	`sha256:f2368fab42b393cf0d466f41e00852b69e7784e59567cd5dbc36fa5ce4ec58af`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:b537631d5f543ab42b7f667a07e998ede31530378bd901880715a8907cf941c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132036739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c193a82ef71fae6ae3b84ad0bca9e3bb8008f600afa5267a0648d544626169c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7602c19d7a228c5890f9e450eb603232eb5a6353adbaa4a15cc06ddff3e402c`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 6.6 MB (6598797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782a5e9a7bdd6d57edb34dd51a5bdfcac3a2b9bd0b00a3e441db3adc72ca2b40`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 87.0 KB (86952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404d95285dee929efa81c5cadcd238b650a375ce35e7d3d0db9a65e86f7ceeb`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f35c2d8cc43ef5a75265b9cdad73b51e18dc52b986d5d19a9311305f72d291`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 64.2 MB (64214561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f581417afe910c2785f1dcdf1ca6903e8dbf88996a6832a0c594ac27343dd`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af0ec459c273b37aa99112ce185577250dab1a2fba2ec4372d78c21012c3a4`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:6ac5495160751363965222768f91a62c33f88b805821f09566c756ea0f89f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709f117ecc9ccc4d044249905af964d3b2383f208e8254b0f8344be92f7ff96`

```dockerfile
```

-	Layers:
	-	`sha256:e3d876ca2a6f22002c6742169913b8b8d2a033be3a0bd77425918a4a8100dc2a`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ba62bab587d68bde5ca081d7b76c0c57583694fea8f4c9b03b4c50b6d0090b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131427605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66576e67cfcbbdbb70a9229bb13f120d3e9bf7019c043ee2a46ed3f988d5dc97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:ec3ebf2c6e55a734c801ca16b683e21f6e542e86f120e587d6891043a3678a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e309b21efb00099c4b0e8117b961199f6c14bf6ad7d333f3f6aa5f22205f6`

```dockerfile
```

-	Layers:
	-	`sha256:17a4da9f797340aba5ff851c456be7c7548b83ea148ddb8f68053270198b1fff`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:d6afe68d2a7648617e95a8f17a8ac59cbc35cc2d8cfe22c40d387e36727386da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d42697e117a63ffb0ca65d43ee4f1d0d40c27a10cb692c830c4c59e3207f88f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157665817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88551c3e8cf1690efd08ab0dcd8d786bfce8a46c19141fb5e0e07672372d3aa5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
# Fri, 19 Jun 2026 02:10:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 19 Jun 2026 02:10:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 19 Jun 2026 02:10:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419e3b36c5c7496ffede1a8cbe30d8067fe2a5882703d9b69bd1ea5b5fc522f8`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 3.5 MB (3470940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2608c2629944dcc1a47baf9e43935062075d2c74c18fe59c2bd5391d889a4182`  
		Last Modified: Fri, 19 Jun 2026 02:10:57 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bb08eaebb42a68ad5c8e1a6bcceeaf94f79064917892f9fad9bdd363b3c201`  
		Last Modified: Fri, 19 Jun 2026 02:10:57 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5954c8a3bab51d96ff16b24c7784de623b3114e06e36081dbca85a35f77fea21`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 12.1 MB (12103310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf559b90eb3bd3c881831664baf02d8e6f739c11e019f4e18d0317a47372b802`  
		Last Modified: Fri, 19 Jun 2026 02:10:59 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:012bcc9495430f4516d5308bb6e20ae9b7ea8b94bdaea59d2ab72e84839bcab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084774071601e6a0ae2642841c71471664136714a3a954b32ac2464e5c40865b`

```dockerfile
```

-	Layers:
	-	`sha256:9f4cb30c1725e4d0baad7606e01a9c9a36495634a66b1b174ea5d08eb35e5d4b`  
		Last Modified: Fri, 19 Jun 2026 02:10:57 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5bbfc206e4b89e7798cddd64d8a04ffd22d286db582c7ad606682b52ed4737f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146114227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975eb110b97983cdfd78076835d60eadbc7725cf10571cfb7def7afc2edc29f1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
# Fri, 19 Jun 2026 02:10:52 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 19 Jun 2026 02:10:52 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 19 Jun 2026 02:10:53 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 19 Jun 2026 02:10:53 GMT
USER rootless
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b85916ff55f8ce2c8da67e7772a25474b355a1dd493f214d41d43253d1548b`  
		Last Modified: Fri, 19 Jun 2026 02:11:00 GMT  
		Size: 3.4 MB (3448189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0bc425a243c0c3eeab80b3e48cf1ea6ec21ccd16a312d98af2f927eb121c35`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5446d512f11d6265cce1ca159d2a482006f4877affb531aef47ef80a551bcc8`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6709844d97a0d426c04590edab3343d70dac7258c494d66b8cf6d7be8c3fe6aa`  
		Last Modified: Fri, 19 Jun 2026 02:11:01 GMT  
		Size: 11.2 MB (11237093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee17a95a048e81c0024fe1c7ba0070d5da1d52476f556326583db6ec29ce5e0`  
		Last Modified: Fri, 19 Jun 2026 02:11:01 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2c45bfb44aa0b61299433e6020d94ac958002fdbcfaaaa025ba91ab1f9c79285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e53d33599a433f08a1651bf641f69073d3a0bdf5afd3d11bb53f9bc8a8a144`

```dockerfile
```

-	Layers:
	-	`sha256:7eb9bc6866e8e0ecd67588973ad4555300490d051e2c2b97238eff97115164f5`  
		Last Modified: Fri, 19 Jun 2026 02:10:58 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:7bb861a04bb42bda1d237fc2cb539f9823c9b666ecfbfdbd3e534ab74c8cb976
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
$ docker pull docker@sha256:ac6b53ddb8d0cf0128662faad22917d149c0dc38ea06d19ee77f73aacac785ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142090227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69223e53412298a32a68f53aa962dfd39ed914c741b78d59180d7c58302a217`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:10:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:10:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:10:24 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:10:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:10:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:10:24 GMT
CMD []
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ae5bd0a6c921476254240cfdb4296617e0f2af6ae29bd75d8d7d0992796403`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 8.2 MB (8170558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8278a40be4305d9eb6b5f1ba9d51d2706ca7afaa7d5095858cb39a9a59a3f160`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 19.4 MB (19439724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d141ee30abedeb696cdd5e29070090e922b7db90b4d86e993de518e7172bd`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 23.0 MB (23036818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56264edbbdea985e1f5c535a75c0844757a024b88319d8be8275ffdaccf6922`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 11.4 MB (11395944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611b2953a04214941dc779e1e373abe13e90a59c9a872853487f8d7a504a51e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c126138ea0de33e3dae588c31f6377b3ac19d22679a2b97159990cacd215a`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4095a2f5aa81c262324453a5e3a2be5606b8aa960f1805cc0b2b805f78060b`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 7.0 MB (6965234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b64570c282ea77be3932cba6645a77a4e7ea10e753645cdd8033006463d59`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 91.3 KB (91319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715caae7f5af6c5fd9df3f15aa36092f0d10302a64b1490c04ef79beaad810f9`  
		Last Modified: Fri, 19 Jun 2026 01:10:35 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369a6a36dceb9dfc4599bcc3f6f7e8976ab8825bbcaeadf686e874a50d022fb3`  
		Last Modified: Fri, 19 Jun 2026 01:10:37 GMT  
		Size: 69.1 MB (69136084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2447670438502396f15fc53806e5a8fa631021a34c91660408e86d4eb35bf688`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ad6ffc815a618d1611dae3cda0ba5a6ee9398e5f33e6029b7a4fe51f10b1`  
		Last Modified: Fri, 19 Jun 2026 01:10:36 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:cc89ce54f24170d3e92dc52ddf8d9451830b8093805cc59dfa9947c7650d39a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01538af45e248b6089d3e5d730527b1c41cd13cf7d80910ac9b146f27f82cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:c0ae1d7e8d6d8a75a26ce2b38b3e844ee22f276b95eab267bd0b820df4c919c2`  
		Last Modified: Fri, 19 Jun 2026 01:10:34 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:ade95fd5db120a8cc651141edd19e1985b5bbbeed68417c4f3cd090086140969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133959761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029fdfd1ee53c34ae022a0e6263fc4789fdb8c35bb1f4f490f16ec3f8b7b331d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:10 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:32 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:32 GMT
CMD []
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029b1fe72dc7cce24acf2682ceebab3dbf2ab73951fb8bdf67596ba5fcba197`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 8.1 MB (8070164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cc7d1bbae9ec3abf96977858bdbe848622e8d5be980062ea7862eabba2feeb`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 18.1 MB (18080663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780502d4c89e9f452302262c44d6714daa2fb0d71c06d3f79b390e4dddb456`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 21.7 MB (21652838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016a0d13c9c49f1125b986941e1abfdc162301cd7f4b02862bd3e408c53c957`  
		Last Modified: Fri, 19 Jun 2026 00:30:17 GMT  
		Size: 10.8 MB (10812568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db3a315f73b25d3a5d7b0380ee14a03b0ee2840c02f75165a76574b301fdd83`  
		Last Modified: Fri, 19 Jun 2026 00:30:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3602716d8600ce0112d07456ed48af3f46501db699cf1003e9b17878018e3`  
		Last Modified: Fri, 19 Jun 2026 00:30:19 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6ed179d6553964051ab13c0043428f4dc9a463edfd83c0097f2b145e3ac03`  
		Last Modified: Fri, 19 Jun 2026 00:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b44148ab836c9c91366a663c6061a36ddfe799dd9268e45c41a601b3b1f431`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 7.3 MB (7304119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa72ae8939b6d7f8167771741034d8b3feffafc7dee6187650c48ec4dfb8915`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 90.7 KB (90713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca459390458d8c58ff2e5207edc2bc3e6aa14bb6b22d18ecb09192b7032b5857`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba84346ee44681dc1558263d926ca540e010ed4e6b89bf5ee521a1a395a2e9c`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 64.4 MB (64387101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc367eb5e023ebb9d901cd1bc05761fc3b4c6bbb9a7e35b9dbbb745452f3eb7`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594760236ac59d6bf3223b8cd2eb39e2bf3813283ce6c018becfe64410510763`  
		Last Modified: Fri, 19 Jun 2026 01:09:44 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a6665de2e94a1021005baef734d74c522104963efdcf1abb8e0db44ae2515047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e070c59d6a4b0856e4c75d176a9a7908a60d248472d355f20775de1e2e1ac0`

```dockerfile
```

-	Layers:
	-	`sha256:f2368fab42b393cf0d466f41e00852b69e7784e59567cd5dbc36fa5ce4ec58af`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:b537631d5f543ab42b7f667a07e998ede31530378bd901880715a8907cf941c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132036739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c193a82ef71fae6ae3b84ad0bca9e3bb8008f600afa5267a0648d544626169c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:08 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:12 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:15 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:17 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:30 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:30 GMT
CMD []
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a3465f6915e8ba16eeb8f68c59e839bb149be17d0d409e0528ed23f659190`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 7.4 MB (7371180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0780dfc65dfb4eb5b8d3227311d7f0bb6ac297b251ec0271bbf555ab39b2fad`  
		Last Modified: Fri, 19 Jun 2026 00:30:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620d0d0a24b5ba0a04d8342c27580cc370d436c3025fa91eb092348e5534be64`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 18.1 MB (18060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e1cb884cbe153cfac7fc52dab6469562c3ced84d7954f3f2e7164eb444d9b6`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 21.6 MB (21635981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc67309ab87ac42c9b83a7fd87fe9b3c530eb1ee7d79a2db3d2aff01cee4156`  
		Last Modified: Fri, 19 Jun 2026 00:30:24 GMT  
		Size: 10.8 MB (10799586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79e0ed46b8e7697e6e0ac355541e3bac352cf7cf80c5c3360b2bf8d136fc28`  
		Last Modified: Fri, 19 Jun 2026 00:30:25 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee671ed109f9d4c1219e1a17ab925b50895bc3f4aa74f8401b642841a0bcc1a`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7beabd8b363018cba1ee6333b82feeaefc4c13407f1577a7a6fbcc496ff8c03`  
		Last Modified: Fri, 19 Jun 2026 00:30:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7602c19d7a228c5890f9e450eb603232eb5a6353adbaa4a15cc06ddff3e402c`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 6.6 MB (6598797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782a5e9a7bdd6d57edb34dd51a5bdfcac3a2b9bd0b00a3e441db3adc72ca2b40`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 87.0 KB (86952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404d95285dee929efa81c5cadcd238b650a375ce35e7d3d0db9a65e86f7ceeb`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f35c2d8cc43ef5a75265b9cdad73b51e18dc52b986d5d19a9311305f72d291`  
		Last Modified: Fri, 19 Jun 2026 01:09:43 GMT  
		Size: 64.2 MB (64214561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f581417afe910c2785f1dcdf1ca6903e8dbf88996a6832a0c594ac27343dd`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af0ec459c273b37aa99112ce185577250dab1a2fba2ec4372d78c21012c3a4`  
		Last Modified: Fri, 19 Jun 2026 01:09:42 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:6ac5495160751363965222768f91a62c33f88b805821f09566c756ea0f89f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709f117ecc9ccc4d044249905af964d3b2383f208e8254b0f8344be92f7ff96`

```dockerfile
```

-	Layers:
	-	`sha256:e3d876ca2a6f22002c6742169913b8b8d2a033be3a0bd77425918a4a8100dc2a`  
		Last Modified: Fri, 19 Jun 2026 01:09:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ba62bab587d68bde5ca081d7b76c0c57583694fea8f4c9b03b4c50b6d0090b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131427605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66576e67cfcbbdbb70a9229bb13f120d3e9bf7019c043ee2a46ed3f988d5dc97`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 00:30:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jun 2026 00:30:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:30:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jun 2026 00:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-amd64'; 			sha256='d41ece72044243b4f58b343441ae37446d9c29a7d6b5e11c61847bbcf8f7dfda'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v6'; 			sha256='5938b81dc6203361bb984e961fc0afbcdc2bf05c5a666ec093ea99e612de616c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm-v7'; 			sha256='e1fe67cbe2d5a7b242e5f732a9708e6abaa6d19d717e65bfbd1d13baa8669d1f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-arm64'; 			sha256='c4248d6cbc4a619a7e0b4609c11e509ad4ac0b475e1c64817c0ac20c5d90c766'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-ppc64le'; 			sha256='bcee77464deb25cfd0b905d4d871b0aad1b1164d6bcdf8b2fd8b1adb1db021c3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-riscv64'; 			sha256='3ecaf173eb24402ba29e9d3b7ddac4bde259a3a54e98112077014918ab49f61f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.linux-s390x'; 			sha256='ef1738f3c70166e968d1bca3f853dbc515a3aa7ffa82f1a2ded033a050cd3203'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jun 2026 00:30:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jun 2026 00:30:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jun 2026 00:30:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jun 2026 00:30:05 GMT
CMD ["sh"]
# Fri, 19 Jun 2026 01:09:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jun 2026 01:09:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.6.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.6.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.6.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.6.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 19 Jun 2026 01:09:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jun 2026 01:09:47 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jun 2026 01:09:47 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jun 2026 01:09:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jun 2026 01:09:47 GMT
CMD []
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6386612f54119019de0a89795a8e08c36539365f437d02ebb907ce72436a7a4`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 8.2 MB (8231708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcd07e2bf846f5a6f0c2e08c728a59b9cf135260d45ab69d9865ae9381a76`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4e6e16ae213651776663ce346b57e0f895565cfeaaa2f8283b6d0da433101`  
		Last Modified: Fri, 19 Jun 2026 00:30:11 GMT  
		Size: 17.9 MB (17889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3553c76df18c8290e83d4fe56d43d1ca12a49205fa6ea95958d762b5c5f9d1`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 20.9 MB (20856370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7b4f8b29dc7f5be108583f5957aa151cfa059411f452a13279121b412ac0e`  
		Last Modified: Fri, 19 Jun 2026 00:30:12 GMT  
		Size: 10.4 MB (10359863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f8f269035fe9b0102402efd0a5c0f5065ce5d2d059131251064cfce07265e`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9a8e6446a2f03ee07e256257e0e2aa8a4daf04c19b45867747ed89383490d`  
		Last Modified: Fri, 19 Jun 2026 00:30:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9bf0b503b32729fb5c8f470f90a6a33fdf5b071ff2e201ce714a1e0542becd`  
		Last Modified: Fri, 19 Jun 2026 00:30:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a61d94c39ad4a53f7f77437daf48a15ba3b6e67dc975d196489d5acfa7a5dc`  
		Last Modified: Fri, 19 Jun 2026 01:09:57 GMT  
		Size: 7.2 MB (7239997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9473cdcebfd9742a139968eb182e216b2dc92f61464ecfbb99385da6efc7e0b`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 99.9 KB (99933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ad3a90f17838bbdea1587e387e3d86af24fd2548d95010dd88ed623bf2e01`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732858dc7176ddaf464663ed70c8d1dd414f220af7f12dcfd9ea3f956be61c43`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 62.6 MB (62558807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec08e10f36f77aecfdae84e108128f662fa17dcadc828799e03dc5507ef7e7`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58d537de061c3cbf00e4b218e562eb3a0216165be87ef205e9ed66eb02de521`  
		Last Modified: Fri, 19 Jun 2026 01:09:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:ec3ebf2c6e55a734c801ca16b683e21f6e542e86f120e587d6891043a3678a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e309b21efb00099c4b0e8117b961199f6c14bf6ad7d333f3f6aa5f22205f6`

```dockerfile
```

-	Layers:
	-	`sha256:17a4da9f797340aba5ff851c456be7c7548b83ea148ddb8f68053270198b1fff`  
		Last Modified: Fri, 19 Jun 2026 01:09:56 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:33ca0ba2ef616adbccf6ec29dbe41037f05ec7b2ff0591eb8191e2bcea9f2d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:3c679d372ae52d1c28c9ab6ebced51a5fc87a64a25d54affae466fb1ae939e6d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335822962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd42ca38e16fd99dae655e21faf8655cb770ec144d9e7dd79d228f01e3d6a62`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 19 Jun 2026 00:32:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:33:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:33:27 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:33:29 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:33:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:46 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:33:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:33:59 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd84ed1f36f4efc3b209c9830da5ce867308531f8850dee14d52abb78c24ef35`  
		Last Modified: Fri, 19 Jun 2026 00:34:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc70eeb4f52ac6a7a7d7219a5aab349b6d1f40aee83507f35f61f570d6946c0`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 407.0 KB (407033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff31ec88e5ceae0d2116513bb8fac8ebf6f8217a0ff82da620022665db87ace`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a63cc16cd2e92c1ae24ececf097f2aa9b42a34e5f5aaa2856f8fba9f8eba49`  
		Last Modified: Fri, 19 Jun 2026 00:34:15 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c51f0c0352a67c5a6d50ec07cdb8f4c25155da43c6ef50149ba4cd148690e9d`  
		Last Modified: Fri, 19 Jun 2026 00:34:18 GMT  
		Size: 20.2 MB (20164255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d47d97257144bf00e368b0b0e424c30f0e617ba8809da54e09ff0d7510ec2`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f4b710350fc80b3707afebe6c639d0a528fcf63e728e7dc7268c605ec36b4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe83587f120b40642d24d410c04f1fe3b06e9269af6636fe95bc3fe76a4d5f4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa274e151272e3ce6c4f4bef2852f2d7ccd285bc4070a087ee737ab8edb812`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 24.0 MB (23974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce95d86829e5292395cf5c68519a8dbeac2dc78a393c768a3069f74f3320e21`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5901d08fde069f52ef9edb45aa9eec15b39e7d34e50c0096956fee163bf36ba8`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78920a4746cf58101f91230b8c0454dafe8ae966df0bcc9735018718e86f69`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36599a24e8dc3e1d8c2d3f0b9e4484ce5dcaa28688b7016a1298b37d7dcb9d8`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 12.1 MB (12122720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:1ceb80b203fc35f1a449bada44bec0ca9cf59a57d893543b8bf7713b770790b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188772660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528c58692e87fbd65e69ca069cfa499808ef51d4652a2999dd5f0536716a1951`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 19 Jun 2026 00:32:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:34:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:34:02 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:34:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:34:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:24 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:34:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:34:26 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:34:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:34:37 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef8125c4e3ba69e4c1b5648bc9e4c51f4f72cd8f7933f46264e122474c534fb`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14a32fee7fc61f8677fdf1f6aaeecd31ff9e20213d1e59cc1f224fc9db8ba53`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 500.8 KB (500768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a6748886801cffcbd40fc56cd739c7893abb9fe2e3ccde48830cf67c53b8`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54be8eb6ae637d7d441fb62bc41ebcbb203d452885a7549652058b22f099c1bd`  
		Last Modified: Fri, 19 Jun 2026 00:34:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6313b440ac970bf7c9d7042bc1a22e367e4acd507b6893cc0479aa3017641d6`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 20.1 MB (20116805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95422775683da39734a4b00798b9565ca9cbf9cd513769ce5c3e806615e2e661`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601dd0e3e31c052c9c89015191a50d2be09baae731765c3adec0afbf9a0f9317`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1255da46d16e32ef90b88172eb889057ec9d997c2eee79e2419090b2f01baa`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5379064dfc9db6e4b3cf409673d41f43552241f3e1acc5eaefd1bb0124281251`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 23.9 MB (23938202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a376f34b936040b15a1dc7cf7baac58bd29dcb2ac1c56876126b7f972b33df`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d50d2853e68cfa1771416ecd51e8ce0c013503da7627107837e7d626911197f`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e5e5fc4cdaaf27fcbb09bc4cc565a3e45e7a2972417de65cbb139832b77d57`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf0b25cc396df62980d6882d986ced7bfbae4595d5e5f01de0d164e46742b14`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 12.1 MB (12079646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:10552617643580c1b4a18cb25bcf958d7a793879b1d3d259e868aa1ca69d1084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull docker@sha256:1ceb80b203fc35f1a449bada44bec0ca9cf59a57d893543b8bf7713b770790b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2188772660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528c58692e87fbd65e69ca069cfa499808ef51d4652a2999dd5f0536716a1951`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 19 Jun 2026 00:32:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:34:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:34:02 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:34:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:34:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:24 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:34:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:34:26 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:34:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:34:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:34:37 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef8125c4e3ba69e4c1b5648bc9e4c51f4f72cd8f7933f46264e122474c534fb`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14a32fee7fc61f8677fdf1f6aaeecd31ff9e20213d1e59cc1f224fc9db8ba53`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 500.8 KB (500768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a6748886801cffcbd40fc56cd739c7893abb9fe2e3ccde48830cf67c53b8`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54be8eb6ae637d7d441fb62bc41ebcbb203d452885a7549652058b22f099c1bd`  
		Last Modified: Fri, 19 Jun 2026 00:34:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6313b440ac970bf7c9d7042bc1a22e367e4acd507b6893cc0479aa3017641d6`  
		Last Modified: Fri, 19 Jun 2026 00:35:00 GMT  
		Size: 20.1 MB (20116805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95422775683da39734a4b00798b9565ca9cbf9cd513769ce5c3e806615e2e661`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601dd0e3e31c052c9c89015191a50d2be09baae731765c3adec0afbf9a0f9317`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1255da46d16e32ef90b88172eb889057ec9d997c2eee79e2419090b2f01baa`  
		Last Modified: Fri, 19 Jun 2026 00:34:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5379064dfc9db6e4b3cf409673d41f43552241f3e1acc5eaefd1bb0124281251`  
		Last Modified: Fri, 19 Jun 2026 00:34:59 GMT  
		Size: 23.9 MB (23938202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a376f34b936040b15a1dc7cf7baac58bd29dcb2ac1c56876126b7f972b33df`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d50d2853e68cfa1771416ecd51e8ce0c013503da7627107837e7d626911197f`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e5e5fc4cdaaf27fcbb09bc4cc565a3e45e7a2972417de65cbb139832b77d57`  
		Last Modified: Fri, 19 Jun 2026 00:34:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf0b25cc396df62980d6882d986ced7bfbae4595d5e5f01de0d164e46742b14`  
		Last Modified: Fri, 19 Jun 2026 00:34:57 GMT  
		Size: 12.1 MB (12079646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:72eb56ff73ff4197d65d10e826964030c0c99de084a5a2ed5b70affbda71f964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull docker@sha256:3c679d372ae52d1c28c9ab6ebced51a5fc87a64a25d54affae466fb1ae939e6d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335822962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd42ca38e16fd99dae655e21faf8655cb770ec144d9e7dd79d228f01e3d6a62`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 19 Jun 2026 00:32:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 19 Jun 2026 00:33:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 19 Jun 2026 00:33:27 GMT
ENV DOCKER_VERSION=29.6.0
# Fri, 19 Jun 2026 00:33:29 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.6.0.zip
# Fri, 19 Jun 2026 00:33:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:46 GMT
ENV DOCKER_BUILDX_VERSION=0.35.0
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.35.0/buildx-v0.35.0.windows-amd64.exe
# Fri, 19 Jun 2026 00:33:47 GMT
ENV DOCKER_BUILDX_SHA256=8076395009787cd1d30c94edeb5d7ac3945273374fc162c00e9810c3e9325ebe
# Fri, 19 Jun 2026 00:33:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Fri, 19 Jun 2026 00:33:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Fri, 19 Jun 2026 00:33:59 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Fri, 19 Jun 2026 00:34:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd84ed1f36f4efc3b209c9830da5ce867308531f8850dee14d52abb78c24ef35`  
		Last Modified: Fri, 19 Jun 2026 00:34:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc70eeb4f52ac6a7a7d7219a5aab349b6d1f40aee83507f35f61f570d6946c0`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 407.0 KB (407033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff31ec88e5ceae0d2116513bb8fac8ebf6f8217a0ff82da620022665db87ace`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a63cc16cd2e92c1ae24ececf097f2aa9b42a34e5f5aaa2856f8fba9f8eba49`  
		Last Modified: Fri, 19 Jun 2026 00:34:15 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c51f0c0352a67c5a6d50ec07cdb8f4c25155da43c6ef50149ba4cd148690e9d`  
		Last Modified: Fri, 19 Jun 2026 00:34:18 GMT  
		Size: 20.2 MB (20164255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d47d97257144bf00e368b0b0e424c30f0e617ba8809da54e09ff0d7510ec2`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f4b710350fc80b3707afebe6c639d0a528fcf63e728e7dc7268c605ec36b4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe83587f120b40642d24d410c04f1fe3b06e9269af6636fe95bc3fe76a4d5f4`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa274e151272e3ce6c4f4bef2852f2d7ccd285bc4070a087ee737ab8edb812`  
		Last Modified: Fri, 19 Jun 2026 00:34:16 GMT  
		Size: 24.0 MB (23974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce95d86829e5292395cf5c68519a8dbeac2dc78a393c768a3069f74f3320e21`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5901d08fde069f52ef9edb45aa9eec15b39e7d34e50c0096956fee163bf36ba8`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78920a4746cf58101f91230b8c0454dafe8ae966df0bcc9735018718e86f69`  
		Last Modified: Fri, 19 Jun 2026 00:34:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36599a24e8dc3e1d8c2d3f0b9e4484ce5dcaa28688b7016a1298b37d7dcb9d8`  
		Last Modified: Fri, 19 Jun 2026 00:34:14 GMT  
		Size: 12.1 MB (12122720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

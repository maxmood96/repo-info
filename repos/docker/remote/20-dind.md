## `docker:20-dind`

```console
$ docker pull docker@sha256:3fd7eaed284a881a8ca2b254fb56047a3f100a44ecbb8c3d6f3521cd981db828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:7abbf564024e76ee5fc2b055b2a0790db660080bf35a7f827739df76c5622044
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108394154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5daac9489dc300a47bcb0ea96855ff17e5353aaab9065dbe19b890f480626683`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:19:24 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Thu, 06 Oct 2022 20:19:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 26 Oct 2022 06:52:17 GMT
ENV DOCKER_VERSION=20.10.21
# Wed, 26 Oct 2022 06:52:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.21.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.21.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.21.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.21.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Wed, 26 Oct 2022 06:52:22 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Wed, 26 Oct 2022 06:52:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Wed, 26 Oct 2022 06:52:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.12.2
# Wed, 26 Oct 2022 06:52:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-x86_64'; 			sha256='36d1728ce001c7f021294be43bdfa3f508038bb00886c34b0794f7731cc9bf4b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-armv6'; 			sha256='e384beeb08ca89e4aeae5c47c561c5d49905e170d453e59440252015833183af'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-armv7'; 			sha256='22cfe5b2eab86a4832f328049cafacc8e7d76c12185ea7bdff7e7c7ce42f5f10'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-aarch64'; 			sha256='a2c9819115df18ada4e6a68be37f6515121984189d379456bdfd53058e07128b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-ppc64le'; 			sha256='155df9a23b30011ca5318ee4b2df436938c8cebe03d78c9b349998d1bec9ca79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-riscv64'; 			sha256='e6903410dbf2d8705dbc9984cbf235306c4f85f7dd84b21bc4ed042b6fed4667'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-s390x'; 			sha256='b318a46c768efcc2a5344a859c9dd9b969e5aa0967af0454dd50152e307a3dc3'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 26 Oct 2022 06:52:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 26 Oct 2022 06:52:26 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 26 Oct 2022 06:52:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Oct 2022 06:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 26 Oct 2022 06:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 06:52:27 GMT
CMD ["sh"]
# Wed, 26 Oct 2022 06:52:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 26 Oct 2022 06:52:34 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 26 Oct 2022 06:52:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.21.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.21.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.21.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.21.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Wed, 26 Oct 2022 06:52:40 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 26 Oct 2022 06:52:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 26 Oct 2022 06:52:41 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 26 Oct 2022 06:52:41 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Oct 2022 06:52:41 GMT
EXPOSE 2375 2376
# Wed, 26 Oct 2022 06:52:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Oct 2022 06:52:41 GMT
CMD []
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0dd730a5c3e0f2ca69ebcd573f312df80344d4349d3cdfc40bdc75c406b44d`  
		Last Modified: Thu, 06 Oct 2022 20:21:25 GMT  
		Size: 2.0 MB (2036059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b90f8029a368ccb8e58eae4ebf51ea850e9116df1d92a8e8687a6902c01e69f`  
		Last Modified: Thu, 06 Oct 2022 20:21:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89466c712af9ab8a7abdd90a1855026b236763417363050776d8b759fe3964b`  
		Last Modified: Wed, 26 Oct 2022 06:53:45 GMT  
		Size: 14.0 MB (13983070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6a0a734fa9e967ad4fcce18686a936d533e0dc1589098834c099d585cc61f5`  
		Last Modified: Wed, 26 Oct 2022 06:53:43 GMT  
		Size: 15.2 MB (15204071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beeedf2bf9bb418db005446933330724754a8d9fbf00c647e8542ed66e319be5`  
		Last Modified: Wed, 26 Oct 2022 06:53:43 GMT  
		Size: 14.5 MB (14480779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc3016a91231dd848bfd60343267c98ca9cf384592115d15e58fd6d329db17b`  
		Last Modified: Wed, 26 Oct 2022 06:53:41 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d4345031563663d73d682b529231cc4ec411043fc8031a22c4a2d013192eba`  
		Last Modified: Wed, 26 Oct 2022 06:53:40 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539e1dfa39931c56aa5eeb10acbc0573659d8a17841e8d64bc957d9ec94c259f`  
		Last Modified: Wed, 26 Oct 2022 06:53:40 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0219f7532a8e74e32a1676579f832e53bbac918c55e6eac133f9e23949fba49a`  
		Last Modified: Wed, 26 Oct 2022 06:54:18 GMT  
		Size: 6.9 MB (6863661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190a2fb84408684acc0703ccb3f1c47a0789e6dbcbf370d1804e52acff142cc5`  
		Last Modified: Wed, 26 Oct 2022 06:54:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa203f981c78023ab643c66c72547933cd61117b41ac6b025b36767244b28fa1`  
		Last Modified: Wed, 26 Oct 2022 06:54:28 GMT  
		Size: 53.0 MB (53013554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616ae5a1587823a83d7fd6878543874cafe281db358c5581b52a057ba9eeedd4`  
		Last Modified: Wed, 26 Oct 2022 06:54:17 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d41681601ca19265af75c4bd23dacb2379bcf874b116b269a0581fcdace5005`  
		Last Modified: Wed, 26 Oct 2022 06:54:17 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:12f02a5b5af3a7923b260fa6e0de307448f8b7e583f7af6d76b6acd22660270a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99562504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17d318d1a31c21ceb3f7f07297076de6f37a8fba715bf905d55aad190dce295`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 00:28:46 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 25 Oct 2022 00:28:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 25 Oct 2022 00:29:22 GMT
ENV DOCKER_VERSION=20.10.20
# Tue, 25 Oct 2022 00:29:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.20.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.20.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.20.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.20.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 25 Oct 2022 00:29:25 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Tue, 25 Oct 2022 00:29:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Tue, 25 Oct 2022 00:29:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.12.2
# Tue, 25 Oct 2022 00:29:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-x86_64'; 			sha256='36d1728ce001c7f021294be43bdfa3f508038bb00886c34b0794f7731cc9bf4b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-armv6'; 			sha256='e384beeb08ca89e4aeae5c47c561c5d49905e170d453e59440252015833183af'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-armv7'; 			sha256='22cfe5b2eab86a4832f328049cafacc8e7d76c12185ea7bdff7e7c7ce42f5f10'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-aarch64'; 			sha256='a2c9819115df18ada4e6a68be37f6515121984189d379456bdfd53058e07128b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-ppc64le'; 			sha256='155df9a23b30011ca5318ee4b2df436938c8cebe03d78c9b349998d1bec9ca79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-riscv64'; 			sha256='e6903410dbf2d8705dbc9984cbf235306c4f85f7dd84b21bc4ed042b6fed4667'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-s390x'; 			sha256='b318a46c768efcc2a5344a859c9dd9b969e5aa0967af0454dd50152e307a3dc3'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 25 Oct 2022 00:29:28 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 25 Oct 2022 00:29:28 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 25 Oct 2022 00:29:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Oct 2022 00:29:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 25 Oct 2022 00:29:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 00:29:29 GMT
CMD ["sh"]
# Tue, 25 Oct 2022 00:29:34 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 25 Oct 2022 00:29:35 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 25 Oct 2022 00:29:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.20.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.20.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.20.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.20.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Tue, 25 Oct 2022 00:29:39 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 25 Oct 2022 00:29:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 25 Oct 2022 00:29:39 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 25 Oct 2022 00:29:39 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Oct 2022 00:29:39 GMT
EXPOSE 2375 2376
# Tue, 25 Oct 2022 00:29:40 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Oct 2022 00:29:40 GMT
CMD []
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5833820420a0776b323417da6527ee1ed41947060ce2b721ee3dbdb5c828cf1`  
		Last Modified: Tue, 25 Oct 2022 00:30:35 GMT  
		Size: 2.0 MB (2010755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79069699b8305641a125c0409ad7decf0f1b775c9d2e6d13a4f388895271ae15`  
		Last Modified: Tue, 25 Oct 2022 00:30:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee9c3c3cf30ff6876edc42c4d3e102f6e619624678d1901bdccb58cbd424389`  
		Last Modified: Tue, 25 Oct 2022 00:32:02 GMT  
		Size: 12.7 MB (12739253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d61bd8b9f59e427e79d99f9602c02e639b1636ad63f4cfb4a7b799e97af305`  
		Last Modified: Tue, 25 Oct 2022 00:32:00 GMT  
		Size: 13.8 MB (13764593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245f2ec60f2d667a2dd09801bef8ee5568952a3d4abe329d5cc5f73270570ca5`  
		Last Modified: Tue, 25 Oct 2022 00:32:00 GMT  
		Size: 13.1 MB (13077299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565435f1ea6065f0b16a9166d5e5205569b47f830359e0a5532558149f8214ad`  
		Last Modified: Tue, 25 Oct 2022 00:31:58 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b0e4f6483b4434f6b9807a9e6121205eaf6d9083d978433901f077df69825e`  
		Last Modified: Tue, 25 Oct 2022 00:31:58 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ebfe41273f4c8ed8c3e89e706e99608dc04d1f07e56de95c669dbf0c50e5b`  
		Last Modified: Tue, 25 Oct 2022 00:31:58 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3187e7bf89ab83a2c3d839dd3ec28377627cfae77330874ef87b32bc8b3999`  
		Last Modified: Tue, 25 Oct 2022 00:32:34 GMT  
		Size: 6.7 MB (6736752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef872ef773d177baed42803456d7843bf2f24efe1c05d0d044e6b15fa312e3a7`  
		Last Modified: Tue, 25 Oct 2022 00:32:33 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1174b7276f0ab95fda4303295e1efeba66e1ae7028d997c2fd3c98350aff4b31`  
		Last Modified: Tue, 25 Oct 2022 00:32:39 GMT  
		Size: 48.5 MB (48519283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27614098e06bedb9993aea4bb74a7b3c95af2d9a0a5f47668f8c06fe8317b10d`  
		Last Modified: Tue, 25 Oct 2022 00:32:33 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0221342c6159d0e5201c40aacde15886f656a385d972949e872dd10218006f72`  
		Last Modified: Tue, 25 Oct 2022 00:32:33 GMT  
		Size: 2.8 KB (2750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

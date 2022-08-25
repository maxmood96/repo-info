## `docker:rc`

```console
$ docker pull docker@sha256:e068dd2d61b7ac8a71bbb4b948c4c0362e4c181f7e735131c46adb3897ffe5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc` - linux; amd64

```console
$ docker pull docker@sha256:3b20953b2a4ce0155c1baf7acf46f3ecbcd7c8f502bd018fe28b88962aa65a20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98313155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcc5c7ba77b374f6cc5b2c6d3f3404287f50bdc59ad0e9aed3289f678df4889`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 09 Aug 2022 18:20:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:20:49 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Tue, 09 Aug 2022 18:20:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 19 Aug 2022 00:19:27 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Fri, 19 Aug 2022 00:19:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Wed, 24 Aug 2022 23:17:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.10.1
# Wed, 24 Aug 2022 23:17:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-x86_64'; 			sha256='dfe2e3f134cc053e020891a11c23a0923eb49ee35556ec40b37d098eaa5a55f6'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-armv6'; 			sha256='8f9e1ccf35763b292443112795418b3ec9e8df46f8d78ca2c92d44645a90b88f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-armv7'; 			sha256='4a1bd3d72ff2d21248f5e1a32cdabc81aca9d613ce0eee661ac3cb6815db1258'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-aarch64'; 			sha256='2598b299693d3ef6087a8faa02e91e29bc2f4515347a0cf4c9ea18967584f153'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-ppc64le'; 			sha256='4866a6df1bc35eda103b0d32b357e2da4aae0b4eff96dd19ea4c1d6ddbc43e9f'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-riscv64'; 			sha256='8211dc32f228ac6d8685c2d07f579654771af3e792ebc6cc8a212536229630c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-s390x'; 			sha256='56b70071f7ab4acf7387cb3ce8492ec084650b435a2f483d355931bfa5536496'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 24 Aug 2022 23:17:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 24 Aug 2022 23:17:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 24 Aug 2022 23:17:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 24 Aug 2022 23:17:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 24 Aug 2022 23:17:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Aug 2022 23:17:14 GMT
CMD ["sh"]
# Wed, 24 Aug 2022 23:17:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 24 Aug 2022 23:17:19 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 24 Aug 2022 23:17:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Wed, 24 Aug 2022 23:17:25 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 24 Aug 2022 23:17:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 24 Aug 2022 23:17:26 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 24 Aug 2022 23:17:26 GMT
VOLUME [/var/lib/docker]
# Wed, 24 Aug 2022 23:17:26 GMT
EXPOSE 2375 2376
# Wed, 24 Aug 2022 23:17:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 24 Aug 2022 23:17:26 GMT
CMD []
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb510456a427665c9755e7417ad432e68b6e95a1a9a6665f72f0adc6f9ec59d`  
		Last Modified: Tue, 09 Aug 2022 18:22:44 GMT  
		Size: 2.0 MB (2036045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4627ba0696d0614a94c97a4b5c212e055112e2a8f0831f342f3b138955035153`  
		Last Modified: Tue, 09 Aug 2022 18:22:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d957832b8a49136f6d95f00340a0c764c8cd051be7514885f8fca6a80053215`  
		Last Modified: Tue, 09 Aug 2022 18:22:45 GMT  
		Size: 8.7 MB (8706435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd48969715b862016850752e05193de3fe3dbc355a5f277cece7c52d69f4793`  
		Last Modified: Fri, 19 Aug 2022 00:21:18 GMT  
		Size: 15.2 MB (15204103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b457a3085999b1f501d0ed7b62e86a90d0b41563715f55c0189ff8da5c007b`  
		Last Modified: Wed, 24 Aug 2022 23:18:55 GMT  
		Size: 9.4 MB (9351261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ec4ab43f121c4c4e549d22fddada81a818a1cbac485f30587df7bdef77cee6`  
		Last Modified: Wed, 24 Aug 2022 23:18:53 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd175e05748624b79db41ddd232e7b6d47c0fcdebb51b1c188dae04a77e8d7d0`  
		Last Modified: Wed, 24 Aug 2022 23:18:53 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cce2b1610321ba2cb3bfb55feaf77a750e23a26bdfcc16eee4b21c1df6e901`  
		Last Modified: Wed, 24 Aug 2022 23:18:53 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0641c5ae66348051ac5fd22ef429cb3c2e52916fce6a42afac9cf8e55334df1a`  
		Last Modified: Wed, 24 Aug 2022 23:19:10 GMT  
		Size: 6.9 MB (6863615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f8c17926cb95e79e4a21437acdbf0e0cdf0738998fdfa1c249bb0c9a3c16bf`  
		Last Modified: Wed, 24 Aug 2022 23:19:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c4ad063314f0721fa2b4cfefc819b3608072acd5bd4ff803cc073dbfdf4d06`  
		Last Modified: Wed, 24 Aug 2022 23:19:17 GMT  
		Size: 53.3 MB (53338718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca501239be501453f1b283f720d226c9506e02b5a4a28fdea81a62cb8d58146`  
		Last Modified: Wed, 24 Aug 2022 23:19:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5650d9cfd8cb4256fd0bab427e756846dffd3249ea0d64919a9de286a096b05`  
		Last Modified: Wed, 24 Aug 2022 23:19:09 GMT  
		Size: 2.8 KB (2756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3af7c627212f2fb85d7be0bed949869bc3fa3c3d874dcd693e74f1b72ee77f2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90820577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95b8864c4a646920435934c54f1df3879d6c35c6d709c4a25860a37448b8701`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:24:48 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 09 Aug 2022 18:24:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:24:50 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Tue, 09 Aug 2022 18:24:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 19 Aug 2022 02:45:35 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Fri, 19 Aug 2022 02:45:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Thu, 25 Aug 2022 01:50:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.10.1
# Thu, 25 Aug 2022 01:50:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-x86_64'; 			sha256='dfe2e3f134cc053e020891a11c23a0923eb49ee35556ec40b37d098eaa5a55f6'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-armv6'; 			sha256='8f9e1ccf35763b292443112795418b3ec9e8df46f8d78ca2c92d44645a90b88f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-armv7'; 			sha256='4a1bd3d72ff2d21248f5e1a32cdabc81aca9d613ce0eee661ac3cb6815db1258'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-aarch64'; 			sha256='2598b299693d3ef6087a8faa02e91e29bc2f4515347a0cf4c9ea18967584f153'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-ppc64le'; 			sha256='4866a6df1bc35eda103b0d32b357e2da4aae0b4eff96dd19ea4c1d6ddbc43e9f'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-riscv64'; 			sha256='8211dc32f228ac6d8685c2d07f579654771af3e792ebc6cc8a212536229630c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.10.1/docker-compose-linux-s390x'; 			sha256='56b70071f7ab4acf7387cb3ce8492ec084650b435a2f483d355931bfa5536496'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Thu, 25 Aug 2022 01:50:46 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 25 Aug 2022 01:50:47 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 25 Aug 2022 01:50:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 25 Aug 2022 01:50:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 25 Aug 2022 01:50:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Aug 2022 01:50:50 GMT
CMD ["sh"]
# Thu, 25 Aug 2022 01:50:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 25 Aug 2022 01:50:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 25 Aug 2022 01:51:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Thu, 25 Aug 2022 01:51:05 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Thu, 25 Aug 2022 01:51:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 25 Aug 2022 01:51:08 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Thu, 25 Aug 2022 01:51:08 GMT
VOLUME [/var/lib/docker]
# Thu, 25 Aug 2022 01:51:09 GMT
EXPOSE 2375 2376
# Thu, 25 Aug 2022 01:51:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 25 Aug 2022 01:51:11 GMT
CMD []
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abd6445c68b28c4fea9c5ead64de6d84bfbcf44d2ea150df466f2efe4ca7ac8`  
		Last Modified: Tue, 09 Aug 2022 18:28:29 GMT  
		Size: 2.0 MB (2010519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6c1cdde4920e39b02e2eaa9a348dd527a363263a4901b3efdf13020d24a917`  
		Last Modified: Tue, 09 Aug 2022 18:28:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1503a42e3097b1eaf3bbc5e72622fc4950bd97ec2439372d2daf9fe4324a21b5`  
		Last Modified: Tue, 09 Aug 2022 18:28:30 GMT  
		Size: 8.0 MB (8048680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f94397c525f39d44ef3fda3b0bba921a889eb33ccc36156f3ba73a88804a75`  
		Last Modified: Fri, 19 Aug 2022 02:49:05 GMT  
		Size: 13.8 MB (13764592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e023f344e2e8ef2e9ff384c968eacae0da278f834f19ec3bfcf001b77dcf98a7`  
		Last Modified: Thu, 25 Aug 2022 01:53:59 GMT  
		Size: 8.6 MB (8568411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f6b1f4f38e7d797834fefe0894f6791cd416771ed66d9425ba8e5543cbd8f0`  
		Last Modified: Thu, 25 Aug 2022 01:53:58 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a0612f8f027a9eaf1887a42600db53596290b731f1f662ee36446a26f548c1`  
		Last Modified: Thu, 25 Aug 2022 01:53:58 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b34538d4f651a5b7d982d7f3fdabe57bf75288a28affd37bc18083cc23b15f`  
		Last Modified: Thu, 25 Aug 2022 01:53:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6940897e2eb9ce49e2dfb8136be2df3401021ae0c88f175c62a0aa18ca4b09`  
		Last Modified: Thu, 25 Aug 2022 01:54:18 GMT  
		Size: 6.7 MB (6736667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4096d227f05943b1fc87593e7e6531b1bd1f1155bca91f06da34f7f5d83833be`  
		Last Modified: Thu, 25 Aug 2022 01:54:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac63d628122d36fc060cc27a7a1af5394f7bdcf707c19fb2bb484ead896e056`  
		Last Modified: Thu, 25 Aug 2022 01:54:24 GMT  
		Size: 49.0 MB (48977184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f926fe515a2c62cf52ea7dffb4f3cedeeb7651643475a6c67d8cdbf69743f093`  
		Last Modified: Thu, 25 Aug 2022 01:54:16 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdcd4eef89fe8e0300362e6734e5a6362bff1ec5e18cfb9b6f6436a9511b144`  
		Last Modified: Thu, 25 Aug 2022 01:54:16 GMT  
		Size: 2.8 KB (2756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

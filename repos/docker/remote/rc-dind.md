## `docker:rc-dind`

```console
$ docker pull docker@sha256:8c325fc710d116a88f8d196001d2c7cc28a92653cf34162b920c32680309a7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:bc3c0619fe3e553c77740380a0ee2e856bbef059dd7530721b994cf64f0a86f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97546006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663c3259607a0efd6dac545c98f546a06a422124976191a714364d22141c0fdc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:15:12 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Jul 2022 22:15:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:15:13 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 18 Jul 2022 22:15:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:18 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:19 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:21 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:21 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:22 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:15:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Jul 2022 22:15:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:15:28 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Jul 2022 22:15:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Jul 2022 22:15:29 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:29 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Jul 2022 22:15:29 GMT
EXPOSE 2375 2376
# Mon, 18 Jul 2022 22:15:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:30 GMT
CMD []
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33702c1843d19cf7c37af730bcf50c456ac6456ed789053432b000db75d3bed3`  
		Last Modified: Mon, 18 Jul 2022 22:17:03 GMT  
		Size: 2.0 MB (2021603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c203384d5b9b22606055f5a6708153653df701158a6c04748cb77be8238c9e`  
		Last Modified: Mon, 18 Jul 2022 22:17:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f2af2e6d461489ee7ae266cc5e28edeff4591cd31668c9b2ad4e428ed7b3ae`  
		Last Modified: Mon, 18 Jul 2022 22:17:13 GMT  
		Size: 62.0 MB (62038253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba6ab3ae59c91ff978c0a8e827eee32ca53cf77c30aadc317b6e02cb62dba36`  
		Last Modified: Mon, 18 Jul 2022 22:17:03 GMT  
		Size: 14.5 MB (14454321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c93e0b3cd4faff61104773d98e89d85e188024b105738e7632281f19f887bf`  
		Last Modified: Mon, 18 Jul 2022 22:17:02 GMT  
		Size: 9.4 MB (9362939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36616eca4033868cc8e298b255ea119075cca4c94953d0180f17be4d77650dd0`  
		Last Modified: Mon, 18 Jul 2022 22:17:00 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d049055706b1909acba8c2679bf51cffa081799346abd23c9dd7b88b141f67b3`  
		Last Modified: Mon, 18 Jul 2022 22:17:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a18bda8d8edba1ec8b8181098baa75d6532cd3d5c3dc2adb04c4aeb9652a196`  
		Last Modified: Mon, 18 Jul 2022 22:17:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db6e11ea5c36c4163165122bc6ede92ef1669dd29ee2771a5f7bf41b8e3355c`  
		Last Modified: Mon, 18 Jul 2022 22:17:30 GMT  
		Size: 6.9 MB (6863194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf41aa5d079ac68e52a7c894b5aaacb41e8983eb0e8056af4e1bed2d3e866f6`  
		Last Modified: Mon, 18 Jul 2022 22:17:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf73ad813577178b8482e9ba1db4e0a3fd52abf3d42991b56944fe817c416d92`  
		Last Modified: Mon, 18 Jul 2022 22:17:28 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f3f9dd5a719bc42e121bdfcc1fee89b655a33f691caba7bafc459f3a2720d0`  
		Last Modified: Mon, 18 Jul 2022 22:17:28 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b7c73d09c71d4cafff1db1bea5aa38351c2d9b7cf266ff8ae64e683c3ece3252
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90137152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053f5ed213cbc5ea3d86eb5b00c1f2a469a3e0d538bb8a951602c5adfd6d4b52`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 04:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 19 Jul 2022 04:35:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jul 2022 04:35:25 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Tue, 19 Jul 2022 04:35:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:35:32 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:35:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:35:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:35:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:35:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:35:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:35:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:35:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:35:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:35:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:35:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 19 Jul 2022 04:35:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:35:57 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 19 Jul 2022 04:35:58 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 19 Jul 2022 04:36:00 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:00 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Jul 2022 04:36:01 GMT
EXPOSE 2375 2376
# Tue, 19 Jul 2022 04:36:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:03 GMT
CMD []
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c091ce5682ea3dc37cb34a07cb2f7f7eef6db6db9ce92946c13f6998cddde5d`  
		Last Modified: Tue, 19 Jul 2022 04:38:36 GMT  
		Size: 2.0 MB (1996624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35394750c918441228eb16c7b94ac5f3b42003d306bf543947c63a99ce4bbf56`  
		Last Modified: Tue, 19 Jul 2022 04:38:36 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478e66e026caf43f7dd1cb87d57bf95197ffa1e22a6c1e5135525a1ab777526b`  
		Last Modified: Tue, 19 Jul 2022 04:38:44 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614596087bce76667d7455dba7936748cf11f2d197b19ddd0a708feb550ef11f`  
		Last Modified: Tue, 19 Jul 2022 04:38:36 GMT  
		Size: 13.1 MB (13097921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0923ae35e2fc257ca39b89c39c66df203b48dab0f030329b33f661b17964227c`  
		Last Modified: Tue, 19 Jul 2022 04:38:35 GMT  
		Size: 8.6 MB (8578066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1799b33f7febcbc24a6392bf1e8a7b78a1f928b39dfed175b2dc31258878495`  
		Last Modified: Tue, 19 Jul 2022 04:38:33 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bece3812e62f299e5c3063e2dbc1f6b2a596166d551ac6ae74c6c2224b20c12b`  
		Last Modified: Tue, 19 Jul 2022 04:38:33 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c5f5b89130c13df8a78b3cf49c9cb3864f6183faa12f36b25e42bf0f93b600`  
		Last Modified: Tue, 19 Jul 2022 04:38:33 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c0607fda6276fb0c842ad7c73580c7e475ac21b3a16156161c5121d09f978f`  
		Last Modified: Tue, 19 Jul 2022 04:39:03 GMT  
		Size: 6.7 MB (6735694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f515c5e169269cb212bcf9de50238b942752fdba27446b5f81a9c0ad89ee0a4e`  
		Last Modified: Tue, 19 Jul 2022 04:39:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212c180a858ee5a23e31ed00e2ac9cb879c00a42218c0a2567b402f51eb97447`  
		Last Modified: Tue, 19 Jul 2022 04:39:02 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee5c7530ed7fdb78b3a825d80384b5b0ba5bd3ef9a7dcb2fdc2dbc12d36356b`  
		Last Modified: Tue, 19 Jul 2022 04:39:02 GMT  
		Size: 2.7 KB (2747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

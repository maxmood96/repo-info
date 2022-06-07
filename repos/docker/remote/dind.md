## `docker:dind`

```console
$ docker pull docker@sha256:a7a9383d0631b5f6b59f0a8138912d20b63c9320127e3fb065cb9ca0257a58b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:8cdb600dd59001892484f7c4be06166e42a2952065b6822b98c5aa7b8ef2ce8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101111945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbe252bd9afb23859f250989da416b2cd8ab30f4b61a2bc8fca6f9b05d7e665`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 27 May 2022 00:21:48 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 07 Jun 2022 18:23:40 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 07 Jun 2022 18:23:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 07 Jun 2022 18:23:46 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 07 Jun 2022 18:23:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 07 Jun 2022 18:23:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.0
# Tue, 07 Jun 2022 18:23:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-x86_64'; 			sha256='4eb9084cd9e33d906bd1ea11b5bc2e77a43f8ffbe7228bcf7c829a7687f5c4bb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-armv6'; 			sha256='6f447869c2286d583d5497e8a1c50b7251dc9f0763c45b064a4b898a53ebce4c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-armv7'; 			sha256='cf566ae18f89498bb20ac71d949b82b97bec3e9f972e009141c4f2faf440257a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-aarch64'; 			sha256='f2bc74dddaa58add7b428b5a764ccd4f048b366f3eb5c80a77ff06fcdc00b3ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-ppc64le'; 			sha256='0e6163ccbddf4faea428a78c46c214c6bba0ab3fef57e3cad364e9ca520fa176'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-s390x'; 			sha256='df667634751a575ab29bc4f125b69dfa09d1924daf26bbc0f46e6b09ee1e6699'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 07 Jun 2022 18:23:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 07 Jun 2022 18:23:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 07 Jun 2022 18:23:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Jun 2022 18:23:52 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 07 Jun 2022 18:23:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jun 2022 18:23:52 GMT
CMD ["sh"]
# Tue, 07 Jun 2022 18:24:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 07 Jun 2022 18:24:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 07 Jun 2022 18:24:03 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 07 Jun 2022 18:24:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 07 Jun 2022 18:24:04 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 07 Jun 2022 18:24:04 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Jun 2022 18:24:04 GMT
EXPOSE 2375 2376
# Tue, 07 Jun 2022 18:24:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Jun 2022 18:24:05 GMT
CMD []
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d991df732aca5558e3374cd6554967a937cd594176f8e0fb592322528caf411f`  
		Last Modified: Fri, 27 May 2022 00:22:47 GMT  
		Size: 2.0 MB (2021620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d05af1c4101377236dcaf5b686eb6313f88a6ccf0cb4b1ad9383337eaaabd1`  
		Last Modified: Fri, 27 May 2022 00:22:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a01eeb4b9660234932fe1a5ed6ee12b88476503688d1af44ef2cf5589db59c5`  
		Last Modified: Tue, 07 Jun 2022 18:25:11 GMT  
		Size: 65.5 MB (65511093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f16477544224c056335320872aa8dd6c2a404df9982484e1f62603e0f1f8e2a`  
		Last Modified: Tue, 07 Jun 2022 18:25:01 GMT  
		Size: 14.5 MB (14454323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e917105572c19bab12a64c5f1079e8d7b0a3e10899bd0398d1f136d41a4af191`  
		Last Modified: Tue, 07 Jun 2022 18:25:00 GMT  
		Size: 9.5 MB (9456585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b709778230e46fbd5042dc9165462ac00b69b08da200fd164c4b55ee90d71ed6`  
		Last Modified: Tue, 07 Jun 2022 18:24:59 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94076fc9c77a2ec8cd8737d8ee69c11882eaa16be0e46ea97b42763d6de07213`  
		Last Modified: Tue, 07 Jun 2022 18:24:59 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0650593e055d90b3f09ecf2e61114a35929437150d1f25d6e9aea5e4d4ef57`  
		Last Modified: Tue, 07 Jun 2022 18:24:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8739efbf33852756a9d17dd471ab7ab9d9a1f183df6185763c4f54d55f3e5ef`  
		Last Modified: Tue, 07 Jun 2022 18:25:31 GMT  
		Size: 6.9 MB (6862542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528486149a1ec660cc13a105d322cbe384bf2fd0bb5b32436043928d35701e8`  
		Last Modified: Tue, 07 Jun 2022 18:25:30 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fce28207d4c0f42d2a8352f195f1551714dfa68bcc768565b63a0e030a46813`  
		Last Modified: Tue, 07 Jun 2022 18:25:29 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c6543c9821cdb12ce3c3b95bed6148272f6ee648fcaf31c1b5b6d7aa67c459`  
		Last Modified: Tue, 07 Jun 2022 18:25:29 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c82526b54ad542830185247b1fd7cd75ca06c4b7379625a631193ebebbffceb8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93216008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2d13d30ebd3836c5760272dda377aa12d9253bf2aee7a175a1360773e2a9d9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:42:03 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 27 May 2022 00:42:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 07 Jun 2022 18:44:31 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 07 Jun 2022 18:44:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 07 Jun 2022 18:44:36 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 07 Jun 2022 18:44:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 07 Jun 2022 18:44:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.0
# Tue, 07 Jun 2022 18:44:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-x86_64'; 			sha256='4eb9084cd9e33d906bd1ea11b5bc2e77a43f8ffbe7228bcf7c829a7687f5c4bb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-armv6'; 			sha256='6f447869c2286d583d5497e8a1c50b7251dc9f0763c45b064a4b898a53ebce4c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-armv7'; 			sha256='cf566ae18f89498bb20ac71d949b82b97bec3e9f972e009141c4f2faf440257a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-aarch64'; 			sha256='f2bc74dddaa58add7b428b5a764ccd4f048b366f3eb5c80a77ff06fcdc00b3ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-ppc64le'; 			sha256='0e6163ccbddf4faea428a78c46c214c6bba0ab3fef57e3cad364e9ca520fa176'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-s390x'; 			sha256='df667634751a575ab29bc4f125b69dfa09d1924daf26bbc0f46e6b09ee1e6699'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 07 Jun 2022 18:44:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 07 Jun 2022 18:44:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 07 Jun 2022 18:44:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Jun 2022 18:44:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 07 Jun 2022 18:44:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jun 2022 18:44:52 GMT
CMD ["sh"]
# Tue, 07 Jun 2022 18:45:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 07 Jun 2022 18:45:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 07 Jun 2022 18:45:03 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 07 Jun 2022 18:45:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 07 Jun 2022 18:45:06 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 07 Jun 2022 18:45:06 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Jun 2022 18:45:07 GMT
EXPOSE 2375 2376
# Tue, 07 Jun 2022 18:45:08 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Jun 2022 18:45:09 GMT
CMD []
```

-	Layers:
	-	`sha256:b3c136eddcbf2003d3180787cef00f39d46b9fd9e4623178282ad6a8d63ad3b0`  
		Last Modified: Mon, 23 May 2022 19:08:34 GMT  
		Size: 2.7 MB (2694464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3e5a9e15a60519e35e8b9a753200b3a5fd5d702eb7ce3db15a5cc6dfea4c7d`  
		Last Modified: Fri, 27 May 2022 00:44:06 GMT  
		Size: 2.0 MB (1996621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2296f0760e1d9178f62ef54c685f9eeea21ee68455df53b6823bf3da5784f5df`  
		Last Modified: Fri, 27 May 2022 00:44:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7208c9164699a390332f26552a4e3372cbba8153d21dd8c579d78b4820727447`  
		Last Modified: Tue, 07 Jun 2022 18:46:58 GMT  
		Size: 60.0 MB (60022171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fd660eb6acfde977fdcc2e06e1f8b820b994c605f8d7c2a43c8043fee47a59`  
		Last Modified: Tue, 07 Jun 2022 18:46:49 GMT  
		Size: 13.1 MB (13097908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed4b77ab26353356aa5e47399b195759c104e1949f2c8552ed99141fcd5a8e6`  
		Last Modified: Tue, 07 Jun 2022 18:46:48 GMT  
		Size: 8.7 MB (8663386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e346f102da723c6d8f8709a20fe5d2b88c6efc5c31da9c1e7fba1007acd0ec1f`  
		Last Modified: Tue, 07 Jun 2022 18:46:46 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97325db524006b151b2a34f2981b47567785b4362b383f8672aa4ccd00df3bfe`  
		Last Modified: Tue, 07 Jun 2022 18:46:47 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6e016098eef53d87f0df18ffe9c41bda01a822971b75a0d351d1787a4d59fb`  
		Last Modified: Tue, 07 Jun 2022 18:46:46 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e98490325d999d399e486a1107cbb821ef56e26e4b8e09cba42eab6de668f53`  
		Last Modified: Tue, 07 Jun 2022 18:47:20 GMT  
		Size: 6.7 MB (6734617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3937658d06fd0152ee0795e63b1ac2bef28cd0e08636738ed86cfb3f270efe87`  
		Last Modified: Tue, 07 Jun 2022 18:47:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520215962f31f70fbe23340f593756dd36c602b6523c60d6edf47191a3366f70`  
		Last Modified: Tue, 07 Jun 2022 18:47:19 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c038ae79644412f10a6fd71b2aeb63c3462ca53f5eba947465d067157abd1d`  
		Last Modified: Tue, 07 Jun 2022 18:47:19 GMT  
		Size: 2.7 KB (2748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

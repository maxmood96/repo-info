## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:9ffe7e58a8cd4f9ea1ffabedbae9bb300f195e32cbc2b4b3bd5f540cabb23605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:debb3bf5dc60e116bae48060a3706cd3f1cfdd8f6772cdeda5ab87d00183cbe8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131916670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1d24679530a758f55eef857856c72ffabadb919674c48f549e0cc0c8a52e28`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 07 Mar 2023 19:40:30 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 07 Mar 2023 19:40:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Tue, 07 Mar 2023 19:40:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Tue, 07 Mar 2023 19:40:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 07 Mar 2023 19:40:35 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 07 Mar 2023 19:40:35 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 07 Mar 2023 19:40:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Mar 2023 19:40:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 07 Mar 2023 19:40:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Mar 2023 19:40:36 GMT
CMD ["sh"]
# Tue, 07 Mar 2023 19:40:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 07 Mar 2023 19:40:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 07 Mar 2023 19:40:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Tue, 07 Mar 2023 19:40:48 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 07 Mar 2023 19:40:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 07 Mar 2023 19:40:49 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Tue, 07 Mar 2023 19:40:49 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Mar 2023 19:40:49 GMT
EXPOSE 2375 2376
# Tue, 07 Mar 2023 19:40:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Mar 2023 19:40:49 GMT
CMD []
# Tue, 07 Mar 2023 19:40:53 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Tue, 07 Mar 2023 19:40:54 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 07 Mar 2023 19:40:54 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 07 Mar 2023 19:40:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 07 Mar 2023 19:40:57 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 07 Mar 2023 19:40:57 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 07 Mar 2023 19:40:57 GMT
USER rootless
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4927f75f31364ad04a4dc42dfc39fee8d641e4d89462d798a6af390b45daeff1`  
		Last Modified: Tue, 07 Mar 2023 19:43:08 GMT  
		Size: 16.0 MB (16001695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66bd219994aa14cced96198323224b6cf488471252697c33f07e73384129339`  
		Last Modified: Tue, 07 Mar 2023 19:43:09 GMT  
		Size: 15.3 MB (15343456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b31935344b35fb5abc8b68f4559e2cbc3739c4c573b86580518bf715bfaae4`  
		Last Modified: Tue, 07 Mar 2023 19:43:06 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e7ea90fd8cbf6d4e476e1294ae071545141495c16818d74dbe12d9e68eeff5`  
		Last Modified: Tue, 07 Mar 2023 19:43:06 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e298663ae8eccfc4f8c0709f08dba3c1adca8825c04aaa4d684631cf176e07`  
		Last Modified: Tue, 07 Mar 2023 19:43:06 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6944289dbe52bada58713721b7607b93ef33a7e5ffa0ada3f7847fc0feed3bb6`  
		Last Modified: Tue, 07 Mar 2023 19:43:31 GMT  
		Size: 6.8 MB (6839018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd114704efc74eacdcc7b9107e97fbf366d86027db8c079378a9e33a1b520224`  
		Last Modified: Tue, 07 Mar 2023 19:43:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f920e3a34f6a2833619f67858ad6b4a6df018f775acc08251c9f288a9a11e3`  
		Last Modified: Tue, 07 Mar 2023 19:43:38 GMT  
		Size: 53.0 MB (53016622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4ddd7f9d30c628e78a59a434fbfe940277ec11b5696edda16e34a1d2dd4734`  
		Last Modified: Tue, 07 Mar 2023 19:43:30 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304d3e03bd7cd957bd42bcb8b9d04ae6e95407fa82721cb8b50955db961daf1f`  
		Last Modified: Tue, 07 Mar 2023 19:43:30 GMT  
		Size: 2.8 KB (2822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfcde3fc6adfee83b6d4958a2c2806dbd1409b426245a48fb939c59fdbc5f7b`  
		Last Modified: Tue, 07 Mar 2023 19:43:52 GMT  
		Size: 1.4 MB (1375673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e19a629e81d9710eade59bec38a139f55c8611f750df94ae3955f7265ba93e5`  
		Last Modified: Tue, 07 Mar 2023 19:43:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4e98cb82ccf4e5175641e6b14930e046954a2069667624eb30415e66d25f0c`  
		Last Modified: Tue, 07 Mar 2023 19:43:51 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5499459456a6863f1a52cbbb19380d41a5acca6a7fb14d88557b343300837987`  
		Last Modified: Tue, 07 Mar 2023 19:43:55 GMT  
		Size: 19.9 MB (19909524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf08125883ccb2de0a06d319d4d2ba597e50d36a8086a7a9afdc1616b1a969d`  
		Last Modified: Tue, 07 Mar 2023 19:43:51 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b86410b688a73f4dabb4abc261fe218d4ecff4c9dae6aee82c2fa7bed4c5715a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125266722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1ca437bb4492c47e594c8cdd18ba27b1712c3d9878523344eb991cce827020`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 07 Mar 2023 19:42:24 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 07 Mar 2023 19:42:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Tue, 07 Mar 2023 19:42:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Tue, 07 Mar 2023 19:42:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 07 Mar 2023 19:42:28 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 07 Mar 2023 19:42:28 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 07 Mar 2023 19:42:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Mar 2023 19:42:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 07 Mar 2023 19:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Mar 2023 19:42:29 GMT
CMD ["sh"]
# Tue, 07 Mar 2023 19:42:35 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 07 Mar 2023 19:42:35 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 07 Mar 2023 19:42:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Tue, 07 Mar 2023 19:42:39 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 07 Mar 2023 19:42:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 07 Mar 2023 19:42:40 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Tue, 07 Mar 2023 19:42:40 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Mar 2023 19:42:40 GMT
EXPOSE 2375 2376
# Tue, 07 Mar 2023 19:42:40 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Mar 2023 19:42:40 GMT
CMD []
# Tue, 07 Mar 2023 19:42:45 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Tue, 07 Mar 2023 19:42:46 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 07 Mar 2023 19:42:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 07 Mar 2023 19:42:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 07 Mar 2023 19:42:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 07 Mar 2023 19:42:49 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 07 Mar 2023 19:42:49 GMT
USER rootless
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0b5e8fb705e85176b3e83174bd85f70a7b1cb78f26717f945d058641c64572`  
		Last Modified: Tue, 07 Mar 2023 19:45:01 GMT  
		Size: 14.4 MB (14441448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5425837e7f76e989a0adaeaf5158ca3f5ee4016eeed1a24f29cabaa00f220c3`  
		Last Modified: Tue, 07 Mar 2023 19:45:01 GMT  
		Size: 13.8 MB (13819063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b438d4a132b18571b5394af422088020ef48271dbe5e22c6fbcf0cf6f9c74411`  
		Last Modified: Tue, 07 Mar 2023 19:44:59 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2911d71c794177bb1154eeceb359e970ac481fc95a30c85f7ddbdc3ed01ca7`  
		Last Modified: Tue, 07 Mar 2023 19:44:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0077b9f0b20e12262afe073d09ac98807c149593d620ac14838a3796686c17e2`  
		Last Modified: Tue, 07 Mar 2023 19:44:59 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebf66cda2d09afbf1fe2d23276fb310fc9e751fa7a45786a2fdf89e9cd859aa`  
		Last Modified: Tue, 07 Mar 2023 19:45:24 GMT  
		Size: 7.0 MB (6992856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7328abe101678060006e90e716831bbcd740529a8d6b535442ac7b8033f05957`  
		Last Modified: Tue, 07 Mar 2023 19:45:24 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fd226966401a97810f15283fbb79f58200e6802caffbb2c63fbc7dd059afd9`  
		Last Modified: Tue, 07 Mar 2023 19:45:29 GMT  
		Size: 48.7 MB (48680412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80ba472f381ed11923226197b5dffc01528f6e6d55c0e22fd5e66c59966bd70`  
		Last Modified: Tue, 07 Mar 2023 19:45:24 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c173823f9ec6e0e164f630ff711495c988f3996c619d2be77bd0340987dcca`  
		Last Modified: Tue, 07 Mar 2023 19:45:24 GMT  
		Size: 2.8 KB (2820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90379be36e20656d3b4cb7deaeb95b9c2f836deb1045b684730de3a31d708134`  
		Last Modified: Tue, 07 Mar 2023 19:45:44 GMT  
		Size: 1.4 MB (1401572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81b9f6f9ad09615183574eb19be35a7e57c64f81349f2e5e668b9360346fa22`  
		Last Modified: Tue, 07 Mar 2023 19:45:44 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30e5b5d1287671a2f6cc57e1bf2867591ff7859373461123f91fe8386af3fde`  
		Last Modified: Tue, 07 Mar 2023 19:45:43 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fc9efe3f93402d2e507a969aabdfec75ce211218a891ae66c2d67f027528d1`  
		Last Modified: Tue, 07 Mar 2023 19:45:46 GMT  
		Size: 21.9 MB (21881889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8286f58fdb8c51fef54697598a9b417b6aaf3e103429f9f7d4082ba7b5249743`  
		Last Modified: Tue, 07 Mar 2023 19:45:43 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

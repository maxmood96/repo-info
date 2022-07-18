<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:20`](#docker20)
-	[`docker:20-dind`](#docker20-dind)
-	[`docker:20-dind-rootless`](#docker20-dind-rootless)
-	[`docker:20-git`](#docker20-git)
-	[`docker:20-windowsservercore`](#docker20-windowsservercore)
-	[`docker:20-windowsservercore-1809`](#docker20-windowsservercore-1809)
-	[`docker:20-windowsservercore-ltsc2022`](#docker20-windowsservercore-ltsc2022)
-	[`docker:20.10`](#docker2010)
-	[`docker:20.10-dind`](#docker2010-dind)
-	[`docker:20.10-dind-rootless`](#docker2010-dind-rootless)
-	[`docker:20.10-git`](#docker2010-git)
-	[`docker:20.10-windowsservercore`](#docker2010-windowsservercore)
-	[`docker:20.10-windowsservercore-1809`](#docker2010-windowsservercore-1809)
-	[`docker:20.10-windowsservercore-ltsc2022`](#docker2010-windowsservercore-ltsc2022)
-	[`docker:20.10.17`](#docker201017)
-	[`docker:20.10.17-alpine3.16`](#docker201017-alpine316)
-	[`docker:20.10.17-dind`](#docker201017-dind)
-	[`docker:20.10.17-dind-alpine3.16`](#docker201017-dind-alpine316)
-	[`docker:20.10.17-dind-rootless`](#docker201017-dind-rootless)
-	[`docker:20.10.17-git`](#docker201017-git)
-	[`docker:20.10.17-windowsservercore`](#docker201017-windowsservercore)
-	[`docker:20.10.17-windowsservercore-1809`](#docker201017-windowsservercore-1809)
-	[`docker:20.10.17-windowsservercore-ltsc2022`](#docker201017-windowsservercore-ltsc2022)
-	[`docker:22.06-rc`](#docker2206-rc)
-	[`docker:22.06-rc-dind`](#docker2206-rc-dind)
-	[`docker:22.06-rc-dind-rootless`](#docker2206-rc-dind-rootless)
-	[`docker:22.06-rc-git`](#docker2206-rc-git)
-	[`docker:22.06-rc-windowsservercore`](#docker2206-rc-windowsservercore)
-	[`docker:22.06-rc-windowsservercore-1809`](#docker2206-rc-windowsservercore-1809)
-	[`docker:22.06-rc-windowsservercore-ltsc2022`](#docker2206-rc-windowsservercore-ltsc2022)
-	[`docker:22.06.0-beta.0`](#docker22060-beta0)
-	[`docker:22.06.0-beta.0-alpine3.16`](#docker22060-beta0-alpine316)
-	[`docker:22.06.0-beta.0-dind`](#docker22060-beta0-dind)
-	[`docker:22.06.0-beta.0-dind-alpine3.16`](#docker22060-beta0-dind-alpine316)
-	[`docker:22.06.0-beta.0-dind-rootless`](#docker22060-beta0-dind-rootless)
-	[`docker:22.06.0-beta.0-git`](#docker22060-beta0-git)
-	[`docker:22.06.0-beta.0-windowsservercore`](#docker22060-beta0-windowsservercore)
-	[`docker:22.06.0-beta.0-windowsservercore-1809`](#docker22060-beta0-windowsservercore-1809)
-	[`docker:22.06.0-beta.0-windowsservercore-ltsc2022`](#docker22060-beta0-windowsservercore-ltsc2022)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:rc`](#dockerrc)
-	[`docker:rc-dind`](#dockerrc-dind)
-	[`docker:rc-dind-rootless`](#dockerrc-dind-rootless)
-	[`docker:rc-git`](#dockerrc-git)
-	[`docker:rc-windowsservercore`](#dockerrc-windowsservercore)
-	[`docker:rc-windowsservercore-1809`](#dockerrc-windowsservercore-1809)
-	[`docker:rc-windowsservercore-ltsc2022`](#dockerrc-windowsservercore-ltsc2022)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:20`

```console
$ docker pull docker@sha256:386dd216988a21c83233d32b3926300909a111fa73266d035e992280aa3a9e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:03b0716af18eedd4025b71c92fafcd09dd8cd4f020fd109284abc699983849c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94150653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283a30f3dbe83eba914a4aa16f95458512fa7799d177e069561e8e424f7f0fb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:15:12 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Jul 2022 22:15:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e76ec14a5acc9a9061233f0465f115b928de5c621ea85c2032ea9a5bb258e2e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86391090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0229d8a86a420066bf144bb1ef30a5a796ba08e3b84c35e8d1082ff5bc46b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:70cd116f750841065b75efc37f92051894dd66d2893af0ac2b78c60eb9abe0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:7c563086f2a9d640be3d723e9b0c0c5095de9844e7c0bdb0c042d769ff7ada80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101018932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07e77e26a3961cf233e96434f0473d09d3c5499c1927fb873936115e7f5c9d4`
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
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:03 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Jul 2022 22:16:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:04 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Jul 2022 22:16:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Jul 2022 22:16:05 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:16:05 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Jul 2022 22:16:05 GMT
EXPOSE 2375 2376
# Mon, 18 Jul 2022 22:16:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Jul 2022 22:16:05 GMT
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88901f96301057594237c9864b66f790ff7a5fef0c32a77d2ec663d644d45432`  
		Last Modified: Mon, 18 Jul 2022 22:18:50 GMT  
		Size: 6.9 MB (6863256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9991b1b34b037f21020309d31bd20f65cf695235ee4f3336717010d66bc9136e`  
		Last Modified: Mon, 18 Jul 2022 22:18:49 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f123d0d06ab3c31e76d283d36506013fad0ac3f4111bce66c1d0f030f47251e`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033c6a3c8675a7a8e57d8b4f8bf3bcb073fe6b879f7309c055996e051eb36cc5`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e51c69aca258a3bdf624db6685e328df185513577ac7b28dac10916816777d2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93130744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1490f7b533aeb3f1ee222cea8e688b5d6ca260444f849ecec19228e6882a81ba`
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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:40:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:40:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:40:47 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:40:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:40:50 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:50 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:40:51 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:40:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:53 GMT
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c82eb82389bdb9c7d276b1643f13d3c5caae406cf7465fdc96939f266e6f12`  
		Last Modified: Mon, 27 Jun 2022 19:44:06 GMT  
		Size: 6.7 MB (6734644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bbc1c8669d112dd5ccbe24eae85fcf64a7e05164f1f15bda3f7af0bcbffbb6`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12b2450c676909ee9dae0cd4c9dde25caa5de2d4e5522a64aa5baf279120806`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 963.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17ce1449b637b669cb1dff1718ae17b979ff4efa77ec1fc72be0194468c9540`  
		Last Modified: Mon, 27 Jun 2022 19:44:04 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:fc06ba995a9159944a5778145af22d7b3c5486f995c2e79f003d75fa5dfe30a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d6aac839f895a692d2bfa97f1c6092037b4affec034ede63afc8f5a3913bc4ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121725927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c4bb481982e73b10e8d9a47a9944a836e3193b95c6930b9ad4f9a86d2aa69e`
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
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:03 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Jul 2022 22:16:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:04 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Jul 2022 22:16:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Jul 2022 22:16:05 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:16:05 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Jul 2022 22:16:05 GMT
EXPOSE 2375 2376
# Mon, 18 Jul 2022 22:16:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Jul 2022 22:16:05 GMT
CMD []
# Mon, 18 Jul 2022 22:16:09 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 18 Jul 2022 22:16:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Jul 2022 22:16:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Jul 2022 22:16:19 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Jul 2022 22:16:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Jul 2022 22:16:19 GMT
USER rootless
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88901f96301057594237c9864b66f790ff7a5fef0c32a77d2ec663d644d45432`  
		Last Modified: Mon, 18 Jul 2022 22:18:50 GMT  
		Size: 6.9 MB (6863256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9991b1b34b037f21020309d31bd20f65cf695235ee4f3336717010d66bc9136e`  
		Last Modified: Mon, 18 Jul 2022 22:18:49 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f123d0d06ab3c31e76d283d36506013fad0ac3f4111bce66c1d0f030f47251e`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033c6a3c8675a7a8e57d8b4f8bf3bcb073fe6b879f7309c055996e051eb36cc5`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eaa4c3317aeec448940ff55356194c5de34d5d5ea2113e689b8dfc6cc65169`  
		Last Modified: Mon, 18 Jul 2022 22:19:10 GMT  
		Size: 1.4 MB (1358399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961740e547309d1bd3298dec9b78f143c42f08f9bdac3ce03bded0b6157c1787`  
		Last Modified: Mon, 18 Jul 2022 22:19:09 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca55d339fdc5ea0e18b66ac4f32d2170b2bdea7d444184792b0fd967cc34ef1`  
		Last Modified: Mon, 18 Jul 2022 22:19:09 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8c9be32912483c3d1874104ba9364eae2f6cc5a8e41d629c02aedce4b3a38c`  
		Last Modified: Mon, 18 Jul 2022 22:19:13 GMT  
		Size: 19.3 MB (19346880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c27463145e14b7eb1fae03941f74bf3a5ce1b7907fbde1f352429064c1d5031`  
		Last Modified: Mon, 18 Jul 2022 22:19:09 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:79728767115a191b17a69d129a65be1a067d5828bbf90d43e5833b92e2fe41b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115679783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23551a0cecc123712f378299710ae922fa0cb237e78e630aad050070f84ad943`
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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:40:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:40:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:40:47 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:40:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:40:50 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:50 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:40:51 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:40:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:53 GMT
CMD []
# Mon, 27 Jun 2022 19:41:01 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 27 Jun 2022 19:41:01 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 27 Jun 2022 19:41:02 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:41:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 27 Jun 2022 19:41:05 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 27 Jun 2022 19:41:06 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 27 Jun 2022 19:41:07 GMT
USER rootless
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c82eb82389bdb9c7d276b1643f13d3c5caae406cf7465fdc96939f266e6f12`  
		Last Modified: Mon, 27 Jun 2022 19:44:06 GMT  
		Size: 6.7 MB (6734644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bbc1c8669d112dd5ccbe24eae85fcf64a7e05164f1f15bda3f7af0bcbffbb6`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12b2450c676909ee9dae0cd4c9dde25caa5de2d4e5522a64aa5baf279120806`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 963.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17ce1449b637b669cb1dff1718ae17b979ff4efa77ec1fc72be0194468c9540`  
		Last Modified: Mon, 27 Jun 2022 19:44:04 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73afe9c1ea8a9add0560096dfa62e68214d911a898f87a2e607375f2fe5683eb`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 1.4 MB (1370343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ba1c6a8841b95b395c49b28169677c6307a3101e227708a700de94e9c8d0b2`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64830e281baf40fb6bf58458f881f01f312bda27135405c9b5546de5cabf49d`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28141130595ce38345733636d0d91f525fa08777adf2284bfce0a9c5236dab2d`  
		Last Modified: Mon, 27 Jun 2022 19:44:31 GMT  
		Size: 21.2 MB (21177072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fab70f37b78c4047be0923ffdada8d53cc2e47aa319d07b593475cc92dd034`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:47bd1331d72aebfee67194c4bebf45c0a6303b63755848ca98cce74b70ac44dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:a3cacd2bbc1d323daa79d5a8bda48305966261dbe791228dd6cffcd3e95e30f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101094335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c483e5e493f0032c1e9c95d8b4883431b6f5dd02d0bb185dc0a6d7809bd7ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:15:12 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Jul 2022 22:15:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:23 GMT
RUN apk add --no-cache git
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f712b6a4d7efecf0efa1961bf4e2fdc1859268c16db32d45fcfa7cc72abc20`  
		Last Modified: Mon, 18 Jul 2022 22:19:31 GMT  
		Size: 6.9 MB (6943682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:32f4c05237f4f02261aac5b4a0f970965a78dc3eba25ea432fd1b17f80838c61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93445547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc060a5a282fca1d0c38b4b1ccc8792e0c13d753ed216a66a9a87992cff14258`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:41:15 GMT
RUN apk add --no-cache git
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9d9fddd250721c2f847a9bbc6d46da61d812217213838e3879459cd5c1e2e7`  
		Last Modified: Mon, 27 Jun 2022 19:44:52 GMT  
		Size: 7.1 MB (7054457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:aa0b01f106685b0d0494aff223fcca039e507bf16c4859593b26714599074fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `docker:20-windowsservercore` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:7262b1947cffb1bf370d142eba1fc216dd59510b2f6af0bd9b43d4da8f5042db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353410338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96da4d70661fa4eac578cd29bb6e6f9ab0753d3b20202e726a3794d037979f56`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:11:48 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:11:49 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:12:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1da040c1cae02b726504c01ddb04ab6bc757384118e4997d2dc4b7e71fa76`  
		Last Modified: Wed, 13 Jul 2022 17:14:37 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd127957c40c6e903e73c2d36fd99a3937d8d4247d3068b446ae89771561f56`  
		Last Modified: Wed, 13 Jul 2022 17:14:38 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848a713cc66b0bd9b05ab1649d40f3a864c3557b09ee84feaf88a50bf9e71962`  
		Last Modified: Wed, 13 Jul 2022 17:14:48 GMT  
		Size: 52.5 MB (52520655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:d286ed6b7161125360b30763cddc35da6be81a4a8d40a46269788a647ab0b4a6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2724680561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00e049b0813b313a68cbcc666e527d2ee40c170b3c61f83c75952483ee5fbb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:13:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86af5967d42c804ec0ac2f177b83169359deede4dafa6dbfb40bc97aad7181`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d48e2e1c03a59c2bc5fa97787d608c1c56d2c5dea767bcb8266ece9c31be0`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f086bc01bdb19544655edff05b0730da6228f93c165306b8a1c2afbac5b4396`  
		Last Modified: Wed, 13 Jul 2022 17:15:11 GMT  
		Size: 52.3 MB (52281174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:c4c60a9bf7998d5b05c8c6d30644c7301e26edcba1ba9a13afbb4e8d372b9043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:d286ed6b7161125360b30763cddc35da6be81a4a8d40a46269788a647ab0b4a6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2724680561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00e049b0813b313a68cbcc666e527d2ee40c170b3c61f83c75952483ee5fbb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:13:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86af5967d42c804ec0ac2f177b83169359deede4dafa6dbfb40bc97aad7181`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d48e2e1c03a59c2bc5fa97787d608c1c56d2c5dea767bcb8266ece9c31be0`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f086bc01bdb19544655edff05b0730da6228f93c165306b8a1c2afbac5b4396`  
		Last Modified: Wed, 13 Jul 2022 17:15:11 GMT  
		Size: 52.3 MB (52281174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:b6f7a5dae2f95505f6fee244d4588441986227aeb49eda1e7bf8019a46da3957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `docker:20-windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:7262b1947cffb1bf370d142eba1fc216dd59510b2f6af0bd9b43d4da8f5042db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353410338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96da4d70661fa4eac578cd29bb6e6f9ab0753d3b20202e726a3794d037979f56`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:11:48 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:11:49 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:12:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1da040c1cae02b726504c01ddb04ab6bc757384118e4997d2dc4b7e71fa76`  
		Last Modified: Wed, 13 Jul 2022 17:14:37 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd127957c40c6e903e73c2d36fd99a3937d8d4247d3068b446ae89771561f56`  
		Last Modified: Wed, 13 Jul 2022 17:14:38 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848a713cc66b0bd9b05ab1649d40f3a864c3557b09ee84feaf88a50bf9e71962`  
		Last Modified: Wed, 13 Jul 2022 17:14:48 GMT  
		Size: 52.5 MB (52520655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10`

```console
$ docker pull docker@sha256:386dd216988a21c83233d32b3926300909a111fa73266d035e992280aa3a9e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:03b0716af18eedd4025b71c92fafcd09dd8cd4f020fd109284abc699983849c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94150653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283a30f3dbe83eba914a4aa16f95458512fa7799d177e069561e8e424f7f0fb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:15:12 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Jul 2022 22:15:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e76ec14a5acc9a9061233f0465f115b928de5c621ea85c2032ea9a5bb258e2e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86391090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0229d8a86a420066bf144bb1ef30a5a796ba08e3b84c35e8d1082ff5bc46b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:70cd116f750841065b75efc37f92051894dd66d2893af0ac2b78c60eb9abe0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:7c563086f2a9d640be3d723e9b0c0c5095de9844e7c0bdb0c042d769ff7ada80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101018932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07e77e26a3961cf233e96434f0473d09d3c5499c1927fb873936115e7f5c9d4`
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
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:03 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Jul 2022 22:16:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:04 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Jul 2022 22:16:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Jul 2022 22:16:05 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:16:05 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Jul 2022 22:16:05 GMT
EXPOSE 2375 2376
# Mon, 18 Jul 2022 22:16:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Jul 2022 22:16:05 GMT
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88901f96301057594237c9864b66f790ff7a5fef0c32a77d2ec663d644d45432`  
		Last Modified: Mon, 18 Jul 2022 22:18:50 GMT  
		Size: 6.9 MB (6863256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9991b1b34b037f21020309d31bd20f65cf695235ee4f3336717010d66bc9136e`  
		Last Modified: Mon, 18 Jul 2022 22:18:49 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f123d0d06ab3c31e76d283d36506013fad0ac3f4111bce66c1d0f030f47251e`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033c6a3c8675a7a8e57d8b4f8bf3bcb073fe6b879f7309c055996e051eb36cc5`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e51c69aca258a3bdf624db6685e328df185513577ac7b28dac10916816777d2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93130744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1490f7b533aeb3f1ee222cea8e688b5d6ca260444f849ecec19228e6882a81ba`
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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:40:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:40:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:40:47 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:40:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:40:50 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:50 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:40:51 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:40:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:53 GMT
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c82eb82389bdb9c7d276b1643f13d3c5caae406cf7465fdc96939f266e6f12`  
		Last Modified: Mon, 27 Jun 2022 19:44:06 GMT  
		Size: 6.7 MB (6734644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bbc1c8669d112dd5ccbe24eae85fcf64a7e05164f1f15bda3f7af0bcbffbb6`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12b2450c676909ee9dae0cd4c9dde25caa5de2d4e5522a64aa5baf279120806`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 963.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17ce1449b637b669cb1dff1718ae17b979ff4efa77ec1fc72be0194468c9540`  
		Last Modified: Mon, 27 Jun 2022 19:44:04 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:fc06ba995a9159944a5778145af22d7b3c5486f995c2e79f003d75fa5dfe30a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d6aac839f895a692d2bfa97f1c6092037b4affec034ede63afc8f5a3913bc4ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121725927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c4bb481982e73b10e8d9a47a9944a836e3193b95c6930b9ad4f9a86d2aa69e`
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
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:03 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Jul 2022 22:16:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:04 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Jul 2022 22:16:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Jul 2022 22:16:05 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:16:05 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Jul 2022 22:16:05 GMT
EXPOSE 2375 2376
# Mon, 18 Jul 2022 22:16:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Jul 2022 22:16:05 GMT
CMD []
# Mon, 18 Jul 2022 22:16:09 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 18 Jul 2022 22:16:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Jul 2022 22:16:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Jul 2022 22:16:19 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Jul 2022 22:16:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Jul 2022 22:16:19 GMT
USER rootless
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88901f96301057594237c9864b66f790ff7a5fef0c32a77d2ec663d644d45432`  
		Last Modified: Mon, 18 Jul 2022 22:18:50 GMT  
		Size: 6.9 MB (6863256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9991b1b34b037f21020309d31bd20f65cf695235ee4f3336717010d66bc9136e`  
		Last Modified: Mon, 18 Jul 2022 22:18:49 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f123d0d06ab3c31e76d283d36506013fad0ac3f4111bce66c1d0f030f47251e`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033c6a3c8675a7a8e57d8b4f8bf3bcb073fe6b879f7309c055996e051eb36cc5`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eaa4c3317aeec448940ff55356194c5de34d5d5ea2113e689b8dfc6cc65169`  
		Last Modified: Mon, 18 Jul 2022 22:19:10 GMT  
		Size: 1.4 MB (1358399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961740e547309d1bd3298dec9b78f143c42f08f9bdac3ce03bded0b6157c1787`  
		Last Modified: Mon, 18 Jul 2022 22:19:09 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca55d339fdc5ea0e18b66ac4f32d2170b2bdea7d444184792b0fd967cc34ef1`  
		Last Modified: Mon, 18 Jul 2022 22:19:09 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8c9be32912483c3d1874104ba9364eae2f6cc5a8e41d629c02aedce4b3a38c`  
		Last Modified: Mon, 18 Jul 2022 22:19:13 GMT  
		Size: 19.3 MB (19346880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c27463145e14b7eb1fae03941f74bf3a5ce1b7907fbde1f352429064c1d5031`  
		Last Modified: Mon, 18 Jul 2022 22:19:09 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:79728767115a191b17a69d129a65be1a067d5828bbf90d43e5833b92e2fe41b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115679783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23551a0cecc123712f378299710ae922fa0cb237e78e630aad050070f84ad943`
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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:40:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:40:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:40:47 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:40:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:40:50 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:50 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:40:51 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:40:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:53 GMT
CMD []
# Mon, 27 Jun 2022 19:41:01 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 27 Jun 2022 19:41:01 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 27 Jun 2022 19:41:02 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:41:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 27 Jun 2022 19:41:05 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 27 Jun 2022 19:41:06 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 27 Jun 2022 19:41:07 GMT
USER rootless
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c82eb82389bdb9c7d276b1643f13d3c5caae406cf7465fdc96939f266e6f12`  
		Last Modified: Mon, 27 Jun 2022 19:44:06 GMT  
		Size: 6.7 MB (6734644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bbc1c8669d112dd5ccbe24eae85fcf64a7e05164f1f15bda3f7af0bcbffbb6`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12b2450c676909ee9dae0cd4c9dde25caa5de2d4e5522a64aa5baf279120806`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 963.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17ce1449b637b669cb1dff1718ae17b979ff4efa77ec1fc72be0194468c9540`  
		Last Modified: Mon, 27 Jun 2022 19:44:04 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73afe9c1ea8a9add0560096dfa62e68214d911a898f87a2e607375f2fe5683eb`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 1.4 MB (1370343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ba1c6a8841b95b395c49b28169677c6307a3101e227708a700de94e9c8d0b2`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64830e281baf40fb6bf58458f881f01f312bda27135405c9b5546de5cabf49d`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28141130595ce38345733636d0d91f525fa08777adf2284bfce0a9c5236dab2d`  
		Last Modified: Mon, 27 Jun 2022 19:44:31 GMT  
		Size: 21.2 MB (21177072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fab70f37b78c4047be0923ffdada8d53cc2e47aa319d07b593475cc92dd034`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:47bd1331d72aebfee67194c4bebf45c0a6303b63755848ca98cce74b70ac44dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:a3cacd2bbc1d323daa79d5a8bda48305966261dbe791228dd6cffcd3e95e30f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101094335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c483e5e493f0032c1e9c95d8b4883431b6f5dd02d0bb185dc0a6d7809bd7ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:15:12 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Jul 2022 22:15:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:23 GMT
RUN apk add --no-cache git
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f712b6a4d7efecf0efa1961bf4e2fdc1859268c16db32d45fcfa7cc72abc20`  
		Last Modified: Mon, 18 Jul 2022 22:19:31 GMT  
		Size: 6.9 MB (6943682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:32f4c05237f4f02261aac5b4a0f970965a78dc3eba25ea432fd1b17f80838c61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93445547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc060a5a282fca1d0c38b4b1ccc8792e0c13d753ed216a66a9a87992cff14258`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:41:15 GMT
RUN apk add --no-cache git
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9d9fddd250721c2f847a9bbc6d46da61d812217213838e3879459cd5c1e2e7`  
		Last Modified: Mon, 27 Jun 2022 19:44:52 GMT  
		Size: 7.1 MB (7054457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore`

```console
$ docker pull docker@sha256:aa0b01f106685b0d0494aff223fcca039e507bf16c4859593b26714599074fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `docker:20.10-windowsservercore` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:7262b1947cffb1bf370d142eba1fc216dd59510b2f6af0bd9b43d4da8f5042db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353410338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96da4d70661fa4eac578cd29bb6e6f9ab0753d3b20202e726a3794d037979f56`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:11:48 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:11:49 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:12:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1da040c1cae02b726504c01ddb04ab6bc757384118e4997d2dc4b7e71fa76`  
		Last Modified: Wed, 13 Jul 2022 17:14:37 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd127957c40c6e903e73c2d36fd99a3937d8d4247d3068b446ae89771561f56`  
		Last Modified: Wed, 13 Jul 2022 17:14:38 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848a713cc66b0bd9b05ab1649d40f3a864c3557b09ee84feaf88a50bf9e71962`  
		Last Modified: Wed, 13 Jul 2022 17:14:48 GMT  
		Size: 52.5 MB (52520655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:d286ed6b7161125360b30763cddc35da6be81a4a8d40a46269788a647ab0b4a6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2724680561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00e049b0813b313a68cbcc666e527d2ee40c170b3c61f83c75952483ee5fbb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:13:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86af5967d42c804ec0ac2f177b83169359deede4dafa6dbfb40bc97aad7181`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d48e2e1c03a59c2bc5fa97787d608c1c56d2c5dea767bcb8266ece9c31be0`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f086bc01bdb19544655edff05b0730da6228f93c165306b8a1c2afbac5b4396`  
		Last Modified: Wed, 13 Jul 2022 17:15:11 GMT  
		Size: 52.3 MB (52281174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-1809`

```console
$ docker pull docker@sha256:c4c60a9bf7998d5b05c8c6d30644c7301e26edcba1ba9a13afbb4e8d372b9043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `docker:20.10-windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:d286ed6b7161125360b30763cddc35da6be81a4a8d40a46269788a647ab0b4a6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2724680561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00e049b0813b313a68cbcc666e527d2ee40c170b3c61f83c75952483ee5fbb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:13:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86af5967d42c804ec0ac2f177b83169359deede4dafa6dbfb40bc97aad7181`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d48e2e1c03a59c2bc5fa97787d608c1c56d2c5dea767bcb8266ece9c31be0`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f086bc01bdb19544655edff05b0730da6228f93c165306b8a1c2afbac5b4396`  
		Last Modified: Wed, 13 Jul 2022 17:15:11 GMT  
		Size: 52.3 MB (52281174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:b6f7a5dae2f95505f6fee244d4588441986227aeb49eda1e7bf8019a46da3957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `docker:20.10-windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:7262b1947cffb1bf370d142eba1fc216dd59510b2f6af0bd9b43d4da8f5042db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353410338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96da4d70661fa4eac578cd29bb6e6f9ab0753d3b20202e726a3794d037979f56`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:11:48 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:11:49 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:12:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1da040c1cae02b726504c01ddb04ab6bc757384118e4997d2dc4b7e71fa76`  
		Last Modified: Wed, 13 Jul 2022 17:14:37 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd127957c40c6e903e73c2d36fd99a3937d8d4247d3068b446ae89771561f56`  
		Last Modified: Wed, 13 Jul 2022 17:14:38 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848a713cc66b0bd9b05ab1649d40f3a864c3557b09ee84feaf88a50bf9e71962`  
		Last Modified: Wed, 13 Jul 2022 17:14:48 GMT  
		Size: 52.5 MB (52520655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17`

```console
$ docker pull docker@sha256:386dd216988a21c83233d32b3926300909a111fa73266d035e992280aa3a9e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.17` - linux; amd64

```console
$ docker pull docker@sha256:03b0716af18eedd4025b71c92fafcd09dd8cd4f020fd109284abc699983849c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94150653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283a30f3dbe83eba914a4aa16f95458512fa7799d177e069561e8e424f7f0fb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:15:12 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Jul 2022 22:15:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.17` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e76ec14a5acc9a9061233f0465f115b928de5c621ea85c2032ea9a5bb258e2e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86391090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0229d8a86a420066bf144bb1ef30a5a796ba08e3b84c35e8d1082ff5bc46b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-alpine3.16`

```console
$ docker pull docker@sha256:386dd216988a21c83233d32b3926300909a111fa73266d035e992280aa3a9e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.17-alpine3.16` - linux; amd64

```console
$ docker pull docker@sha256:03b0716af18eedd4025b71c92fafcd09dd8cd4f020fd109284abc699983849c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94150653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283a30f3dbe83eba914a4aa16f95458512fa7799d177e069561e8e424f7f0fb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:15:12 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Jul 2022 22:15:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.17-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e76ec14a5acc9a9061233f0465f115b928de5c621ea85c2032ea9a5bb258e2e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86391090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0229d8a86a420066bf144bb1ef30a5a796ba08e3b84c35e8d1082ff5bc46b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-dind`

```console
$ docker pull docker@sha256:70cd116f750841065b75efc37f92051894dd66d2893af0ac2b78c60eb9abe0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.17-dind` - linux; amd64

```console
$ docker pull docker@sha256:7c563086f2a9d640be3d723e9b0c0c5095de9844e7c0bdb0c042d769ff7ada80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101018932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07e77e26a3961cf233e96434f0473d09d3c5499c1927fb873936115e7f5c9d4`
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
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:03 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Jul 2022 22:16:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:04 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Jul 2022 22:16:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Jul 2022 22:16:05 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:16:05 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Jul 2022 22:16:05 GMT
EXPOSE 2375 2376
# Mon, 18 Jul 2022 22:16:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Jul 2022 22:16:05 GMT
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88901f96301057594237c9864b66f790ff7a5fef0c32a77d2ec663d644d45432`  
		Last Modified: Mon, 18 Jul 2022 22:18:50 GMT  
		Size: 6.9 MB (6863256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9991b1b34b037f21020309d31bd20f65cf695235ee4f3336717010d66bc9136e`  
		Last Modified: Mon, 18 Jul 2022 22:18:49 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f123d0d06ab3c31e76d283d36506013fad0ac3f4111bce66c1d0f030f47251e`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033c6a3c8675a7a8e57d8b4f8bf3bcb073fe6b879f7309c055996e051eb36cc5`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.17-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e51c69aca258a3bdf624db6685e328df185513577ac7b28dac10916816777d2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93130744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1490f7b533aeb3f1ee222cea8e688b5d6ca260444f849ecec19228e6882a81ba`
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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:40:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:40:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:40:47 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:40:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:40:50 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:50 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:40:51 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:40:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:53 GMT
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c82eb82389bdb9c7d276b1643f13d3c5caae406cf7465fdc96939f266e6f12`  
		Last Modified: Mon, 27 Jun 2022 19:44:06 GMT  
		Size: 6.7 MB (6734644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bbc1c8669d112dd5ccbe24eae85fcf64a7e05164f1f15bda3f7af0bcbffbb6`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12b2450c676909ee9dae0cd4c9dde25caa5de2d4e5522a64aa5baf279120806`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 963.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17ce1449b637b669cb1dff1718ae17b979ff4efa77ec1fc72be0194468c9540`  
		Last Modified: Mon, 27 Jun 2022 19:44:04 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-dind-alpine3.16`

```console
$ docker pull docker@sha256:70cd116f750841065b75efc37f92051894dd66d2893af0ac2b78c60eb9abe0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.17-dind-alpine3.16` - linux; amd64

```console
$ docker pull docker@sha256:7c563086f2a9d640be3d723e9b0c0c5095de9844e7c0bdb0c042d769ff7ada80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101018932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07e77e26a3961cf233e96434f0473d09d3c5499c1927fb873936115e7f5c9d4`
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
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:03 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Jul 2022 22:16:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:04 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Jul 2022 22:16:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Jul 2022 22:16:05 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:16:05 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Jul 2022 22:16:05 GMT
EXPOSE 2375 2376
# Mon, 18 Jul 2022 22:16:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Jul 2022 22:16:05 GMT
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88901f96301057594237c9864b66f790ff7a5fef0c32a77d2ec663d644d45432`  
		Last Modified: Mon, 18 Jul 2022 22:18:50 GMT  
		Size: 6.9 MB (6863256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9991b1b34b037f21020309d31bd20f65cf695235ee4f3336717010d66bc9136e`  
		Last Modified: Mon, 18 Jul 2022 22:18:49 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f123d0d06ab3c31e76d283d36506013fad0ac3f4111bce66c1d0f030f47251e`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033c6a3c8675a7a8e57d8b4f8bf3bcb073fe6b879f7309c055996e051eb36cc5`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.17-dind-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e51c69aca258a3bdf624db6685e328df185513577ac7b28dac10916816777d2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93130744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1490f7b533aeb3f1ee222cea8e688b5d6ca260444f849ecec19228e6882a81ba`
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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:40:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:40:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:40:47 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:40:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:40:50 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:50 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:40:51 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:40:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:53 GMT
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c82eb82389bdb9c7d276b1643f13d3c5caae406cf7465fdc96939f266e6f12`  
		Last Modified: Mon, 27 Jun 2022 19:44:06 GMT  
		Size: 6.7 MB (6734644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bbc1c8669d112dd5ccbe24eae85fcf64a7e05164f1f15bda3f7af0bcbffbb6`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12b2450c676909ee9dae0cd4c9dde25caa5de2d4e5522a64aa5baf279120806`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 963.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17ce1449b637b669cb1dff1718ae17b979ff4efa77ec1fc72be0194468c9540`  
		Last Modified: Mon, 27 Jun 2022 19:44:04 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-dind-rootless`

```console
$ docker pull docker@sha256:fc06ba995a9159944a5778145af22d7b3c5486f995c2e79f003d75fa5dfe30a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.17-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d6aac839f895a692d2bfa97f1c6092037b4affec034ede63afc8f5a3913bc4ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121725927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c4bb481982e73b10e8d9a47a9944a836e3193b95c6930b9ad4f9a86d2aa69e`
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
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:03 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Jul 2022 22:16:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:04 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Jul 2022 22:16:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Jul 2022 22:16:05 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:16:05 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Jul 2022 22:16:05 GMT
EXPOSE 2375 2376
# Mon, 18 Jul 2022 22:16:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Jul 2022 22:16:05 GMT
CMD []
# Mon, 18 Jul 2022 22:16:09 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 18 Jul 2022 22:16:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Jul 2022 22:16:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Jul 2022 22:16:19 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Jul 2022 22:16:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Jul 2022 22:16:19 GMT
USER rootless
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88901f96301057594237c9864b66f790ff7a5fef0c32a77d2ec663d644d45432`  
		Last Modified: Mon, 18 Jul 2022 22:18:50 GMT  
		Size: 6.9 MB (6863256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9991b1b34b037f21020309d31bd20f65cf695235ee4f3336717010d66bc9136e`  
		Last Modified: Mon, 18 Jul 2022 22:18:49 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f123d0d06ab3c31e76d283d36506013fad0ac3f4111bce66c1d0f030f47251e`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033c6a3c8675a7a8e57d8b4f8bf3bcb073fe6b879f7309c055996e051eb36cc5`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eaa4c3317aeec448940ff55356194c5de34d5d5ea2113e689b8dfc6cc65169`  
		Last Modified: Mon, 18 Jul 2022 22:19:10 GMT  
		Size: 1.4 MB (1358399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961740e547309d1bd3298dec9b78f143c42f08f9bdac3ce03bded0b6157c1787`  
		Last Modified: Mon, 18 Jul 2022 22:19:09 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca55d339fdc5ea0e18b66ac4f32d2170b2bdea7d444184792b0fd967cc34ef1`  
		Last Modified: Mon, 18 Jul 2022 22:19:09 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8c9be32912483c3d1874104ba9364eae2f6cc5a8e41d629c02aedce4b3a38c`  
		Last Modified: Mon, 18 Jul 2022 22:19:13 GMT  
		Size: 19.3 MB (19346880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c27463145e14b7eb1fae03941f74bf3a5ce1b7907fbde1f352429064c1d5031`  
		Last Modified: Mon, 18 Jul 2022 22:19:09 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.17-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:79728767115a191b17a69d129a65be1a067d5828bbf90d43e5833b92e2fe41b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115679783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23551a0cecc123712f378299710ae922fa0cb237e78e630aad050070f84ad943`
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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:40:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:40:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:40:47 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:40:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:40:50 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:50 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:40:51 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:40:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:53 GMT
CMD []
# Mon, 27 Jun 2022 19:41:01 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 27 Jun 2022 19:41:01 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 27 Jun 2022 19:41:02 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:41:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 27 Jun 2022 19:41:05 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 27 Jun 2022 19:41:06 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 27 Jun 2022 19:41:07 GMT
USER rootless
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c82eb82389bdb9c7d276b1643f13d3c5caae406cf7465fdc96939f266e6f12`  
		Last Modified: Mon, 27 Jun 2022 19:44:06 GMT  
		Size: 6.7 MB (6734644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bbc1c8669d112dd5ccbe24eae85fcf64a7e05164f1f15bda3f7af0bcbffbb6`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12b2450c676909ee9dae0cd4c9dde25caa5de2d4e5522a64aa5baf279120806`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 963.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17ce1449b637b669cb1dff1718ae17b979ff4efa77ec1fc72be0194468c9540`  
		Last Modified: Mon, 27 Jun 2022 19:44:04 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73afe9c1ea8a9add0560096dfa62e68214d911a898f87a2e607375f2fe5683eb`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 1.4 MB (1370343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ba1c6a8841b95b395c49b28169677c6307a3101e227708a700de94e9c8d0b2`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64830e281baf40fb6bf58458f881f01f312bda27135405c9b5546de5cabf49d`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28141130595ce38345733636d0d91f525fa08777adf2284bfce0a9c5236dab2d`  
		Last Modified: Mon, 27 Jun 2022 19:44:31 GMT  
		Size: 21.2 MB (21177072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fab70f37b78c4047be0923ffdada8d53cc2e47aa319d07b593475cc92dd034`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-git`

```console
$ docker pull docker@sha256:47bd1331d72aebfee67194c4bebf45c0a6303b63755848ca98cce74b70ac44dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.17-git` - linux; amd64

```console
$ docker pull docker@sha256:a3cacd2bbc1d323daa79d5a8bda48305966261dbe791228dd6cffcd3e95e30f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101094335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c483e5e493f0032c1e9c95d8b4883431b6f5dd02d0bb185dc0a6d7809bd7ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:15:12 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Jul 2022 22:15:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:23 GMT
RUN apk add --no-cache git
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f712b6a4d7efecf0efa1961bf4e2fdc1859268c16db32d45fcfa7cc72abc20`  
		Last Modified: Mon, 18 Jul 2022 22:19:31 GMT  
		Size: 6.9 MB (6943682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.17-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:32f4c05237f4f02261aac5b4a0f970965a78dc3eba25ea432fd1b17f80838c61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93445547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc060a5a282fca1d0c38b4b1ccc8792e0c13d753ed216a66a9a87992cff14258`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:41:15 GMT
RUN apk add --no-cache git
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9d9fddd250721c2f847a9bbc6d46da61d812217213838e3879459cd5c1e2e7`  
		Last Modified: Mon, 27 Jun 2022 19:44:52 GMT  
		Size: 7.1 MB (7054457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-windowsservercore`

```console
$ docker pull docker@sha256:aa0b01f106685b0d0494aff223fcca039e507bf16c4859593b26714599074fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `docker:20.10.17-windowsservercore` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:7262b1947cffb1bf370d142eba1fc216dd59510b2f6af0bd9b43d4da8f5042db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353410338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96da4d70661fa4eac578cd29bb6e6f9ab0753d3b20202e726a3794d037979f56`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:11:48 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:11:49 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:12:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1da040c1cae02b726504c01ddb04ab6bc757384118e4997d2dc4b7e71fa76`  
		Last Modified: Wed, 13 Jul 2022 17:14:37 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd127957c40c6e903e73c2d36fd99a3937d8d4247d3068b446ae89771561f56`  
		Last Modified: Wed, 13 Jul 2022 17:14:38 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848a713cc66b0bd9b05ab1649d40f3a864c3557b09ee84feaf88a50bf9e71962`  
		Last Modified: Wed, 13 Jul 2022 17:14:48 GMT  
		Size: 52.5 MB (52520655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.17-windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:d286ed6b7161125360b30763cddc35da6be81a4a8d40a46269788a647ab0b4a6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2724680561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00e049b0813b313a68cbcc666e527d2ee40c170b3c61f83c75952483ee5fbb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:13:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86af5967d42c804ec0ac2f177b83169359deede4dafa6dbfb40bc97aad7181`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d48e2e1c03a59c2bc5fa97787d608c1c56d2c5dea767bcb8266ece9c31be0`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f086bc01bdb19544655edff05b0730da6228f93c165306b8a1c2afbac5b4396`  
		Last Modified: Wed, 13 Jul 2022 17:15:11 GMT  
		Size: 52.3 MB (52281174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-windowsservercore-1809`

```console
$ docker pull docker@sha256:c4c60a9bf7998d5b05c8c6d30644c7301e26edcba1ba9a13afbb4e8d372b9043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `docker:20.10.17-windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:d286ed6b7161125360b30763cddc35da6be81a4a8d40a46269788a647ab0b4a6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2724680561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00e049b0813b313a68cbcc666e527d2ee40c170b3c61f83c75952483ee5fbb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:13:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86af5967d42c804ec0ac2f177b83169359deede4dafa6dbfb40bc97aad7181`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d48e2e1c03a59c2bc5fa97787d608c1c56d2c5dea767bcb8266ece9c31be0`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f086bc01bdb19544655edff05b0730da6228f93c165306b8a1c2afbac5b4396`  
		Last Modified: Wed, 13 Jul 2022 17:15:11 GMT  
		Size: 52.3 MB (52281174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:b6f7a5dae2f95505f6fee244d4588441986227aeb49eda1e7bf8019a46da3957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `docker:20.10.17-windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:7262b1947cffb1bf370d142eba1fc216dd59510b2f6af0bd9b43d4da8f5042db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353410338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96da4d70661fa4eac578cd29bb6e6f9ab0753d3b20202e726a3794d037979f56`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:11:48 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:11:49 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:12:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1da040c1cae02b726504c01ddb04ab6bc757384118e4997d2dc4b7e71fa76`  
		Last Modified: Wed, 13 Jul 2022 17:14:37 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd127957c40c6e903e73c2d36fd99a3937d8d4247d3068b446ae89771561f56`  
		Last Modified: Wed, 13 Jul 2022 17:14:38 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848a713cc66b0bd9b05ab1649d40f3a864c3557b09ee84feaf88a50bf9e71962`  
		Last Modified: Wed, 13 Jul 2022 17:14:48 GMT  
		Size: 52.5 MB (52520655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06-rc`

```console
$ docker pull docker@sha256:7194d6eede49cc84058559ac28820d4c8dfabc42d734d36a4757fe7e2972dec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:22.06-rc` - linux; amd64

```console
$ docker pull docker@sha256:e60a2ef7839c490329df49038cbe624a1763ba3f7b12d6f275caad4e801e258c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90677794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d93366468860c1a8d38c78e0e5ea4e17636cfb4068e1cdbecbfaa44328c30f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:22.06-rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9d35908c73010922d0ffb8239ff9578585ce853b936b4de9498ab8e14377ad44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83396179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c55de3815461863397eb345765493fce740ffec6f6be027356039f0fc081536`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:42:03 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 27 May 2022 00:42:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06-rc-dind`

```console
$ docker pull docker@sha256:57b84a62855eec3bffe815f131d23e35f14feb02408816afae2c81b60b44dbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:22.06-rc-dind` - linux; amd64

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

### `docker:22.06-rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c656a031df45b2fd53a01ae478adc91bb8fd593383d573e7a003a6b5781905e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90135836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdec5913ad3c2177d0869d6f152fa7ce8887f280f4673ef3ecc40b767070d1`
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
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:57 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:39:58 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:00 GMT
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461a7af5a02121a302d2e50704a0a555a028e64fe24cbfb84884f4122adbce70`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 6.7 MB (6734648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d0bb0a216f03245f2d6d1507fbe50b176695a523650d18aa9435dd1ad5b056`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e581a5e0448861bef772f9b7593e8e9c334ff3700e24a603534a348b485995`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 964.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ef26b393cbf609a417ec318bf7a20248b3b652ae0dd801b31240a9767d5eb2`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06-rc-dind-rootless`

```console
$ docker pull docker@sha256:09011d4928d29766051c316a04c0d4ab16fa95f698aea696f43afdbbc6eb6354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:22.06-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:8af640db63697b6a0559494e756a49f378aead7e0771e675c8fbf8e4dc0ef3f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118823979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77142a88cbb0b911fa4cb6564639cfde9030c5b68b37d1a2962e027bfa931128`
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
# Mon, 18 Jul 2022 22:15:33 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 18 Jul 2022 22:15:34 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Jul 2022 22:15:35 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:15:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Jul 2022 22:15:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Jul 2022 22:15:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Jul 2022 22:15:38 GMT
USER rootless
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
	-	`sha256:4ad59a92b8978d23c0d6c55d7e6ee9067f612b63c1ce6dab479ef80a345d582d`  
		Last Modified: Mon, 18 Jul 2022 22:17:46 GMT  
		Size: 1.4 MB (1358397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bcb6f1b075953cacd6f229c90efb7d2f056da898ba81378e7f068c91c9540b`  
		Last Modified: Mon, 18 Jul 2022 22:17:45 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5551ff5b4c4001b50fb7baa0e5abe92ecd7692295631b2debff42273cb68b03b`  
		Last Modified: Mon, 18 Jul 2022 22:17:45 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0991d23110a3adeff3066b429fdbb09ba97670d611b097f2307eb41455ba2a6`  
		Last Modified: Mon, 18 Jul 2022 22:17:49 GMT  
		Size: 19.9 MB (19917858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129af77ff56b315f6e69a45db23206f6ef143dae3a3e04fdb0b6c2136547092f`  
		Last Modified: Mon, 18 Jul 2022 22:17:46 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:22.06-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b0e236d972dd893b17074bae4d2136f17ac035d5f525e81b6b15d11af9eef7e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113395176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5031b56c49046f970499d34570766b5eb9af875807acbb213609604dfe8d4f9d`
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
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:57 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:39:58 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:00 GMT
CMD []
# Mon, 27 Jun 2022 19:40:08 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 27 Jun 2022 19:40:08 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 27 Jun 2022 19:40:09 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:40:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 27 Jun 2022 19:40:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 27 Jun 2022 19:40:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 27 Jun 2022 19:40:15 GMT
USER rootless
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461a7af5a02121a302d2e50704a0a555a028e64fe24cbfb84884f4122adbce70`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 6.7 MB (6734648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d0bb0a216f03245f2d6d1507fbe50b176695a523650d18aa9435dd1ad5b056`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e581a5e0448861bef772f9b7593e8e9c334ff3700e24a603534a348b485995`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 964.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ef26b393cbf609a417ec318bf7a20248b3b652ae0dd801b31240a9767d5eb2`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb81cd00d951430d0d6a10659f3cc595a956259be8873d793585d2338219ba6a`  
		Last Modified: Mon, 27 Jun 2022 19:43:08 GMT  
		Size: 1.4 MB (1370340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe035b69142cb3e2217653d63a0847885a13030bf1a65e774a379ca934d7268`  
		Last Modified: Mon, 27 Jun 2022 19:43:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354159b9f8e77204c8a136be72ff2630314987acbfb05bad82def89c68ead49f`  
		Last Modified: Mon, 27 Jun 2022 19:43:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5901fdfbac1923f4024314e677b4f31e53a8e7a19f3eafdcae185428f768aef5`  
		Last Modified: Mon, 27 Jun 2022 19:43:11 GMT  
		Size: 21.9 MB (21887381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7901c23f8491a677237a7698774bf57b4e95c6b9de321952a74a186de30c7948`  
		Last Modified: Mon, 27 Jun 2022 19:43:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06-rc-git`

```console
$ docker pull docker@sha256:b36802aae7c9718573516031bc675ad017c1b0fd79521900e62384bd12d87861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:22.06-rc-git` - linux; amd64

```console
$ docker pull docker@sha256:413c8a5dc862d1d85ae1474b18ab671a236fbc05eba8b168a489423de080f96d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97621472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ca41888a2c5d5d63f0780a05897b6ba402930ac943d0b61f82510615022e0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Mon, 18 Jul 2022 22:15:42 GMT
RUN apk add --no-cache git
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
	-	`sha256:b6364ecd6bc81eb855021d5d56c8cf4f669eaee31c754affc91a381e965ae9c7`  
		Last Modified: Mon, 18 Jul 2022 22:18:03 GMT  
		Size: 6.9 MB (6943678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:22.06-rc-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:69c954b769b9014dc73efd4cf3cf7c7a54518271dfd0c7556caa01a6430c29f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90450634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f0fab2c694c55846599e01b9f69c04153ecd1994066217e458eefc35ab925f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:42:03 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 27 May 2022 00:42:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:40:22 GMT
RUN apk add --no-cache git
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a306f45f18ccb9a32f7f2b7fbe663bca6648af057abb4defe68aad16b886e9`  
		Last Modified: Mon, 27 Jun 2022 19:43:28 GMT  
		Size: 7.1 MB (7054455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06-rc-windowsservercore`

```console
$ docker pull docker@sha256:a715787594b32b9cdb188adb4bd34f591f6d1157320936b5f029237cb698bb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `docker:22.06-rc-windowsservercore` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:21894d75dc7ad7b1128482f6ee9f6d940927c986213c3957180da2d19f23185b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310655058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397dfb1ed2fda6c7862c1fd0893a8349cac1129c0040c28013b1a0dab7e2608e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:09:15 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:09:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:09:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b7d5cf167dc176e16f7f47520ad35fb27c5d9b4adbcca6204a3d8fe6e6b5ee`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9504b70312192db63cb4837d1adcd0aec44b658f596d069f409787f9c055c0`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e945f6d7d36e52540a1c818463f967d23624fe79480e55f162e0f4262c9a3feb`  
		Last Modified: Wed, 13 Jul 2022 17:14:08 GMT  
		Size: 9.8 MB (9765370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:22.06-rc-windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:11e833c8880b2318e4f0f2c161c7ecf04ec129277ae8d9040971b04185b53b04
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2681925749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4e2c4281dbb643e4ea2b0ae3993b6652eb026718c537c2223dc3d607bb1de7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:10:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:10:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:11:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca49c3d0f1b10ab622d1ad62fdff5b201db2b1b5d796919f0d74b70a933b6a2`  
		Last Modified: Wed, 13 Jul 2022 17:14:21 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadd2a4879da5a12799c4722e6d956052140ab1b2c9246ade10879c43a875d98`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd78d697ed3fbe490f2c2eab2f6d2591b4205efc5b6c041f7b6853dcebd8d154`  
		Last Modified: Wed, 13 Jul 2022 17:14:24 GMT  
		Size: 9.5 MB (9526144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:35d815c0f33797de72b554f4b54011993fc220a443932c9d7a57ec5b5e1ff5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `docker:22.06-rc-windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:11e833c8880b2318e4f0f2c161c7ecf04ec129277ae8d9040971b04185b53b04
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2681925749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4e2c4281dbb643e4ea2b0ae3993b6652eb026718c537c2223dc3d607bb1de7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:10:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:10:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:11:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca49c3d0f1b10ab622d1ad62fdff5b201db2b1b5d796919f0d74b70a933b6a2`  
		Last Modified: Wed, 13 Jul 2022 17:14:21 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadd2a4879da5a12799c4722e6d956052140ab1b2c9246ade10879c43a875d98`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd78d697ed3fbe490f2c2eab2f6d2591b4205efc5b6c041f7b6853dcebd8d154`  
		Last Modified: Wed, 13 Jul 2022 17:14:24 GMT  
		Size: 9.5 MB (9526144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:e12c921c0f72f0dcfac2205e0ad1d7f7bc4c3258faf7040f02467314fb48c3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `docker:22.06-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:21894d75dc7ad7b1128482f6ee9f6d940927c986213c3957180da2d19f23185b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310655058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397dfb1ed2fda6c7862c1fd0893a8349cac1129c0040c28013b1a0dab7e2608e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:09:15 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:09:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:09:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b7d5cf167dc176e16f7f47520ad35fb27c5d9b4adbcca6204a3d8fe6e6b5ee`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9504b70312192db63cb4837d1adcd0aec44b658f596d069f409787f9c055c0`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e945f6d7d36e52540a1c818463f967d23624fe79480e55f162e0f4262c9a3feb`  
		Last Modified: Wed, 13 Jul 2022 17:14:08 GMT  
		Size: 9.8 MB (9765370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06.0-beta.0`

```console
$ docker pull docker@sha256:7194d6eede49cc84058559ac28820d4c8dfabc42d734d36a4757fe7e2972dec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:22.06.0-beta.0` - linux; amd64

```console
$ docker pull docker@sha256:e60a2ef7839c490329df49038cbe624a1763ba3f7b12d6f275caad4e801e258c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90677794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d93366468860c1a8d38c78e0e5ea4e17636cfb4068e1cdbecbfaa44328c30f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:22.06.0-beta.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9d35908c73010922d0ffb8239ff9578585ce853b936b4de9498ab8e14377ad44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83396179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c55de3815461863397eb345765493fce740ffec6f6be027356039f0fc081536`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:42:03 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 27 May 2022 00:42:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06.0-beta.0-alpine3.16`

```console
$ docker pull docker@sha256:7194d6eede49cc84058559ac28820d4c8dfabc42d734d36a4757fe7e2972dec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:22.06.0-beta.0-alpine3.16` - linux; amd64

```console
$ docker pull docker@sha256:e60a2ef7839c490329df49038cbe624a1763ba3f7b12d6f275caad4e801e258c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90677794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d93366468860c1a8d38c78e0e5ea4e17636cfb4068e1cdbecbfaa44328c30f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:22.06.0-beta.0-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9d35908c73010922d0ffb8239ff9578585ce853b936b4de9498ab8e14377ad44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83396179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c55de3815461863397eb345765493fce740ffec6f6be027356039f0fc081536`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:42:03 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 27 May 2022 00:42:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06.0-beta.0-dind`

```console
$ docker pull docker@sha256:57b84a62855eec3bffe815f131d23e35f14feb02408816afae2c81b60b44dbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:22.06.0-beta.0-dind` - linux; amd64

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

### `docker:22.06.0-beta.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c656a031df45b2fd53a01ae478adc91bb8fd593383d573e7a003a6b5781905e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90135836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdec5913ad3c2177d0869d6f152fa7ce8887f280f4673ef3ecc40b767070d1`
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
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:57 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:39:58 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:00 GMT
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461a7af5a02121a302d2e50704a0a555a028e64fe24cbfb84884f4122adbce70`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 6.7 MB (6734648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d0bb0a216f03245f2d6d1507fbe50b176695a523650d18aa9435dd1ad5b056`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e581a5e0448861bef772f9b7593e8e9c334ff3700e24a603534a348b485995`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 964.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ef26b393cbf609a417ec318bf7a20248b3b652ae0dd801b31240a9767d5eb2`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06.0-beta.0-dind-alpine3.16`

```console
$ docker pull docker@sha256:57b84a62855eec3bffe815f131d23e35f14feb02408816afae2c81b60b44dbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:22.06.0-beta.0-dind-alpine3.16` - linux; amd64

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

### `docker:22.06.0-beta.0-dind-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c656a031df45b2fd53a01ae478adc91bb8fd593383d573e7a003a6b5781905e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90135836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdec5913ad3c2177d0869d6f152fa7ce8887f280f4673ef3ecc40b767070d1`
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
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:57 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:39:58 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:00 GMT
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461a7af5a02121a302d2e50704a0a555a028e64fe24cbfb84884f4122adbce70`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 6.7 MB (6734648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d0bb0a216f03245f2d6d1507fbe50b176695a523650d18aa9435dd1ad5b056`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e581a5e0448861bef772f9b7593e8e9c334ff3700e24a603534a348b485995`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 964.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ef26b393cbf609a417ec318bf7a20248b3b652ae0dd801b31240a9767d5eb2`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06.0-beta.0-dind-rootless`

```console
$ docker pull docker@sha256:09011d4928d29766051c316a04c0d4ab16fa95f698aea696f43afdbbc6eb6354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:22.06.0-beta.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:8af640db63697b6a0559494e756a49f378aead7e0771e675c8fbf8e4dc0ef3f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118823979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77142a88cbb0b911fa4cb6564639cfde9030c5b68b37d1a2962e027bfa931128`
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
# Mon, 18 Jul 2022 22:15:33 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 18 Jul 2022 22:15:34 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Jul 2022 22:15:35 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:15:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Jul 2022 22:15:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Jul 2022 22:15:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Jul 2022 22:15:38 GMT
USER rootless
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
	-	`sha256:4ad59a92b8978d23c0d6c55d7e6ee9067f612b63c1ce6dab479ef80a345d582d`  
		Last Modified: Mon, 18 Jul 2022 22:17:46 GMT  
		Size: 1.4 MB (1358397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bcb6f1b075953cacd6f229c90efb7d2f056da898ba81378e7f068c91c9540b`  
		Last Modified: Mon, 18 Jul 2022 22:17:45 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5551ff5b4c4001b50fb7baa0e5abe92ecd7692295631b2debff42273cb68b03b`  
		Last Modified: Mon, 18 Jul 2022 22:17:45 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0991d23110a3adeff3066b429fdbb09ba97670d611b097f2307eb41455ba2a6`  
		Last Modified: Mon, 18 Jul 2022 22:17:49 GMT  
		Size: 19.9 MB (19917858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129af77ff56b315f6e69a45db23206f6ef143dae3a3e04fdb0b6c2136547092f`  
		Last Modified: Mon, 18 Jul 2022 22:17:46 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:22.06.0-beta.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b0e236d972dd893b17074bae4d2136f17ac035d5f525e81b6b15d11af9eef7e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113395176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5031b56c49046f970499d34570766b5eb9af875807acbb213609604dfe8d4f9d`
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
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:57 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:39:58 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:00 GMT
CMD []
# Mon, 27 Jun 2022 19:40:08 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 27 Jun 2022 19:40:08 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 27 Jun 2022 19:40:09 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:40:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 27 Jun 2022 19:40:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 27 Jun 2022 19:40:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 27 Jun 2022 19:40:15 GMT
USER rootless
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461a7af5a02121a302d2e50704a0a555a028e64fe24cbfb84884f4122adbce70`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 6.7 MB (6734648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d0bb0a216f03245f2d6d1507fbe50b176695a523650d18aa9435dd1ad5b056`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e581a5e0448861bef772f9b7593e8e9c334ff3700e24a603534a348b485995`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 964.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ef26b393cbf609a417ec318bf7a20248b3b652ae0dd801b31240a9767d5eb2`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb81cd00d951430d0d6a10659f3cc595a956259be8873d793585d2338219ba6a`  
		Last Modified: Mon, 27 Jun 2022 19:43:08 GMT  
		Size: 1.4 MB (1370340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe035b69142cb3e2217653d63a0847885a13030bf1a65e774a379ca934d7268`  
		Last Modified: Mon, 27 Jun 2022 19:43:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354159b9f8e77204c8a136be72ff2630314987acbfb05bad82def89c68ead49f`  
		Last Modified: Mon, 27 Jun 2022 19:43:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5901fdfbac1923f4024314e677b4f31e53a8e7a19f3eafdcae185428f768aef5`  
		Last Modified: Mon, 27 Jun 2022 19:43:11 GMT  
		Size: 21.9 MB (21887381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7901c23f8491a677237a7698774bf57b4e95c6b9de321952a74a186de30c7948`  
		Last Modified: Mon, 27 Jun 2022 19:43:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06.0-beta.0-git`

```console
$ docker pull docker@sha256:b36802aae7c9718573516031bc675ad017c1b0fd79521900e62384bd12d87861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:22.06.0-beta.0-git` - linux; amd64

```console
$ docker pull docker@sha256:413c8a5dc862d1d85ae1474b18ab671a236fbc05eba8b168a489423de080f96d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97621472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ca41888a2c5d5d63f0780a05897b6ba402930ac943d0b61f82510615022e0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Mon, 18 Jul 2022 22:15:42 GMT
RUN apk add --no-cache git
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
	-	`sha256:b6364ecd6bc81eb855021d5d56c8cf4f669eaee31c754affc91a381e965ae9c7`  
		Last Modified: Mon, 18 Jul 2022 22:18:03 GMT  
		Size: 6.9 MB (6943678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:22.06.0-beta.0-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:69c954b769b9014dc73efd4cf3cf7c7a54518271dfd0c7556caa01a6430c29f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90450634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f0fab2c694c55846599e01b9f69c04153ecd1994066217e458eefc35ab925f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:42:03 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 27 May 2022 00:42:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:40:22 GMT
RUN apk add --no-cache git
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a306f45f18ccb9a32f7f2b7fbe663bca6648af057abb4defe68aad16b886e9`  
		Last Modified: Mon, 27 Jun 2022 19:43:28 GMT  
		Size: 7.1 MB (7054455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06.0-beta.0-windowsservercore`

```console
$ docker pull docker@sha256:a715787594b32b9cdb188adb4bd34f591f6d1157320936b5f029237cb698bb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `docker:22.06.0-beta.0-windowsservercore` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:21894d75dc7ad7b1128482f6ee9f6d940927c986213c3957180da2d19f23185b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310655058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397dfb1ed2fda6c7862c1fd0893a8349cac1129c0040c28013b1a0dab7e2608e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:09:15 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:09:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:09:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b7d5cf167dc176e16f7f47520ad35fb27c5d9b4adbcca6204a3d8fe6e6b5ee`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9504b70312192db63cb4837d1adcd0aec44b658f596d069f409787f9c055c0`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e945f6d7d36e52540a1c818463f967d23624fe79480e55f162e0f4262c9a3feb`  
		Last Modified: Wed, 13 Jul 2022 17:14:08 GMT  
		Size: 9.8 MB (9765370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:22.06.0-beta.0-windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:11e833c8880b2318e4f0f2c161c7ecf04ec129277ae8d9040971b04185b53b04
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2681925749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4e2c4281dbb643e4ea2b0ae3993b6652eb026718c537c2223dc3d607bb1de7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:10:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:10:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:11:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca49c3d0f1b10ab622d1ad62fdff5b201db2b1b5d796919f0d74b70a933b6a2`  
		Last Modified: Wed, 13 Jul 2022 17:14:21 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadd2a4879da5a12799c4722e6d956052140ab1b2c9246ade10879c43a875d98`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd78d697ed3fbe490f2c2eab2f6d2591b4205efc5b6c041f7b6853dcebd8d154`  
		Last Modified: Wed, 13 Jul 2022 17:14:24 GMT  
		Size: 9.5 MB (9526144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06.0-beta.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:35d815c0f33797de72b554f4b54011993fc220a443932c9d7a57ec5b5e1ff5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `docker:22.06.0-beta.0-windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:11e833c8880b2318e4f0f2c161c7ecf04ec129277ae8d9040971b04185b53b04
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2681925749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4e2c4281dbb643e4ea2b0ae3993b6652eb026718c537c2223dc3d607bb1de7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:10:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:10:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:11:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca49c3d0f1b10ab622d1ad62fdff5b201db2b1b5d796919f0d74b70a933b6a2`  
		Last Modified: Wed, 13 Jul 2022 17:14:21 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadd2a4879da5a12799c4722e6d956052140ab1b2c9246ade10879c43a875d98`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd78d697ed3fbe490f2c2eab2f6d2591b4205efc5b6c041f7b6853dcebd8d154`  
		Last Modified: Wed, 13 Jul 2022 17:14:24 GMT  
		Size: 9.5 MB (9526144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06.0-beta.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:e12c921c0f72f0dcfac2205e0ad1d7f7bc4c3258faf7040f02467314fb48c3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `docker:22.06.0-beta.0-windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:21894d75dc7ad7b1128482f6ee9f6d940927c986213c3957180da2d19f23185b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310655058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397dfb1ed2fda6c7862c1fd0893a8349cac1129c0040c28013b1a0dab7e2608e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:09:15 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:09:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:09:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b7d5cf167dc176e16f7f47520ad35fb27c5d9b4adbcca6204a3d8fe6e6b5ee`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9504b70312192db63cb4837d1adcd0aec44b658f596d069f409787f9c055c0`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e945f6d7d36e52540a1c818463f967d23624fe79480e55f162e0f4262c9a3feb`  
		Last Modified: Wed, 13 Jul 2022 17:14:08 GMT  
		Size: 9.8 MB (9765370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:70cd116f750841065b75efc37f92051894dd66d2893af0ac2b78c60eb9abe0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:7c563086f2a9d640be3d723e9b0c0c5095de9844e7c0bdb0c042d769ff7ada80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101018932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07e77e26a3961cf233e96434f0473d09d3c5499c1927fb873936115e7f5c9d4`
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
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:03 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Jul 2022 22:16:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:04 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Jul 2022 22:16:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Jul 2022 22:16:05 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:16:05 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Jul 2022 22:16:05 GMT
EXPOSE 2375 2376
# Mon, 18 Jul 2022 22:16:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Jul 2022 22:16:05 GMT
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88901f96301057594237c9864b66f790ff7a5fef0c32a77d2ec663d644d45432`  
		Last Modified: Mon, 18 Jul 2022 22:18:50 GMT  
		Size: 6.9 MB (6863256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9991b1b34b037f21020309d31bd20f65cf695235ee4f3336717010d66bc9136e`  
		Last Modified: Mon, 18 Jul 2022 22:18:49 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f123d0d06ab3c31e76d283d36506013fad0ac3f4111bce66c1d0f030f47251e`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033c6a3c8675a7a8e57d8b4f8bf3bcb073fe6b879f7309c055996e051eb36cc5`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e51c69aca258a3bdf624db6685e328df185513577ac7b28dac10916816777d2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93130744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1490f7b533aeb3f1ee222cea8e688b5d6ca260444f849ecec19228e6882a81ba`
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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:40:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:40:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:40:47 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:40:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:40:50 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:50 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:40:51 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:40:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:53 GMT
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c82eb82389bdb9c7d276b1643f13d3c5caae406cf7465fdc96939f266e6f12`  
		Last Modified: Mon, 27 Jun 2022 19:44:06 GMT  
		Size: 6.7 MB (6734644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bbc1c8669d112dd5ccbe24eae85fcf64a7e05164f1f15bda3f7af0bcbffbb6`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12b2450c676909ee9dae0cd4c9dde25caa5de2d4e5522a64aa5baf279120806`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 963.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17ce1449b637b669cb1dff1718ae17b979ff4efa77ec1fc72be0194468c9540`  
		Last Modified: Mon, 27 Jun 2022 19:44:04 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:fc06ba995a9159944a5778145af22d7b3c5486f995c2e79f003d75fa5dfe30a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d6aac839f895a692d2bfa97f1c6092037b4affec034ede63afc8f5a3913bc4ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121725927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c4bb481982e73b10e8d9a47a9944a836e3193b95c6930b9ad4f9a86d2aa69e`
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
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:03 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 18 Jul 2022 22:16:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:04 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 18 Jul 2022 22:16:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 18 Jul 2022 22:16:05 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:16:05 GMT
VOLUME [/var/lib/docker]
# Mon, 18 Jul 2022 22:16:05 GMT
EXPOSE 2375 2376
# Mon, 18 Jul 2022 22:16:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 18 Jul 2022 22:16:05 GMT
CMD []
# Mon, 18 Jul 2022 22:16:09 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 18 Jul 2022 22:16:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Jul 2022 22:16:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:16:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Jul 2022 22:16:19 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Jul 2022 22:16:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Jul 2022 22:16:19 GMT
USER rootless
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88901f96301057594237c9864b66f790ff7a5fef0c32a77d2ec663d644d45432`  
		Last Modified: Mon, 18 Jul 2022 22:18:50 GMT  
		Size: 6.9 MB (6863256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9991b1b34b037f21020309d31bd20f65cf695235ee4f3336717010d66bc9136e`  
		Last Modified: Mon, 18 Jul 2022 22:18:49 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f123d0d06ab3c31e76d283d36506013fad0ac3f4111bce66c1d0f030f47251e`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033c6a3c8675a7a8e57d8b4f8bf3bcb073fe6b879f7309c055996e051eb36cc5`  
		Last Modified: Mon, 18 Jul 2022 22:18:48 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eaa4c3317aeec448940ff55356194c5de34d5d5ea2113e689b8dfc6cc65169`  
		Last Modified: Mon, 18 Jul 2022 22:19:10 GMT  
		Size: 1.4 MB (1358399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961740e547309d1bd3298dec9b78f143c42f08f9bdac3ce03bded0b6157c1787`  
		Last Modified: Mon, 18 Jul 2022 22:19:09 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca55d339fdc5ea0e18b66ac4f32d2170b2bdea7d444184792b0fd967cc34ef1`  
		Last Modified: Mon, 18 Jul 2022 22:19:09 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8c9be32912483c3d1874104ba9364eae2f6cc5a8e41d629c02aedce4b3a38c`  
		Last Modified: Mon, 18 Jul 2022 22:19:13 GMT  
		Size: 19.3 MB (19346880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c27463145e14b7eb1fae03941f74bf3a5ce1b7907fbde1f352429064c1d5031`  
		Last Modified: Mon, 18 Jul 2022 22:19:09 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:79728767115a191b17a69d129a65be1a067d5828bbf90d43e5833b92e2fe41b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115679783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23551a0cecc123712f378299710ae922fa0cb237e78e630aad050070f84ad943`
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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:40:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:40:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:40:47 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:40:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:40:50 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:50 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:40:51 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:40:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:53 GMT
CMD []
# Mon, 27 Jun 2022 19:41:01 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 27 Jun 2022 19:41:01 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 27 Jun 2022 19:41:02 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:41:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 27 Jun 2022 19:41:05 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 27 Jun 2022 19:41:06 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 27 Jun 2022 19:41:07 GMT
USER rootless
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c82eb82389bdb9c7d276b1643f13d3c5caae406cf7465fdc96939f266e6f12`  
		Last Modified: Mon, 27 Jun 2022 19:44:06 GMT  
		Size: 6.7 MB (6734644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bbc1c8669d112dd5ccbe24eae85fcf64a7e05164f1f15bda3f7af0bcbffbb6`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12b2450c676909ee9dae0cd4c9dde25caa5de2d4e5522a64aa5baf279120806`  
		Last Modified: Mon, 27 Jun 2022 19:44:05 GMT  
		Size: 963.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17ce1449b637b669cb1dff1718ae17b979ff4efa77ec1fc72be0194468c9540`  
		Last Modified: Mon, 27 Jun 2022 19:44:04 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73afe9c1ea8a9add0560096dfa62e68214d911a898f87a2e607375f2fe5683eb`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 1.4 MB (1370343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ba1c6a8841b95b395c49b28169677c6307a3101e227708a700de94e9c8d0b2`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64830e281baf40fb6bf58458f881f01f312bda27135405c9b5546de5cabf49d`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28141130595ce38345733636d0d91f525fa08777adf2284bfce0a9c5236dab2d`  
		Last Modified: Mon, 27 Jun 2022 19:44:31 GMT  
		Size: 21.2 MB (21177072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fab70f37b78c4047be0923ffdada8d53cc2e47aa319d07b593475cc92dd034`  
		Last Modified: Mon, 27 Jun 2022 19:44:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:47bd1331d72aebfee67194c4bebf45c0a6303b63755848ca98cce74b70ac44dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:a3cacd2bbc1d323daa79d5a8bda48305966261dbe791228dd6cffcd3e95e30f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101094335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c483e5e493f0032c1e9c95d8b4883431b6f5dd02d0bb185dc0a6d7809bd7ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:15:12 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Jul 2022 22:15:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
# Mon, 18 Jul 2022 22:16:23 GMT
RUN apk add --no-cache git
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f712b6a4d7efecf0efa1961bf4e2fdc1859268c16db32d45fcfa7cc72abc20`  
		Last Modified: Mon, 18 Jul 2022 22:19:31 GMT  
		Size: 6.9 MB (6943682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:32f4c05237f4f02261aac5b4a0f970965a78dc3eba25ea432fd1b17f80838c61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93445547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc060a5a282fca1d0c38b4b1ccc8792e0c13d753ed216a66a9a87992cff14258`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:41:15 GMT
RUN apk add --no-cache git
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9d9fddd250721c2f847a9bbc6d46da61d812217213838e3879459cd5c1e2e7`  
		Last Modified: Mon, 27 Jun 2022 19:44:52 GMT  
		Size: 7.1 MB (7054457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:386dd216988a21c83233d32b3926300909a111fa73266d035e992280aa3a9e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:03b0716af18eedd4025b71c92fafcd09dd8cd4f020fd109284abc699983849c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94150653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283a30f3dbe83eba914a4aa16f95458512fa7799d177e069561e8e424f7f0fb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:15:12 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Jul 2022 22:15:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 18 Jul 2022 22:15:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 18 Jul 2022 22:15:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 18 Jul 2022 22:15:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 18 Jul 2022 22:15:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 18 Jul 2022 22:15:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 18 Jul 2022 22:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 22:15:57 GMT
CMD ["sh"]
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
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95599a9e53e6774985f9ebff9d2c7a356f3b79c17dd25ae32812aa6803771458`  
		Last Modified: Mon, 18 Jul 2022 22:18:17 GMT  
		Size: 9.4 MB (9362929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0352047eb1cec0134c9d27c026929a45e8ca1337abb0cdbaa9250928f977de`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4b14e1f9dee487e532bc8858a04fc2dc7c1975d24b67718d9518cbb822cf8a`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6861ad1ee882d59f537543ae6dc117feadaa8a99e54af7d5488f72977f826cc`  
		Last Modified: Mon, 18 Jul 2022 22:18:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e76ec14a5acc9a9061233f0465f115b928de5c621ea85c2032ea9a5bb258e2e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86391090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0229d8a86a420066bf144bb1ef30a5a796ba08e3b84c35e8d1082ff5bc46b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Mon, 27 Jun 2022 19:40:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:40:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:40:32 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:40:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:40:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:40:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:40:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:36 GMT
CMD ["sh"]
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
	-	`sha256:1f160187a62e1b649c0d32c9af1c12aaf377e1a55a966ddbcce7ab48eff550cf`  
		Last Modified: Mon, 27 Jun 2022 19:43:44 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb4f2231cc40657d523a7139d6058b16f8aa0ae3cd70eb599be2335399d6812`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57f8edcb1810114c6447d0de3ac17bb8f2fd04a1e4ce01bbf97b9ff89ec5f5`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32406cfcb79f2d4b1a7d7e63e3ef70119cdca171feea62f1c874636771f0650a`  
		Last Modified: Mon, 27 Jun 2022 19:43:42 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc`

```console
$ docker pull docker@sha256:7194d6eede49cc84058559ac28820d4c8dfabc42d734d36a4757fe7e2972dec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc` - linux; amd64

```console
$ docker pull docker@sha256:e60a2ef7839c490329df49038cbe624a1763ba3f7b12d6f275caad4e801e258c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90677794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d93366468860c1a8d38c78e0e5ea4e17636cfb4068e1cdbecbfaa44328c30f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9d35908c73010922d0ffb8239ff9578585ce853b936b4de9498ab8e14377ad44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83396179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c55de3815461863397eb345765493fce740ffec6f6be027356039f0fc081536`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:42:03 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 27 May 2022 00:42:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-dind`

```console
$ docker pull docker@sha256:57b84a62855eec3bffe815f131d23e35f14feb02408816afae2c81b60b44dbb3
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
$ docker pull docker@sha256:c656a031df45b2fd53a01ae478adc91bb8fd593383d573e7a003a6b5781905e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90135836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdec5913ad3c2177d0869d6f152fa7ce8887f280f4673ef3ecc40b767070d1`
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
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:57 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:39:58 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:00 GMT
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461a7af5a02121a302d2e50704a0a555a028e64fe24cbfb84884f4122adbce70`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 6.7 MB (6734648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d0bb0a216f03245f2d6d1507fbe50b176695a523650d18aa9435dd1ad5b056`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e581a5e0448861bef772f9b7593e8e9c334ff3700e24a603534a348b485995`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 964.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ef26b393cbf609a417ec318bf7a20248b3b652ae0dd801b31240a9767d5eb2`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:09011d4928d29766051c316a04c0d4ab16fa95f698aea696f43afdbbc6eb6354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:8af640db63697b6a0559494e756a49f378aead7e0771e675c8fbf8e4dc0ef3f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118823979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77142a88cbb0b911fa4cb6564639cfde9030c5b68b37d1a2962e027bfa931128`
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
# Mon, 18 Jul 2022 22:15:33 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 18 Jul 2022 22:15:34 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 18 Jul 2022 22:15:35 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 18 Jul 2022 22:15:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 18 Jul 2022 22:15:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 18 Jul 2022 22:15:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 18 Jul 2022 22:15:38 GMT
USER rootless
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
	-	`sha256:4ad59a92b8978d23c0d6c55d7e6ee9067f612b63c1ce6dab479ef80a345d582d`  
		Last Modified: Mon, 18 Jul 2022 22:17:46 GMT  
		Size: 1.4 MB (1358397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bcb6f1b075953cacd6f229c90efb7d2f056da898ba81378e7f068c91c9540b`  
		Last Modified: Mon, 18 Jul 2022 22:17:45 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5551ff5b4c4001b50fb7baa0e5abe92ecd7692295631b2debff42273cb68b03b`  
		Last Modified: Mon, 18 Jul 2022 22:17:45 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0991d23110a3adeff3066b429fdbb09ba97670d611b097f2307eb41455ba2a6`  
		Last Modified: Mon, 18 Jul 2022 22:17:49 GMT  
		Size: 19.9 MB (19917858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129af77ff56b315f6e69a45db23206f6ef143dae3a3e04fdb0b6c2136547092f`  
		Last Modified: Mon, 18 Jul 2022 22:17:46 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b0e236d972dd893b17074bae4d2136f17ac035d5f525e81b6b15d11af9eef7e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113395176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5031b56c49046f970499d34570766b5eb9af875807acbb213609604dfe8d4f9d`
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
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 27 Jun 2022 19:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:39:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 27 Jun 2022 19:39:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 27 Jun 2022 19:39:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:57 GMT
VOLUME [/var/lib/docker]
# Mon, 27 Jun 2022 19:39:58 GMT
EXPOSE 2375 2376
# Mon, 27 Jun 2022 19:39:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 27 Jun 2022 19:40:00 GMT
CMD []
# Mon, 27 Jun 2022 19:40:08 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 27 Jun 2022 19:40:08 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 27 Jun 2022 19:40:09 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 27 Jun 2022 19:40:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 27 Jun 2022 19:40:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 27 Jun 2022 19:40:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 27 Jun 2022 19:40:15 GMT
USER rootless
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461a7af5a02121a302d2e50704a0a555a028e64fe24cbfb84884f4122adbce70`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 6.7 MB (6734648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d0bb0a216f03245f2d6d1507fbe50b176695a523650d18aa9435dd1ad5b056`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e581a5e0448861bef772f9b7593e8e9c334ff3700e24a603534a348b485995`  
		Last Modified: Mon, 27 Jun 2022 19:42:47 GMT  
		Size: 964.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ef26b393cbf609a417ec318bf7a20248b3b652ae0dd801b31240a9767d5eb2`  
		Last Modified: Mon, 27 Jun 2022 19:42:46 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb81cd00d951430d0d6a10659f3cc595a956259be8873d793585d2338219ba6a`  
		Last Modified: Mon, 27 Jun 2022 19:43:08 GMT  
		Size: 1.4 MB (1370340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe035b69142cb3e2217653d63a0847885a13030bf1a65e774a379ca934d7268`  
		Last Modified: Mon, 27 Jun 2022 19:43:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354159b9f8e77204c8a136be72ff2630314987acbfb05bad82def89c68ead49f`  
		Last Modified: Mon, 27 Jun 2022 19:43:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5901fdfbac1923f4024314e677b4f31e53a8e7a19f3eafdcae185428f768aef5`  
		Last Modified: Mon, 27 Jun 2022 19:43:11 GMT  
		Size: 21.9 MB (21887381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7901c23f8491a677237a7698774bf57b4e95c6b9de321952a74a186de30c7948`  
		Last Modified: Mon, 27 Jun 2022 19:43:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-git`

```console
$ docker pull docker@sha256:b36802aae7c9718573516031bc675ad017c1b0fd79521900e62384bd12d87861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-git` - linux; amd64

```console
$ docker pull docker@sha256:413c8a5dc862d1d85ae1474b18ab671a236fbc05eba8b168a489423de080f96d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97621472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ca41888a2c5d5d63f0780a05897b6ba402930ac943d0b61f82510615022e0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Mon, 18 Jul 2022 22:15:42 GMT
RUN apk add --no-cache git
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
	-	`sha256:b6364ecd6bc81eb855021d5d56c8cf4f669eaee31c754affc91a381e965ae9c7`  
		Last Modified: Mon, 18 Jul 2022 22:18:03 GMT  
		Size: 6.9 MB (6943678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:69c954b769b9014dc73efd4cf3cf7c7a54518271dfd0c7556caa01a6430c29f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90450634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f0fab2c694c55846599e01b9f69c04153ecd1994066217e458eefc35ab925f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Fri, 27 May 2022 00:42:03 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 27 May 2022 00:42:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 06 Jun 2022 18:36:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Mon, 06 Jun 2022 18:36:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 06 Jun 2022 18:36:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 06 Jun 2022 18:36:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Mon, 27 Jun 2022 19:39:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Mon, 27 Jun 2022 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 27 Jun 2022 19:39:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 27 Jun 2022 19:39:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 27 Jun 2022 19:39:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 27 Jun 2022 19:39:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 27 Jun 2022 19:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 19:39:43 GMT
CMD ["sh"]
# Mon, 27 Jun 2022 19:40:22 GMT
RUN apk add --no-cache git
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
	-	`sha256:c5f1c4eb6753c4d8ca8abdc68946eaf136ebf43c3ba68b1e3f168d561a7a40e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:21 GMT  
		Size: 57.0 MB (57027293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8543d611571340a3ade0985e604f8050b3bd7c750ce108d248072285be716e4`  
		Last Modified: Mon, 06 Jun 2022 18:39:13 GMT  
		Size: 13.1 MB (13097906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d288aeb78f45219c1727b6023bd09e3aca0bc0ac2906254cdebbaa3371aac5`  
		Last Modified: Mon, 27 Jun 2022 19:42:24 GMT  
		Size: 8.6 MB (8578047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88149d4f722465678b6f0a627e24d5a1026b68da2830834e74f2a5366486d56a`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c923600f007a725875a878e4700a91ddda7a4b1eefcbb9bb83d48b0328ff3c`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86fa76151ef36a9479f1284449f3a7b37b7cf8811af6e9c082c8cae25d556f`  
		Last Modified: Mon, 27 Jun 2022 19:42:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a306f45f18ccb9a32f7f2b7fbe663bca6648af057abb4defe68aad16b886e9`  
		Last Modified: Mon, 27 Jun 2022 19:43:28 GMT  
		Size: 7.1 MB (7054455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:a715787594b32b9cdb188adb4bd34f591f6d1157320936b5f029237cb698bb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `docker:rc-windowsservercore` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:21894d75dc7ad7b1128482f6ee9f6d940927c986213c3957180da2d19f23185b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310655058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397dfb1ed2fda6c7862c1fd0893a8349cac1129c0040c28013b1a0dab7e2608e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:09:15 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:09:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:09:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b7d5cf167dc176e16f7f47520ad35fb27c5d9b4adbcca6204a3d8fe6e6b5ee`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9504b70312192db63cb4837d1adcd0aec44b658f596d069f409787f9c055c0`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e945f6d7d36e52540a1c818463f967d23624fe79480e55f162e0f4262c9a3feb`  
		Last Modified: Wed, 13 Jul 2022 17:14:08 GMT  
		Size: 9.8 MB (9765370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:11e833c8880b2318e4f0f2c161c7ecf04ec129277ae8d9040971b04185b53b04
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2681925749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4e2c4281dbb643e4ea2b0ae3993b6652eb026718c537c2223dc3d607bb1de7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:10:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:10:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:11:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca49c3d0f1b10ab622d1ad62fdff5b201db2b1b5d796919f0d74b70a933b6a2`  
		Last Modified: Wed, 13 Jul 2022 17:14:21 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadd2a4879da5a12799c4722e6d956052140ab1b2c9246ade10879c43a875d98`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd78d697ed3fbe490f2c2eab2f6d2591b4205efc5b6c041f7b6853dcebd8d154`  
		Last Modified: Wed, 13 Jul 2022 17:14:24 GMT  
		Size: 9.5 MB (9526144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:35d815c0f33797de72b554f4b54011993fc220a443932c9d7a57ec5b5e1ff5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `docker:rc-windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:11e833c8880b2318e4f0f2c161c7ecf04ec129277ae8d9040971b04185b53b04
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2681925749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4e2c4281dbb643e4ea2b0ae3993b6652eb026718c537c2223dc3d607bb1de7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:10:44 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:10:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:11:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca49c3d0f1b10ab622d1ad62fdff5b201db2b1b5d796919f0d74b70a933b6a2`  
		Last Modified: Wed, 13 Jul 2022 17:14:21 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadd2a4879da5a12799c4722e6d956052140ab1b2c9246ade10879c43a875d98`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd78d697ed3fbe490f2c2eab2f6d2591b4205efc5b6c041f7b6853dcebd8d154`  
		Last Modified: Wed, 13 Jul 2022 17:14:24 GMT  
		Size: 9.5 MB (9526144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:e12c921c0f72f0dcfac2205e0ad1d7f7bc4c3258faf7040f02467314fb48c3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:21894d75dc7ad7b1128482f6ee9f6d940927c986213c3957180da2d19f23185b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310655058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397dfb1ed2fda6c7862c1fd0893a8349cac1129c0040c28013b1a0dab7e2608e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:09:15 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Wed, 13 Jul 2022 17:09:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-22.06.0-beta.0.zip
# Wed, 13 Jul 2022 17:09:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b7d5cf167dc176e16f7f47520ad35fb27c5d9b4adbcca6204a3d8fe6e6b5ee`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9504b70312192db63cb4837d1adcd0aec44b658f596d069f409787f9c055c0`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e945f6d7d36e52540a1c818463f967d23624fe79480e55f162e0f4262c9a3feb`  
		Last Modified: Wed, 13 Jul 2022 17:14:08 GMT  
		Size: 9.8 MB (9765370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:aa0b01f106685b0d0494aff223fcca039e507bf16c4859593b26714599074fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `docker:windowsservercore` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:7262b1947cffb1bf370d142eba1fc216dd59510b2f6af0bd9b43d4da8f5042db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353410338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96da4d70661fa4eac578cd29bb6e6f9ab0753d3b20202e726a3794d037979f56`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:11:48 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:11:49 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:12:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1da040c1cae02b726504c01ddb04ab6bc757384118e4997d2dc4b7e71fa76`  
		Last Modified: Wed, 13 Jul 2022 17:14:37 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd127957c40c6e903e73c2d36fd99a3937d8d4247d3068b446ae89771561f56`  
		Last Modified: Wed, 13 Jul 2022 17:14:38 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848a713cc66b0bd9b05ab1649d40f3a864c3557b09ee84feaf88a50bf9e71962`  
		Last Modified: Wed, 13 Jul 2022 17:14:48 GMT  
		Size: 52.5 MB (52520655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:d286ed6b7161125360b30763cddc35da6be81a4a8d40a46269788a647ab0b4a6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2724680561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00e049b0813b313a68cbcc666e527d2ee40c170b3c61f83c75952483ee5fbb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:13:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86af5967d42c804ec0ac2f177b83169359deede4dafa6dbfb40bc97aad7181`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d48e2e1c03a59c2bc5fa97787d608c1c56d2c5dea767bcb8266ece9c31be0`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f086bc01bdb19544655edff05b0730da6228f93c165306b8a1c2afbac5b4396`  
		Last Modified: Wed, 13 Jul 2022 17:15:11 GMT  
		Size: 52.3 MB (52281174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:c4c60a9bf7998d5b05c8c6d30644c7301e26edcba1ba9a13afbb4e8d372b9043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull docker@sha256:d286ed6b7161125360b30763cddc35da6be81a4a8d40a46269788a647ab0b4a6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2724680561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00e049b0813b313a68cbcc666e527d2ee40c170b3c61f83c75952483ee5fbb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:10:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:12:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:13:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d6c0a51981d7e8209dadd5b937bfeaf0f26a2c75f59ffe3fd0b942900682fd`  
		Last Modified: Wed, 13 Jul 2022 17:14:22 GMT  
		Size: 351.6 KB (351622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86af5967d42c804ec0ac2f177b83169359deede4dafa6dbfb40bc97aad7181`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d48e2e1c03a59c2bc5fa97787d608c1c56d2c5dea767bcb8266ece9c31be0`  
		Last Modified: Wed, 13 Jul 2022 17:15:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f086bc01bdb19544655edff05b0730da6228f93c165306b8a1c2afbac5b4396`  
		Last Modified: Wed, 13 Jul 2022 17:15:11 GMT  
		Size: 52.3 MB (52281174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:b6f7a5dae2f95505f6fee244d4588441986227aeb49eda1e7bf8019a46da3957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull docker@sha256:7262b1947cffb1bf370d142eba1fc216dd59510b2f6af0bd9b43d4da8f5042db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353410338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96da4d70661fa4eac578cd29bb6e6f9ab0753d3b20202e726a3794d037979f56`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jul 2022 17:09:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Jul 2022 17:11:48 GMT
ENV DOCKER_VERSION=20.10.17
# Wed, 13 Jul 2022 17:11:49 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.17.zip
# Wed, 13 Jul 2022 17:12:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d06cdb2d60782d53dd4cb0435f856546342e4dbd687a391a5427dad11c460`  
		Last Modified: Wed, 13 Jul 2022 17:14:06 GMT  
		Size: 653.8 KB (653846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f1da040c1cae02b726504c01ddb04ab6bc757384118e4997d2dc4b7e71fa76`  
		Last Modified: Wed, 13 Jul 2022 17:14:37 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd127957c40c6e903e73c2d36fd99a3937d8d4247d3068b446ae89771561f56`  
		Last Modified: Wed, 13 Jul 2022 17:14:38 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848a713cc66b0bd9b05ab1649d40f3a864c3557b09ee84feaf88a50bf9e71962`  
		Last Modified: Wed, 13 Jul 2022 17:14:48 GMT  
		Size: 52.5 MB (52520655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

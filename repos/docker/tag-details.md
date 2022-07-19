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
$ docker pull docker@sha256:aa9895439568ab56e3a8eb14a86edfd789c9647b9e87685ea847492271bd61f7
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
$ docker pull docker@sha256:59e034b9d3c7bc2850617faedf73aeed36d7b251256cfc1f23c78700bd67e95f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86391341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae97a023e5398afd9b9bae8040488ae1b1afd2a55f625318226445e249456b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 04:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 19 Jul 2022 04:35:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:1dae0a94309e28ad8cf584ebfa7896589c62556c035f11a5e5a9e564b80fdb1a
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
$ docker pull docker@sha256:e474daa33acae73af5ff785fda5b92e66d778485a6294e77c6c2ac77f5f3e8e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93132013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0bd48db27d0f48d664dd9560bffd3f6ab065d50780203141a6cfb281583765`
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
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:36:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 19 Jul 2022 04:36:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:36:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 19 Jul 2022 04:36:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 19 Jul 2022 04:36:59 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:59 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Jul 2022 04:37:00 GMT
EXPOSE 2375 2376
# Tue, 19 Jul 2022 04:37:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Jul 2022 04:37:02 GMT
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0d869708b25b18f4819147a4f2da34e545988e77a25bb0ed9c9c7dbe55b12f`  
		Last Modified: Tue, 19 Jul 2022 04:40:31 GMT  
		Size: 6.7 MB (6735676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f975a51d5bcb2dda826eb84af4f65e93aa2116a3a356fe10f561eb21a328b4e2`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb67eb99df65109c466265b2f454f7ab0f4454c25be43ab4c16e38301bac0e6`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f5b37e909d4ba4073fecd9bc4aefac284c49e2df06d34655636949c23baa61`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:fe932c9d071de9983109d2635ce809c9ba006ec5862209d126d7801462472965
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
$ docker pull docker@sha256:05bac4dd11e659e25834a17bc22c3f29d01b7e166d41f69bce0643226cf76e5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115681041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0e515596ea2dce6f84dc7b536d18d08058167df3c7ab2322c0714d291b084f`
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
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:36:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 19 Jul 2022 04:36:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:36:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 19 Jul 2022 04:36:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 19 Jul 2022 04:36:59 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:59 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Jul 2022 04:37:00 GMT
EXPOSE 2375 2376
# Tue, 19 Jul 2022 04:37:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Jul 2022 04:37:02 GMT
CMD []
# Tue, 19 Jul 2022 04:37:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Tue, 19 Jul 2022 04:37:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 19 Jul 2022 04:37:12 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:37:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 19 Jul 2022 04:37:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 19 Jul 2022 04:37:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Jul 2022 04:37:17 GMT
USER rootless
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0d869708b25b18f4819147a4f2da34e545988e77a25bb0ed9c9c7dbe55b12f`  
		Last Modified: Tue, 19 Jul 2022 04:40:31 GMT  
		Size: 6.7 MB (6735676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f975a51d5bcb2dda826eb84af4f65e93aa2116a3a356fe10f561eb21a328b4e2`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb67eb99df65109c466265b2f454f7ab0f4454c25be43ab4c16e38301bac0e6`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f5b37e909d4ba4073fecd9bc4aefac284c49e2df06d34655636949c23baa61`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bac721d1ba2525770bb7c64009db291b907d5c82341a278905ad3bf3796084`  
		Last Modified: Tue, 19 Jul 2022 04:40:54 GMT  
		Size: 1.4 MB (1370354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3d7322044f0607149416c10326ef233142914c5765d2a7491dfa20a82c4aad`  
		Last Modified: Tue, 19 Jul 2022 04:40:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7ff72f7fee2cad6314b0d9fb2ef65886794cb85f94f57f05da640c85cee121`  
		Last Modified: Tue, 19 Jul 2022 04:40:53 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454d4afef13e3b687710c36a520cca9cdb6278f3080c62fbd780f0ae049c9ea`  
		Last Modified: Tue, 19 Jul 2022 04:40:57 GMT  
		Size: 21.2 MB (21177051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d2ed6cd2442f2a9d80df1ac2ed484da3fe238b709d2f145a20b48b3e45ffda`  
		Last Modified: Tue, 19 Jul 2022 04:40:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:3d722fd65b343eecdf68a724befec765e5c03d9622e20d40609ee353ddf6a432
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
$ docker pull docker@sha256:08995ad0585295e6f71cbf90e3020fbd5e565f7a9a48f376a368d60add1620db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93448308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370528b6d0358e26a5d28d0a69a8207ee55bf7599eb670871aa9e39ace5f2627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 04:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 19 Jul 2022 04:35:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:37:25 GMT
RUN apk add --no-cache git
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60451317c0939207b1e316dfc1043955d069c5f858e0288b66c07177981ae57e`  
		Last Modified: Tue, 19 Jul 2022 04:41:19 GMT  
		Size: 7.1 MB (7056967 bytes)  
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
$ docker pull docker@sha256:aa9895439568ab56e3a8eb14a86edfd789c9647b9e87685ea847492271bd61f7
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
$ docker pull docker@sha256:59e034b9d3c7bc2850617faedf73aeed36d7b251256cfc1f23c78700bd67e95f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86391341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae97a023e5398afd9b9bae8040488ae1b1afd2a55f625318226445e249456b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 04:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 19 Jul 2022 04:35:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:1dae0a94309e28ad8cf584ebfa7896589c62556c035f11a5e5a9e564b80fdb1a
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
$ docker pull docker@sha256:e474daa33acae73af5ff785fda5b92e66d778485a6294e77c6c2ac77f5f3e8e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93132013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0bd48db27d0f48d664dd9560bffd3f6ab065d50780203141a6cfb281583765`
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
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:36:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 19 Jul 2022 04:36:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:36:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 19 Jul 2022 04:36:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 19 Jul 2022 04:36:59 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:59 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Jul 2022 04:37:00 GMT
EXPOSE 2375 2376
# Tue, 19 Jul 2022 04:37:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Jul 2022 04:37:02 GMT
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0d869708b25b18f4819147a4f2da34e545988e77a25bb0ed9c9c7dbe55b12f`  
		Last Modified: Tue, 19 Jul 2022 04:40:31 GMT  
		Size: 6.7 MB (6735676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f975a51d5bcb2dda826eb84af4f65e93aa2116a3a356fe10f561eb21a328b4e2`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb67eb99df65109c466265b2f454f7ab0f4454c25be43ab4c16e38301bac0e6`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f5b37e909d4ba4073fecd9bc4aefac284c49e2df06d34655636949c23baa61`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:fe932c9d071de9983109d2635ce809c9ba006ec5862209d126d7801462472965
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
$ docker pull docker@sha256:05bac4dd11e659e25834a17bc22c3f29d01b7e166d41f69bce0643226cf76e5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115681041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0e515596ea2dce6f84dc7b536d18d08058167df3c7ab2322c0714d291b084f`
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
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:36:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 19 Jul 2022 04:36:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:36:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 19 Jul 2022 04:36:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 19 Jul 2022 04:36:59 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:59 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Jul 2022 04:37:00 GMT
EXPOSE 2375 2376
# Tue, 19 Jul 2022 04:37:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Jul 2022 04:37:02 GMT
CMD []
# Tue, 19 Jul 2022 04:37:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Tue, 19 Jul 2022 04:37:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 19 Jul 2022 04:37:12 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:37:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 19 Jul 2022 04:37:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 19 Jul 2022 04:37:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Jul 2022 04:37:17 GMT
USER rootless
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0d869708b25b18f4819147a4f2da34e545988e77a25bb0ed9c9c7dbe55b12f`  
		Last Modified: Tue, 19 Jul 2022 04:40:31 GMT  
		Size: 6.7 MB (6735676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f975a51d5bcb2dda826eb84af4f65e93aa2116a3a356fe10f561eb21a328b4e2`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb67eb99df65109c466265b2f454f7ab0f4454c25be43ab4c16e38301bac0e6`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f5b37e909d4ba4073fecd9bc4aefac284c49e2df06d34655636949c23baa61`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bac721d1ba2525770bb7c64009db291b907d5c82341a278905ad3bf3796084`  
		Last Modified: Tue, 19 Jul 2022 04:40:54 GMT  
		Size: 1.4 MB (1370354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3d7322044f0607149416c10326ef233142914c5765d2a7491dfa20a82c4aad`  
		Last Modified: Tue, 19 Jul 2022 04:40:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7ff72f7fee2cad6314b0d9fb2ef65886794cb85f94f57f05da640c85cee121`  
		Last Modified: Tue, 19 Jul 2022 04:40:53 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454d4afef13e3b687710c36a520cca9cdb6278f3080c62fbd780f0ae049c9ea`  
		Last Modified: Tue, 19 Jul 2022 04:40:57 GMT  
		Size: 21.2 MB (21177051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d2ed6cd2442f2a9d80df1ac2ed484da3fe238b709d2f145a20b48b3e45ffda`  
		Last Modified: Tue, 19 Jul 2022 04:40:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:3d722fd65b343eecdf68a724befec765e5c03d9622e20d40609ee353ddf6a432
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
$ docker pull docker@sha256:08995ad0585295e6f71cbf90e3020fbd5e565f7a9a48f376a368d60add1620db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93448308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370528b6d0358e26a5d28d0a69a8207ee55bf7599eb670871aa9e39ace5f2627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 04:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 19 Jul 2022 04:35:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:37:25 GMT
RUN apk add --no-cache git
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60451317c0939207b1e316dfc1043955d069c5f858e0288b66c07177981ae57e`  
		Last Modified: Tue, 19 Jul 2022 04:41:19 GMT  
		Size: 7.1 MB (7056967 bytes)  
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
$ docker pull docker@sha256:aa9895439568ab56e3a8eb14a86edfd789c9647b9e87685ea847492271bd61f7
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
$ docker pull docker@sha256:59e034b9d3c7bc2850617faedf73aeed36d7b251256cfc1f23c78700bd67e95f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86391341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae97a023e5398afd9b9bae8040488ae1b1afd2a55f625318226445e249456b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 04:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 19 Jul 2022 04:35:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-alpine3.16`

```console
$ docker pull docker@sha256:aa9895439568ab56e3a8eb14a86edfd789c9647b9e87685ea847492271bd61f7
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
$ docker pull docker@sha256:59e034b9d3c7bc2850617faedf73aeed36d7b251256cfc1f23c78700bd67e95f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86391341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae97a023e5398afd9b9bae8040488ae1b1afd2a55f625318226445e249456b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 04:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 19 Jul 2022 04:35:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-dind`

```console
$ docker pull docker@sha256:1dae0a94309e28ad8cf584ebfa7896589c62556c035f11a5e5a9e564b80fdb1a
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
$ docker pull docker@sha256:e474daa33acae73af5ff785fda5b92e66d778485a6294e77c6c2ac77f5f3e8e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93132013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0bd48db27d0f48d664dd9560bffd3f6ab065d50780203141a6cfb281583765`
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
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:36:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 19 Jul 2022 04:36:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:36:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 19 Jul 2022 04:36:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 19 Jul 2022 04:36:59 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:59 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Jul 2022 04:37:00 GMT
EXPOSE 2375 2376
# Tue, 19 Jul 2022 04:37:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Jul 2022 04:37:02 GMT
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0d869708b25b18f4819147a4f2da34e545988e77a25bb0ed9c9c7dbe55b12f`  
		Last Modified: Tue, 19 Jul 2022 04:40:31 GMT  
		Size: 6.7 MB (6735676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f975a51d5bcb2dda826eb84af4f65e93aa2116a3a356fe10f561eb21a328b4e2`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb67eb99df65109c466265b2f454f7ab0f4454c25be43ab4c16e38301bac0e6`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f5b37e909d4ba4073fecd9bc4aefac284c49e2df06d34655636949c23baa61`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-dind-alpine3.16`

```console
$ docker pull docker@sha256:1dae0a94309e28ad8cf584ebfa7896589c62556c035f11a5e5a9e564b80fdb1a
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
$ docker pull docker@sha256:e474daa33acae73af5ff785fda5b92e66d778485a6294e77c6c2ac77f5f3e8e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93132013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0bd48db27d0f48d664dd9560bffd3f6ab065d50780203141a6cfb281583765`
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
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:36:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 19 Jul 2022 04:36:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:36:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 19 Jul 2022 04:36:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 19 Jul 2022 04:36:59 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:59 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Jul 2022 04:37:00 GMT
EXPOSE 2375 2376
# Tue, 19 Jul 2022 04:37:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Jul 2022 04:37:02 GMT
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0d869708b25b18f4819147a4f2da34e545988e77a25bb0ed9c9c7dbe55b12f`  
		Last Modified: Tue, 19 Jul 2022 04:40:31 GMT  
		Size: 6.7 MB (6735676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f975a51d5bcb2dda826eb84af4f65e93aa2116a3a356fe10f561eb21a328b4e2`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb67eb99df65109c466265b2f454f7ab0f4454c25be43ab4c16e38301bac0e6`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f5b37e909d4ba4073fecd9bc4aefac284c49e2df06d34655636949c23baa61`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-dind-rootless`

```console
$ docker pull docker@sha256:fe932c9d071de9983109d2635ce809c9ba006ec5862209d126d7801462472965
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
$ docker pull docker@sha256:05bac4dd11e659e25834a17bc22c3f29d01b7e166d41f69bce0643226cf76e5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115681041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0e515596ea2dce6f84dc7b536d18d08058167df3c7ab2322c0714d291b084f`
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
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:36:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 19 Jul 2022 04:36:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:36:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 19 Jul 2022 04:36:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 19 Jul 2022 04:36:59 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:59 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Jul 2022 04:37:00 GMT
EXPOSE 2375 2376
# Tue, 19 Jul 2022 04:37:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Jul 2022 04:37:02 GMT
CMD []
# Tue, 19 Jul 2022 04:37:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Tue, 19 Jul 2022 04:37:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 19 Jul 2022 04:37:12 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:37:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 19 Jul 2022 04:37:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 19 Jul 2022 04:37:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Jul 2022 04:37:17 GMT
USER rootless
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0d869708b25b18f4819147a4f2da34e545988e77a25bb0ed9c9c7dbe55b12f`  
		Last Modified: Tue, 19 Jul 2022 04:40:31 GMT  
		Size: 6.7 MB (6735676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f975a51d5bcb2dda826eb84af4f65e93aa2116a3a356fe10f561eb21a328b4e2`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb67eb99df65109c466265b2f454f7ab0f4454c25be43ab4c16e38301bac0e6`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f5b37e909d4ba4073fecd9bc4aefac284c49e2df06d34655636949c23baa61`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bac721d1ba2525770bb7c64009db291b907d5c82341a278905ad3bf3796084`  
		Last Modified: Tue, 19 Jul 2022 04:40:54 GMT  
		Size: 1.4 MB (1370354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3d7322044f0607149416c10326ef233142914c5765d2a7491dfa20a82c4aad`  
		Last Modified: Tue, 19 Jul 2022 04:40:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7ff72f7fee2cad6314b0d9fb2ef65886794cb85f94f57f05da640c85cee121`  
		Last Modified: Tue, 19 Jul 2022 04:40:53 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454d4afef13e3b687710c36a520cca9cdb6278f3080c62fbd780f0ae049c9ea`  
		Last Modified: Tue, 19 Jul 2022 04:40:57 GMT  
		Size: 21.2 MB (21177051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d2ed6cd2442f2a9d80df1ac2ed484da3fe238b709d2f145a20b48b3e45ffda`  
		Last Modified: Tue, 19 Jul 2022 04:40:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.17-git`

```console
$ docker pull docker@sha256:3d722fd65b343eecdf68a724befec765e5c03d9622e20d40609ee353ddf6a432
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
$ docker pull docker@sha256:08995ad0585295e6f71cbf90e3020fbd5e565f7a9a48f376a368d60add1620db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93448308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370528b6d0358e26a5d28d0a69a8207ee55bf7599eb670871aa9e39ace5f2627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 04:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 19 Jul 2022 04:35:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:37:25 GMT
RUN apk add --no-cache git
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60451317c0939207b1e316dfc1043955d069c5f858e0288b66c07177981ae57e`  
		Last Modified: Tue, 19 Jul 2022 04:41:19 GMT  
		Size: 7.1 MB (7056967 bytes)  
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
$ docker pull docker@sha256:748c7e2545dab2b3ef7e97b92945e7717cb9fd6f068582a3fde4d7404cba0707
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
$ docker pull docker@sha256:7ab2f6c51b0464149dbe68f45c149acd9d92442db835146905e28cb8e4bb62cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83396463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbe4723dc71d8b1db156a8ac03cd02cfc847369867fb34bc02b5734b8e5fc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

## `docker:22.06-rc-dind`

```console
$ docker pull docker@sha256:8c325fc710d116a88f8d196001d2c7cc28a92653cf34162b920c32680309a7a1
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

## `docker:22.06-rc-dind-rootless`

```console
$ docker pull docker@sha256:a446d76b0b8e9bc39226f1b2f534166298e7bc7ea09eacc2c645859bf9b5edfa
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
$ docker pull docker@sha256:238487ee5923271c06cfbfa825d58c3bc98fe07025a6626eebd0f96b9cf515e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113396519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8e022a99b417529c8eeb2fc3899b4bc66c54266f259c12094c9349c142a475`
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
# Tue, 19 Jul 2022 04:36:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Tue, 19 Jul 2022 04:36:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 19 Jul 2022 04:36:12 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:36:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 19 Jul 2022 04:36:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 19 Jul 2022 04:36:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Jul 2022 04:36:18 GMT
USER rootless
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
	-	`sha256:5d191f55714d1355858a32844a4388c6094376ca7d5a7c7c4709a968d2901af8`  
		Last Modified: Tue, 19 Jul 2022 04:39:22 GMT  
		Size: 1.4 MB (1370344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8506cbb20a71a6b88c0fbcc5aa7fc68762c88ecb322512bde7b89817339130b9`  
		Last Modified: Tue, 19 Jul 2022 04:39:21 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3add8827cf2c18e95d120f3b711fcea0b72d432d18815cf0302cff63cd0398`  
		Last Modified: Tue, 19 Jul 2022 04:39:21 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2aba27cd4211a6e638c20bfd7e8b2a197d77d96a41f48372a33c18825d9e9`  
		Last Modified: Tue, 19 Jul 2022 04:39:25 GMT  
		Size: 21.9 MB (21887400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215d513eb51723999a175f00af7440b7ee7104d5103beee76e67556bc0649d85`  
		Last Modified: Tue, 19 Jul 2022 04:39:21 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06-rc-git`

```console
$ docker pull docker@sha256:aed629af5241c54c035d815e21682135b4b3a1d9e2bcb552396eeccc0b71dbd6
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
$ docker pull docker@sha256:3094bfd103fc50c6419c0cfc529c05d8928b24660ab0fe63cef876438674d150
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90453416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e418ab83c88ba5c08861b23d872c4387a0ce79e984e31904c0797c8a8123b82d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Tue, 19 Jul 2022 04:36:25 GMT
RUN apk add --no-cache git
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
	-	`sha256:85bfd80c177ebe04185cd340cb97a980776455d315cfe89fc0b625c22fc7a27b`  
		Last Modified: Tue, 19 Jul 2022 04:39:42 GMT  
		Size: 7.1 MB (7056953 bytes)  
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
$ docker pull docker@sha256:748c7e2545dab2b3ef7e97b92945e7717cb9fd6f068582a3fde4d7404cba0707
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
$ docker pull docker@sha256:7ab2f6c51b0464149dbe68f45c149acd9d92442db835146905e28cb8e4bb62cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83396463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbe4723dc71d8b1db156a8ac03cd02cfc847369867fb34bc02b5734b8e5fc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

## `docker:22.06.0-beta.0-alpine3.16`

```console
$ docker pull docker@sha256:748c7e2545dab2b3ef7e97b92945e7717cb9fd6f068582a3fde4d7404cba0707
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
$ docker pull docker@sha256:7ab2f6c51b0464149dbe68f45c149acd9d92442db835146905e28cb8e4bb62cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83396463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbe4723dc71d8b1db156a8ac03cd02cfc847369867fb34bc02b5734b8e5fc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

## `docker:22.06.0-beta.0-dind`

```console
$ docker pull docker@sha256:8c325fc710d116a88f8d196001d2c7cc28a92653cf34162b920c32680309a7a1
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

## `docker:22.06.0-beta.0-dind-alpine3.16`

```console
$ docker pull docker@sha256:8c325fc710d116a88f8d196001d2c7cc28a92653cf34162b920c32680309a7a1
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

## `docker:22.06.0-beta.0-dind-rootless`

```console
$ docker pull docker@sha256:a446d76b0b8e9bc39226f1b2f534166298e7bc7ea09eacc2c645859bf9b5edfa
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
$ docker pull docker@sha256:238487ee5923271c06cfbfa825d58c3bc98fe07025a6626eebd0f96b9cf515e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113396519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8e022a99b417529c8eeb2fc3899b4bc66c54266f259c12094c9349c142a475`
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
# Tue, 19 Jul 2022 04:36:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Tue, 19 Jul 2022 04:36:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 19 Jul 2022 04:36:12 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:36:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 19 Jul 2022 04:36:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 19 Jul 2022 04:36:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Jul 2022 04:36:18 GMT
USER rootless
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
	-	`sha256:5d191f55714d1355858a32844a4388c6094376ca7d5a7c7c4709a968d2901af8`  
		Last Modified: Tue, 19 Jul 2022 04:39:22 GMT  
		Size: 1.4 MB (1370344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8506cbb20a71a6b88c0fbcc5aa7fc68762c88ecb322512bde7b89817339130b9`  
		Last Modified: Tue, 19 Jul 2022 04:39:21 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3add8827cf2c18e95d120f3b711fcea0b72d432d18815cf0302cff63cd0398`  
		Last Modified: Tue, 19 Jul 2022 04:39:21 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2aba27cd4211a6e638c20bfd7e8b2a197d77d96a41f48372a33c18825d9e9`  
		Last Modified: Tue, 19 Jul 2022 04:39:25 GMT  
		Size: 21.9 MB (21887400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215d513eb51723999a175f00af7440b7ee7104d5103beee76e67556bc0649d85`  
		Last Modified: Tue, 19 Jul 2022 04:39:21 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:22.06.0-beta.0-git`

```console
$ docker pull docker@sha256:aed629af5241c54c035d815e21682135b4b3a1d9e2bcb552396eeccc0b71dbd6
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
$ docker pull docker@sha256:3094bfd103fc50c6419c0cfc529c05d8928b24660ab0fe63cef876438674d150
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90453416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e418ab83c88ba5c08861b23d872c4387a0ce79e984e31904c0797c8a8123b82d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Tue, 19 Jul 2022 04:36:25 GMT
RUN apk add --no-cache git
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
	-	`sha256:85bfd80c177ebe04185cd340cb97a980776455d315cfe89fc0b625c22fc7a27b`  
		Last Modified: Tue, 19 Jul 2022 04:39:42 GMT  
		Size: 7.1 MB (7056953 bytes)  
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
$ docker pull docker@sha256:1dae0a94309e28ad8cf584ebfa7896589c62556c035f11a5e5a9e564b80fdb1a
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
$ docker pull docker@sha256:e474daa33acae73af5ff785fda5b92e66d778485a6294e77c6c2ac77f5f3e8e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93132013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0bd48db27d0f48d664dd9560bffd3f6ab065d50780203141a6cfb281583765`
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
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:36:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 19 Jul 2022 04:36:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:36:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 19 Jul 2022 04:36:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 19 Jul 2022 04:36:59 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:59 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Jul 2022 04:37:00 GMT
EXPOSE 2375 2376
# Tue, 19 Jul 2022 04:37:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Jul 2022 04:37:02 GMT
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0d869708b25b18f4819147a4f2da34e545988e77a25bb0ed9c9c7dbe55b12f`  
		Last Modified: Tue, 19 Jul 2022 04:40:31 GMT  
		Size: 6.7 MB (6735676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f975a51d5bcb2dda826eb84af4f65e93aa2116a3a356fe10f561eb21a328b4e2`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb67eb99df65109c466265b2f454f7ab0f4454c25be43ab4c16e38301bac0e6`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f5b37e909d4ba4073fecd9bc4aefac284c49e2df06d34655636949c23baa61`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:fe932c9d071de9983109d2635ce809c9ba006ec5862209d126d7801462472965
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
$ docker pull docker@sha256:05bac4dd11e659e25834a17bc22c3f29d01b7e166d41f69bce0643226cf76e5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115681041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0e515596ea2dce6f84dc7b536d18d08058167df3c7ab2322c0714d291b084f`
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
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:36:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 19 Jul 2022 04:36:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:36:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 19 Jul 2022 04:36:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 19 Jul 2022 04:36:59 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:59 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Jul 2022 04:37:00 GMT
EXPOSE 2375 2376
# Tue, 19 Jul 2022 04:37:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Jul 2022 04:37:02 GMT
CMD []
# Tue, 19 Jul 2022 04:37:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Tue, 19 Jul 2022 04:37:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 19 Jul 2022 04:37:12 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:37:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 19 Jul 2022 04:37:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 19 Jul 2022 04:37:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Jul 2022 04:37:17 GMT
USER rootless
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0d869708b25b18f4819147a4f2da34e545988e77a25bb0ed9c9c7dbe55b12f`  
		Last Modified: Tue, 19 Jul 2022 04:40:31 GMT  
		Size: 6.7 MB (6735676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f975a51d5bcb2dda826eb84af4f65e93aa2116a3a356fe10f561eb21a328b4e2`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb67eb99df65109c466265b2f454f7ab0f4454c25be43ab4c16e38301bac0e6`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f5b37e909d4ba4073fecd9bc4aefac284c49e2df06d34655636949c23baa61`  
		Last Modified: Tue, 19 Jul 2022 04:40:30 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bac721d1ba2525770bb7c64009db291b907d5c82341a278905ad3bf3796084`  
		Last Modified: Tue, 19 Jul 2022 04:40:54 GMT  
		Size: 1.4 MB (1370354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3d7322044f0607149416c10326ef233142914c5765d2a7491dfa20a82c4aad`  
		Last Modified: Tue, 19 Jul 2022 04:40:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7ff72f7fee2cad6314b0d9fb2ef65886794cb85f94f57f05da640c85cee121`  
		Last Modified: Tue, 19 Jul 2022 04:40:53 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454d4afef13e3b687710c36a520cca9cdb6278f3080c62fbd780f0ae049c9ea`  
		Last Modified: Tue, 19 Jul 2022 04:40:57 GMT  
		Size: 21.2 MB (21177051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d2ed6cd2442f2a9d80df1ac2ed484da3fe238b709d2f145a20b48b3e45ffda`  
		Last Modified: Tue, 19 Jul 2022 04:40:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:3d722fd65b343eecdf68a724befec765e5c03d9622e20d40609ee353ddf6a432
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
$ docker pull docker@sha256:08995ad0585295e6f71cbf90e3020fbd5e565f7a9a48f376a368d60add1620db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93448308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370528b6d0358e26a5d28d0a69a8207ee55bf7599eb670871aa9e39ace5f2627`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 04:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 19 Jul 2022 04:35:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
# Tue, 19 Jul 2022 04:37:25 GMT
RUN apk add --no-cache git
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60451317c0939207b1e316dfc1043955d069c5f858e0288b66c07177981ae57e`  
		Last Modified: Tue, 19 Jul 2022 04:41:19 GMT  
		Size: 7.1 MB (7056967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:aa9895439568ab56e3a8eb14a86edfd789c9647b9e87685ea847492271bd61f7
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
$ docker pull docker@sha256:59e034b9d3c7bc2850617faedf73aeed36d7b251256cfc1f23c78700bd67e95f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86391341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae97a023e5398afd9b9bae8040488ae1b1afd2a55f625318226445e249456b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 04:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 19 Jul 2022 04:35:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Tue, 19 Jul 2022 04:36:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.6.1
# Tue, 19 Jul 2022 04:36:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-x86_64'; 			sha256='ed79398562f3a80a5d8c068fde14b0b12101e80b494aabb2b3533eaa10599e0f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv6'; 			sha256='2b5efc48e8359047cc280712f52e97be23fcb571b47b1e67ba6f56e971ac30f5'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-armv7'; 			sha256='727f67b78d6b1fbfed5de4d66869a691551f7341ad71504476d8a902e37588bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64'; 			sha256='2890aade218c145827521efb247b5765ac10ac5c46f21dddb2220c03c98d7f83'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-ppc64le'; 			sha256='93560efd323f39fe86244b80cbe1ffeb2c16b169c72a3ae25535def98c04e744'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-s390x'; 			sha256='2a56c35df12d7a7ce9a9ae83426df36a612b0035ee36053912594d6f5a6ff356'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Tue, 19 Jul 2022 04:36:42 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 19 Jul 2022 04:36:43 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:36:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Jul 2022 04:36:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 19 Jul 2022 04:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:36:46 GMT
CMD ["sh"]
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
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4411b67fe2a089ef4bb8faafd74f4f692a50354864e9dea99b2e44f086b05ec4`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 8.6 MB (8578076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06907aeeb1e99c6e37c8e13724e984cb8aef108c24c5f7549b7885facac7f61`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123964003229603650e1f2bbd108800210b4e883658471ca38e19a01e79dc30f`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae56ef9490b2b4ab00baac5db00f8b4e4a403e734d22960cb52ace49f024bf`  
		Last Modified: Tue, 19 Jul 2022 04:39:56 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc`

```console
$ docker pull docker@sha256:748c7e2545dab2b3ef7e97b92945e7717cb9fd6f068582a3fde4d7404cba0707
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
$ docker pull docker@sha256:7ab2f6c51b0464149dbe68f45c149acd9d92442db835146905e28cb8e4bb62cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83396463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbe4723dc71d8b1db156a8ac03cd02cfc847369867fb34bc02b5734b8e5fc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:a446d76b0b8e9bc39226f1b2f534166298e7bc7ea09eacc2c645859bf9b5edfa
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
$ docker pull docker@sha256:238487ee5923271c06cfbfa825d58c3bc98fe07025a6626eebd0f96b9cf515e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113396519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8e022a99b417529c8eeb2fc3899b4bc66c54266f259c12094c9349c142a475`
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
# Tue, 19 Jul 2022 04:36:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Tue, 19 Jul 2022 04:36:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 19 Jul 2022 04:36:12 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 19 Jul 2022 04:36:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 19 Jul 2022 04:36:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 19 Jul 2022 04:36:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Jul 2022 04:36:18 GMT
USER rootless
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
	-	`sha256:5d191f55714d1355858a32844a4388c6094376ca7d5a7c7c4709a968d2901af8`  
		Last Modified: Tue, 19 Jul 2022 04:39:22 GMT  
		Size: 1.4 MB (1370344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8506cbb20a71a6b88c0fbcc5aa7fc68762c88ecb322512bde7b89817339130b9`  
		Last Modified: Tue, 19 Jul 2022 04:39:21 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3add8827cf2c18e95d120f3b711fcea0b72d432d18815cf0302cff63cd0398`  
		Last Modified: Tue, 19 Jul 2022 04:39:21 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2aba27cd4211a6e638c20bfd7e8b2a197d77d96a41f48372a33c18825d9e9`  
		Last Modified: Tue, 19 Jul 2022 04:39:25 GMT  
		Size: 21.9 MB (21887400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215d513eb51723999a175f00af7440b7ee7104d5103beee76e67556bc0649d85`  
		Last Modified: Tue, 19 Jul 2022 04:39:21 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-git`

```console
$ docker pull docker@sha256:aed629af5241c54c035d815e21682135b4b3a1d9e2bcb552396eeccc0b71dbd6
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
$ docker pull docker@sha256:3094bfd103fc50c6419c0cfc529c05d8928b24660ab0fe63cef876438674d150
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90453416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e418ab83c88ba5c08861b23d872c4387a0ce79e984e31904c0797c8a8123b82d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Tue, 19 Jul 2022 04:36:25 GMT
RUN apk add --no-cache git
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
	-	`sha256:85bfd80c177ebe04185cd340cb97a980776455d315cfe89fc0b625c22fc7a27b`  
		Last Modified: Tue, 19 Jul 2022 04:39:42 GMT  
		Size: 7.1 MB (7056953 bytes)  
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

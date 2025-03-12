<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-1809`](#docker28-windowsservercore-1809)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.0`](#docker280)
-	[`docker:28.0-cli`](#docker280-cli)
-	[`docker:28.0-dind`](#docker280-dind)
-	[`docker:28.0-dind-rootless`](#docker280-dind-rootless)
-	[`docker:28.0-windowsservercore`](#docker280-windowsservercore)
-	[`docker:28.0-windowsservercore-1809`](#docker280-windowsservercore-1809)
-	[`docker:28.0-windowsservercore-ltsc2022`](#docker280-windowsservercore-ltsc2022)
-	[`docker:28.0-windowsservercore-ltsc2025`](#docker280-windowsservercore-ltsc2025)
-	[`docker:28.0.1`](#docker2801)
-	[`docker:28.0.1-alpine3.21`](#docker2801-alpine321)
-	[`docker:28.0.1-cli`](#docker2801-cli)
-	[`docker:28.0.1-cli-alpine3.21`](#docker2801-cli-alpine321)
-	[`docker:28.0.1-dind`](#docker2801-dind)
-	[`docker:28.0.1-dind-alpine3.21`](#docker2801-dind-alpine321)
-	[`docker:28.0.1-dind-rootless`](#docker2801-dind-rootless)
-	[`docker:28.0.1-windowsservercore`](#docker2801-windowsservercore)
-	[`docker:28.0.1-windowsservercore-1809`](#docker2801-windowsservercore-1809)
-	[`docker:28.0.1-windowsservercore-ltsc2022`](#docker2801-windowsservercore-ltsc2022)
-	[`docker:28.0.1-windowsservercore-ltsc2025`](#docker2801-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:9a651b22672c7151b5d8ca820ed2290b3fe4d4922e9b3f37ab14c8876da6613d
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
$ docker pull docker@sha256:63af38ad28e39198d32b84f6f0766b84f129223962a2b9d0d08895f82b8c974a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141018836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca75ab1d7a7464eafbb043969362b3580b89fc13d0a24015f05784cf1fbf4a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:9f4cacdb6d1c7d18007496fd3fdc3e1a7db761aa9120a04950e745674e852fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d352174790d7d189910e7f5c3030976778ee363ffe05d6c5f85ddf5208ef9bb`

```dockerfile
```

-	Layers:
	-	`sha256:8c7368c1f564a9560c431962f192d16acdb099321d336f23a570f3eadb276e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1781a83e4d8da5abccfbc908e5a59f38842fb75fa3c92a6439f39b5ea582734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131692655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f764f0067ba36f35452a088c243700ee0a13f44b0d8398f4f41320126a60100`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52b5b50da000f825732faa0b306b0b03aba942958f60b4e4a267f64f2609725`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 7.0 MB (7036882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220971bcf994b5c3a2e140bbf3bf38830ebb2d208da3e028d0b4632a69131af`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 89.9 KB (89870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31279910422b314845644d11076adf1d5a5bf46d1bb9f5f946994d70718ba0c2`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972dc8fbd8a452f36a21a28edc3dca31c4f0cb12877b3cf4c19444a24c319082`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7f9370d4ba1a6b159b96643477be5fcd0428ad716dca0cd4ad4548d815dd5`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcbea16a18e4ce2926adfe5a067d7c48dc5df60be0750162782f6ca9e2790e1`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:dae7e1a430d410690e1ac8f97bb7ba4a9970db59b5bad071334209e728508e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fef12049e311755a88f6ed54bc48d4c1b8bf6bb0d141affdec32b274fee2fcd`

```dockerfile
```

-	Layers:
	-	`sha256:e82d1cdacd927eb5664586024dae2a1cb667e1b8faed9e64bbfb6354fea7fc01`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:a06a9ae40437d600bc69403c9867d7c78bbd0261e1e8de585a9a1be038fc7e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130024916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef257cfb222c87f5b6aeb6bf1da8067196ecf6d7446a83c6120c78ccb0b4330`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a803a8a5b5db41392839b8d9e4b5dc98eb15e937e9a49ed46e2497676808283e`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 6.4 MB (6366128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53db656a9deda748d0137317b33e819676026a06a90003335d8129fd531e85`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 86.3 KB (86334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d755394c5b842899dd04ebc742660ce41ab0a2a14f38cf4d10e864b6dcffd5`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc2aa2417919467e58c0171cedbbd58423ec11584c3ed3285031ca790932146`  
		Last Modified: Tue, 04 Mar 2025 01:03:16 GMT  
		Size: 55.6 MB (55593637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eddd72049041d2e5083e7a7838eb4c6952dec7e4c186fe19c57d133194b086`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b244427612290e4f97cc15fb8e4f04d3b60140bf1ef1a77f18381bcdd2c51`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:e63515a65dee56b94046151fdf91185c60bc937a4dcaaf24d898bc9f3a057cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4367ec966899922086d3466b68fade429c2841e0551179512fb2308774c3345`

```dockerfile
```

-	Layers:
	-	`sha256:649fb81baea829805bdd59d93b87a3c335ef4fc45d773b95dcc4fa47fa616e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:13 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90ca9797ce316bce5ff74d335c304e85d41d6bd981f755a3281858072bfc839a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132411588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0250bf64dd26b5fe7a1a358ac561aa69a69de05ac454d6de509ef789813a11`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:f5b23b2ecb5219b4fd968f4f0e77e03bd1739c249efd6cd9743ff73138a96a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e084d1513f7ecd8f052a99a580b237130bd85603d5bacaacf72d2e9508170e20`

```dockerfile
```

-	Layers:
	-	`sha256:36cdd24344a437d2b167b4b38ada68f9f95a41ad871c683e3146b271a927edca`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:79bf825c5bed0d579820cc19f6857738abc424a680b619171591e969114f2015
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
$ docker pull docker@sha256:407b05f8635f0c78530a074e5ac3d7ca547e494f41d0b8279eb378c957d59eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73996743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7ace64e87a3531934d9d783dd55b09fba672037fb47361e760477742f81dbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e83e577007c54ec761b3cc9df69167cff393d56c84b9982c5aeaff3dc875c360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb394d129acd56043f7f5fb7f10a740ff52c5b301d50e34652f30fc3f4968535`

```dockerfile
```

-	Layers:
	-	`sha256:4e8c6e0b6ddceec47cfd0a4b2d23a912d8a9825b3412c2492d4162b91835a3ee`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:eeb4ad44bd101ca297d84a0a0c3d0a65e9c0b45a038e0311f029cf84ea075f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68966316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9dc49b493ad218febee37e481279ef5472fa3bb9a9c005a77ea867233c0fda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc9b040b7560289fbd5081459c6b6ddecaaf4363ef2436ae6c2b925e0382e3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d631428cc9605f46e62098c617996c4c90c97ed9efb14436c836857db508b29`

```dockerfile
```

-	Layers:
	-	`sha256:1fcd6fd391dd1a77f96dadcb8f3583ac995b301d90af68b3d9e3b9937c3213d9`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:da6f62e7a4822d683c95524b9c38b7e39d43633a4d518865fc88807116650172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67972911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1523a85a50b40de6aa255336254486bbf1dc534c39a0f2dcb7a5f69afffde5d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1c453d9c45321fd866c5830abe9036744fd50ea31aef24f0fd5b441f600d0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310b7edd1a05f5a6b1de9c12d0a3fd30be28798ce7d656f5b306158eb590c45c`

```dockerfile
```

-	Layers:
	-	`sha256:da87a8f3030a2c4d7a3e171d90c90259cecb58ab16f1f9570b999f97d340a6c6`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0e8384ace3dbca30fdface67dd29a8510a7285efdd842c51949e027ec0276891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69760973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a211b50f388cffbcec654f2c7e6951b74377f9657875d06fad2bc3915cad32c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:89c7bb5547d975cc3d11e0ae1a8ccc0351bf5fbc5335d2f5ddd2f35f6660c361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34de87369c83245725f8ef817f4b9e791ffcc508b41d1739e66e78f37aa131d9`

```dockerfile
```

-	Layers:
	-	`sha256:c32e99100ba19083df91a0159b4677528fb0e7aa00801be5cf350ba9ffa4b16e`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:9a651b22672c7151b5d8ca820ed2290b3fe4d4922e9b3f37ab14c8876da6613d
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
$ docker pull docker@sha256:63af38ad28e39198d32b84f6f0766b84f129223962a2b9d0d08895f82b8c974a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141018836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca75ab1d7a7464eafbb043969362b3580b89fc13d0a24015f05784cf1fbf4a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9f4cacdb6d1c7d18007496fd3fdc3e1a7db761aa9120a04950e745674e852fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d352174790d7d189910e7f5c3030976778ee363ffe05d6c5f85ddf5208ef9bb`

```dockerfile
```

-	Layers:
	-	`sha256:8c7368c1f564a9560c431962f192d16acdb099321d336f23a570f3eadb276e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1781a83e4d8da5abccfbc908e5a59f38842fb75fa3c92a6439f39b5ea582734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131692655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f764f0067ba36f35452a088c243700ee0a13f44b0d8398f4f41320126a60100`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52b5b50da000f825732faa0b306b0b03aba942958f60b4e4a267f64f2609725`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 7.0 MB (7036882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220971bcf994b5c3a2e140bbf3bf38830ebb2d208da3e028d0b4632a69131af`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 89.9 KB (89870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31279910422b314845644d11076adf1d5a5bf46d1bb9f5f946994d70718ba0c2`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972dc8fbd8a452f36a21a28edc3dca31c4f0cb12877b3cf4c19444a24c319082`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7f9370d4ba1a6b159b96643477be5fcd0428ad716dca0cd4ad4548d815dd5`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcbea16a18e4ce2926adfe5a067d7c48dc5df60be0750162782f6ca9e2790e1`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:dae7e1a430d410690e1ac8f97bb7ba4a9970db59b5bad071334209e728508e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fef12049e311755a88f6ed54bc48d4c1b8bf6bb0d141affdec32b274fee2fcd`

```dockerfile
```

-	Layers:
	-	`sha256:e82d1cdacd927eb5664586024dae2a1cb667e1b8faed9e64bbfb6354fea7fc01`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a06a9ae40437d600bc69403c9867d7c78bbd0261e1e8de585a9a1be038fc7e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130024916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef257cfb222c87f5b6aeb6bf1da8067196ecf6d7446a83c6120c78ccb0b4330`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a803a8a5b5db41392839b8d9e4b5dc98eb15e937e9a49ed46e2497676808283e`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 6.4 MB (6366128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53db656a9deda748d0137317b33e819676026a06a90003335d8129fd531e85`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 86.3 KB (86334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d755394c5b842899dd04ebc742660ce41ab0a2a14f38cf4d10e864b6dcffd5`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc2aa2417919467e58c0171cedbbd58423ec11584c3ed3285031ca790932146`  
		Last Modified: Tue, 04 Mar 2025 01:03:16 GMT  
		Size: 55.6 MB (55593637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eddd72049041d2e5083e7a7838eb4c6952dec7e4c186fe19c57d133194b086`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b244427612290e4f97cc15fb8e4f04d3b60140bf1ef1a77f18381bcdd2c51`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e63515a65dee56b94046151fdf91185c60bc937a4dcaaf24d898bc9f3a057cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4367ec966899922086d3466b68fade429c2841e0551179512fb2308774c3345`

```dockerfile
```

-	Layers:
	-	`sha256:649fb81baea829805bdd59d93b87a3c335ef4fc45d773b95dcc4fa47fa616e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:13 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90ca9797ce316bce5ff74d335c304e85d41d6bd981f755a3281858072bfc839a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132411588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0250bf64dd26b5fe7a1a358ac561aa69a69de05ac454d6de509ef789813a11`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f5b23b2ecb5219b4fd968f4f0e77e03bd1739c249efd6cd9743ff73138a96a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e084d1513f7ecd8f052a99a580b237130bd85603d5bacaacf72d2e9508170e20`

```dockerfile
```

-	Layers:
	-	`sha256:36cdd24344a437d2b167b4b38ada68f9f95a41ad871c683e3146b271a927edca`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:77dfe1ec10cdf5406214798bb37d7eae17b98d0dd1a8ce0cbd181e1e66ae8e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e61ae57240222f863c8a5b06b7cef58e30f0f0d0e151df70bd8b93dcb0add483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159173162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e4181b6a4dbfad3eda6a6cfe192fc9e5395c2b2e3dc7163b8049d8c8d3dae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cffb75e9d3a5007728e392783b97dc4c1457b0c9b5ed0d01c4b6f24414a8a3`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 986.6 KB (986572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2da6fe36e77ab8ccbc591eece09e51d53e8326f48eccb90161590497da92fb`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef728516ba2da965a49726affb6690ca64cca2c079d6990785b9717c4021ee30`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aa9b83388cba05ccc2d8cec1a786a6af3222350840d116b26e5f155e3eb05f`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 17.2 MB (17166413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde177038eb92e35753d04334ab44c59f7fd917a34d85872b666ccffafe69c44`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bbc21e77f41b8b6a40705c9e78a508d27da1c6c2b5cca32ef25f5d8aec78c1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95431ca3e37228cd8c5620454fe5e37fad72d2fe0452d170a71e3811d23fd298`

```dockerfile
```

-	Layers:
	-	`sha256:96d16732d86f704c5501d23bf1c915f1e338bbf89438ad4af2428a2ac063bed5`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8b7764fc03fe18004cf4f8645ed5a8cd81676ea1dafa744c15ead08f05118297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152706572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030ba4eec29973e85084b2475b96b3d968861321f544745a7690475756dd854c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2355ca5978c694d96707e17104bfa53213bbc301d053c1ad18d5848d62d7b95`  
		Last Modified: Tue, 04 Mar 2025 01:07:52 GMT  
		Size: 1.0 MB (1014205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7810dcc87146cd8f8d35999ec2eab9c9b96ec8db7cc0573bf600a6c9b6253f0f`  
		Last Modified: Tue, 04 Mar 2025 01:07:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fc3d18d4751d666afc8c89917cd8a0df97cc28f2e94d2b8554ac8e0e3fc35a`  
		Last Modified: Tue, 04 Mar 2025 01:07:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7088145dc16c08b39c911d6b5b95d35e16b264c54f9759eddefab033383fdb75`  
		Last Modified: Tue, 04 Mar 2025 01:07:52 GMT  
		Size: 19.3 MB (19279437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7163ac37a0e799a8e7e67df4c7e47106af035adff56fd17076dc8c001eb7b1d6`  
		Last Modified: Tue, 04 Mar 2025 01:07:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9231ac8f93e5816c1ba8a4867dbd89036e466b3eaa1729b2a20a1f59e97be229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfe83ec9fbf61240855ccdd060605d1fd5587cbca14cce35b775d471b52d89d`

```dockerfile
```

-	Layers:
	-	`sha256:228c43eddb59977bb2f12d9a6aef4d2fb06fa90ecb174f42e8ca898d410159a0`  
		Last Modified: Tue, 04 Mar 2025 01:07:51 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:888ccff3b9636b55646e6bb5477e92d060a93a2c17c21e6e1bddb8907b3667ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:c1f4df2f1e5249ae9c2805fbaa593bc9c8e76a8ed12a0436996d04e8b7cc038d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2973507774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f730146db9c7982e4e32e090d898ce8bb0203dcff5a072ab1825c8984f3af`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:47:14 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:47:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:47:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:47:26 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:47:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:47:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:47:36 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:47:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5db60003403b188f7c1530d269d228ed8fcb842beb2ef4ac0e0ffe3c87d610`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686d03d51200d5ae151d48672f750801918d278241e440704a22667d7d98b197`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 364.4 KB (364432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a92737683cf4c298dc0edec0672a162c28f51a4be547f12aa894d1bc1b9203`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98fe940464aaad024d9e1802e57ed753c43c1a3da5b7adcc82b0ab16cb0a5bd`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f6146091546c80b9879daf08ba51e90ae07e7ca2a0449b6e62db8ee4355ad2`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 19.8 MB (19832344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2a3f2b03cc567ce88efb88d37ec49e5878d1c065f3d3289b759b6f303d468b`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1efa5ff8dccab563d2fb407dba261e83538e10d8f6a52d55795eca8799e07`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a1f9cfcf1a770b8e0563e10af4fe4fd665d94dbf6202cbb5d6e70d77c47ca`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0ea793b63325756fa010233c0bcec2d5e2540ebd010c854b4871488e591249`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 22.8 MB (22757621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f5b3ea67a8a43b5157e213977222af56ae70e4f8e81817bc714e75892ea9fb`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f89fa36da2f4d182f429d1e909346499105d84b6de15f3c59f203ef327771e4`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4eaef42c69737e26a4f51b2ff86be0f80f023f1cf243c7f24b56c9f07c9125`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb16e071c42270350ca5102ef4475935e3249a11df250a83a637f0c4896a944`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 21.9 MB (21894006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:d857e60eee8f4ee9d71ea880c7faa05fbbf3965f724666008415847844f86520
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334710456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a256501bc1307f791a4185e872770e8b44e05680661816f7974a375494abe2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:53:55 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:53:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:54:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:06 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:54:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:54:08 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:54:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:54:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd0a29ac12f7f5357cfca6a7cb15badd5a2fc342a81bb77ac97698701afecd0`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016be76acd15c6840b1f3c249ab0e88aca806595f849ae4defae54014d672ed3`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 343.3 KB (343272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bba7d1b615e4aa5cf86abd0f490b746e40b90733a7ed5a7b931cc208008a0a`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a757b9a15d3fa1af7bb47a9620e1db135dc5b478b45df78506291e56a9dbcd2d`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608b6e007c175f8ae40b4011323b27a3bb45ab575d0d1ba663d62e371379c2aa`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 19.8 MB (19805728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9396c1d3ca9fd43dded5884b992f48110a5592d944cae25ac9f2739299f2b3e`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a093896c4308e2f82773042ec2d94e515963b7f483a79df82035d6b4e16e0`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2fa19931d46d88400ccbe12850373ec33422e71386cf418f0f31564f379c78`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819822354481476168a3af548619cbceceeae4c2a19a1ab2d2c49613b23d832`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 22.7 MB (22731872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923ebe1421f0c6d0754bd55e14ced92f03a796d4def86fb78edd3e143b9eb5e2`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b222136c7f0e28a6668c3f86bf7c5c39b749998b118cfe6535a5cd194057d40`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97d245b4a24d519ab255dfc31ebb0ed031408cb5df38803fedd776a39828f2b`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f118966c417c3afe3fc57523f23c754d770dd204bf1a7e23ff05c5ccb714b3e5`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 21.9 MB (21876802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:6ec89c50d8a2e7140122be3cc885817ef06db86ff79ab4959f230e563b152edb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216356810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb90c5ec050a045c16a9fcaf25f380389e43ed95b32e89c6754c3d5388ad1a2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:52:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:52:50 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:53:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:53:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:53:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aad9a715a375d2c8dbcf38b891c606580b3c469223f6a06ad300be69b95982`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f35846ff4f094309b4cb17bd9244228a41c1b24f785015035b360c10421eac`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 327.5 KB (327491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753e2664deb2e592c9acd1b487b8e2c541be824f4ab302d395d4a2a61e85ed1`  
		Last Modified: Wed, 12 Mar 2025 18:53:21 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf83ab28dea983722f41794eb1be6949042863a4e4d163096fe8a27f671bcab`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6102740590b962968e8e065bc558a49a14d55e5e20198483d48542470b76e62f`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 19.8 MB (19799094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4693030fb7a286223c350e8b41f2276f8edfec6f292227335cf7fd2dc838111d`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c35ff7e4e472d5368f2f8f84b0986949edd9cd33469def72a632a526cf8bb7`  
		Last Modified: Wed, 12 Mar 2025 18:53:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b5d10cb3dbeb63171a22ffa84f71ea66f067bc4f93b935cfc8e4e88d985f43`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88fed0b769948546d05ad2d707d73d67046f51ae307c46737ace9ce1a3ec1b9`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 22.7 MB (22723657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc8cce8f76304d63d169b17d38a8634765c802bd0c32240d8df737ab81d325`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fed1f356a2be26f78799e2e2a795459a1cb01fee11bbc19d73be193980e8b6`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450b3ffc1b8b10ce5152ee50cb2cf841409eeab832e78cda33e44710d8d9c1f3`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d330fcb490da82d9eb119a9deebdac8dd6a40333e12f3f49b0500bc871119ae1`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 21.9 MB (21860255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:061a40406076ff8843375da449424a3c19052bb114078bab3189d8cb3d4cc72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:6ec89c50d8a2e7140122be3cc885817ef06db86ff79ab4959f230e563b152edb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216356810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb90c5ec050a045c16a9fcaf25f380389e43ed95b32e89c6754c3d5388ad1a2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:52:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:52:50 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:53:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:53:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:53:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aad9a715a375d2c8dbcf38b891c606580b3c469223f6a06ad300be69b95982`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f35846ff4f094309b4cb17bd9244228a41c1b24f785015035b360c10421eac`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 327.5 KB (327491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753e2664deb2e592c9acd1b487b8e2c541be824f4ab302d395d4a2a61e85ed1`  
		Last Modified: Wed, 12 Mar 2025 18:53:21 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf83ab28dea983722f41794eb1be6949042863a4e4d163096fe8a27f671bcab`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6102740590b962968e8e065bc558a49a14d55e5e20198483d48542470b76e62f`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 19.8 MB (19799094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4693030fb7a286223c350e8b41f2276f8edfec6f292227335cf7fd2dc838111d`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c35ff7e4e472d5368f2f8f84b0986949edd9cd33469def72a632a526cf8bb7`  
		Last Modified: Wed, 12 Mar 2025 18:53:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b5d10cb3dbeb63171a22ffa84f71ea66f067bc4f93b935cfc8e4e88d985f43`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88fed0b769948546d05ad2d707d73d67046f51ae307c46737ace9ce1a3ec1b9`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 22.7 MB (22723657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc8cce8f76304d63d169b17d38a8634765c802bd0c32240d8df737ab81d325`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fed1f356a2be26f78799e2e2a795459a1cb01fee11bbc19d73be193980e8b6`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450b3ffc1b8b10ce5152ee50cb2cf841409eeab832e78cda33e44710d8d9c1f3`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d330fcb490da82d9eb119a9deebdac8dd6a40333e12f3f49b0500bc871119ae1`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 21.9 MB (21860255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fa4d958eb2453fec999de01713c508b53a971fbbed9f3bcda63fbe7a275ec92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:d857e60eee8f4ee9d71ea880c7faa05fbbf3965f724666008415847844f86520
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334710456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a256501bc1307f791a4185e872770e8b44e05680661816f7974a375494abe2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:53:55 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:53:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:54:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:06 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:54:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:54:08 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:54:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:54:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd0a29ac12f7f5357cfca6a7cb15badd5a2fc342a81bb77ac97698701afecd0`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016be76acd15c6840b1f3c249ab0e88aca806595f849ae4defae54014d672ed3`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 343.3 KB (343272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bba7d1b615e4aa5cf86abd0f490b746e40b90733a7ed5a7b931cc208008a0a`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a757b9a15d3fa1af7bb47a9620e1db135dc5b478b45df78506291e56a9dbcd2d`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608b6e007c175f8ae40b4011323b27a3bb45ab575d0d1ba663d62e371379c2aa`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 19.8 MB (19805728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9396c1d3ca9fd43dded5884b992f48110a5592d944cae25ac9f2739299f2b3e`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a093896c4308e2f82773042ec2d94e515963b7f483a79df82035d6b4e16e0`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2fa19931d46d88400ccbe12850373ec33422e71386cf418f0f31564f379c78`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819822354481476168a3af548619cbceceeae4c2a19a1ab2d2c49613b23d832`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 22.7 MB (22731872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923ebe1421f0c6d0754bd55e14ced92f03a796d4def86fb78edd3e143b9eb5e2`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b222136c7f0e28a6668c3f86bf7c5c39b749998b118cfe6535a5cd194057d40`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97d245b4a24d519ab255dfc31ebb0ed031408cb5df38803fedd776a39828f2b`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f118966c417c3afe3fc57523f23c754d770dd204bf1a7e23ff05c5ccb714b3e5`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 21.9 MB (21876802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:c1ee7176bc33fb9f8af5afecd2334b44191b9c56c7a64103d001ad7c5984aa31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:c1f4df2f1e5249ae9c2805fbaa593bc9c8e76a8ed12a0436996d04e8b7cc038d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2973507774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f730146db9c7982e4e32e090d898ce8bb0203dcff5a072ab1825c8984f3af`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:47:14 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:47:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:47:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:47:26 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:47:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:47:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:47:36 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:47:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5db60003403b188f7c1530d269d228ed8fcb842beb2ef4ac0e0ffe3c87d610`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686d03d51200d5ae151d48672f750801918d278241e440704a22667d7d98b197`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 364.4 KB (364432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a92737683cf4c298dc0edec0672a162c28f51a4be547f12aa894d1bc1b9203`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98fe940464aaad024d9e1802e57ed753c43c1a3da5b7adcc82b0ab16cb0a5bd`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f6146091546c80b9879daf08ba51e90ae07e7ca2a0449b6e62db8ee4355ad2`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 19.8 MB (19832344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2a3f2b03cc567ce88efb88d37ec49e5878d1c065f3d3289b759b6f303d468b`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1efa5ff8dccab563d2fb407dba261e83538e10d8f6a52d55795eca8799e07`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a1f9cfcf1a770b8e0563e10af4fe4fd665d94dbf6202cbb5d6e70d77c47ca`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0ea793b63325756fa010233c0bcec2d5e2540ebd010c854b4871488e591249`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 22.8 MB (22757621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f5b3ea67a8a43b5157e213977222af56ae70e4f8e81817bc714e75892ea9fb`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f89fa36da2f4d182f429d1e909346499105d84b6de15f3c59f203ef327771e4`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4eaef42c69737e26a4f51b2ff86be0f80f023f1cf243c7f24b56c9f07c9125`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb16e071c42270350ca5102ef4475935e3249a11df250a83a637f0c4896a944`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 21.9 MB (21894006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0`

```console
$ docker pull docker@sha256:9a651b22672c7151b5d8ca820ed2290b3fe4d4922e9b3f37ab14c8876da6613d
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

### `docker:28.0` - linux; amd64

```console
$ docker pull docker@sha256:63af38ad28e39198d32b84f6f0766b84f129223962a2b9d0d08895f82b8c974a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141018836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca75ab1d7a7464eafbb043969362b3580b89fc13d0a24015f05784cf1fbf4a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:9f4cacdb6d1c7d18007496fd3fdc3e1a7db761aa9120a04950e745674e852fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d352174790d7d189910e7f5c3030976778ee363ffe05d6c5f85ddf5208ef9bb`

```dockerfile
```

-	Layers:
	-	`sha256:8c7368c1f564a9560c431962f192d16acdb099321d336f23a570f3eadb276e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1781a83e4d8da5abccfbc908e5a59f38842fb75fa3c92a6439f39b5ea582734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131692655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f764f0067ba36f35452a088c243700ee0a13f44b0d8398f4f41320126a60100`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52b5b50da000f825732faa0b306b0b03aba942958f60b4e4a267f64f2609725`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 7.0 MB (7036882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220971bcf994b5c3a2e140bbf3bf38830ebb2d208da3e028d0b4632a69131af`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 89.9 KB (89870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31279910422b314845644d11076adf1d5a5bf46d1bb9f5f946994d70718ba0c2`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972dc8fbd8a452f36a21a28edc3dca31c4f0cb12877b3cf4c19444a24c319082`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7f9370d4ba1a6b159b96643477be5fcd0428ad716dca0cd4ad4548d815dd5`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcbea16a18e4ce2926adfe5a067d7c48dc5df60be0750162782f6ca9e2790e1`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:dae7e1a430d410690e1ac8f97bb7ba4a9970db59b5bad071334209e728508e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fef12049e311755a88f6ed54bc48d4c1b8bf6bb0d141affdec32b274fee2fcd`

```dockerfile
```

-	Layers:
	-	`sha256:e82d1cdacd927eb5664586024dae2a1cb667e1b8faed9e64bbfb6354fea7fc01`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:a06a9ae40437d600bc69403c9867d7c78bbd0261e1e8de585a9a1be038fc7e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130024916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef257cfb222c87f5b6aeb6bf1da8067196ecf6d7446a83c6120c78ccb0b4330`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a803a8a5b5db41392839b8d9e4b5dc98eb15e937e9a49ed46e2497676808283e`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 6.4 MB (6366128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53db656a9deda748d0137317b33e819676026a06a90003335d8129fd531e85`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 86.3 KB (86334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d755394c5b842899dd04ebc742660ce41ab0a2a14f38cf4d10e864b6dcffd5`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc2aa2417919467e58c0171cedbbd58423ec11584c3ed3285031ca790932146`  
		Last Modified: Tue, 04 Mar 2025 01:03:16 GMT  
		Size: 55.6 MB (55593637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eddd72049041d2e5083e7a7838eb4c6952dec7e4c186fe19c57d133194b086`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b244427612290e4f97cc15fb8e4f04d3b60140bf1ef1a77f18381bcdd2c51`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:e63515a65dee56b94046151fdf91185c60bc937a4dcaaf24d898bc9f3a057cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4367ec966899922086d3466b68fade429c2841e0551179512fb2308774c3345`

```dockerfile
```

-	Layers:
	-	`sha256:649fb81baea829805bdd59d93b87a3c335ef4fc45d773b95dcc4fa47fa616e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:13 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90ca9797ce316bce5ff74d335c304e85d41d6bd981f755a3281858072bfc839a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132411588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0250bf64dd26b5fe7a1a358ac561aa69a69de05ac454d6de509ef789813a11`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:f5b23b2ecb5219b4fd968f4f0e77e03bd1739c249efd6cd9743ff73138a96a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e084d1513f7ecd8f052a99a580b237130bd85603d5bacaacf72d2e9508170e20`

```dockerfile
```

-	Layers:
	-	`sha256:36cdd24344a437d2b167b4b38ada68f9f95a41ad871c683e3146b271a927edca`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-cli`

```console
$ docker pull docker@sha256:79bf825c5bed0d579820cc19f6857738abc424a680b619171591e969114f2015
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

### `docker:28.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:407b05f8635f0c78530a074e5ac3d7ca547e494f41d0b8279eb378c957d59eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73996743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7ace64e87a3531934d9d783dd55b09fba672037fb47361e760477742f81dbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e83e577007c54ec761b3cc9df69167cff393d56c84b9982c5aeaff3dc875c360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb394d129acd56043f7f5fb7f10a740ff52c5b301d50e34652f30fc3f4968535`

```dockerfile
```

-	Layers:
	-	`sha256:4e8c6e0b6ddceec47cfd0a4b2d23a912d8a9825b3412c2492d4162b91835a3ee`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:eeb4ad44bd101ca297d84a0a0c3d0a65e9c0b45a038e0311f029cf84ea075f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68966316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9dc49b493ad218febee37e481279ef5472fa3bb9a9c005a77ea867233c0fda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc9b040b7560289fbd5081459c6b6ddecaaf4363ef2436ae6c2b925e0382e3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d631428cc9605f46e62098c617996c4c90c97ed9efb14436c836857db508b29`

```dockerfile
```

-	Layers:
	-	`sha256:1fcd6fd391dd1a77f96dadcb8f3583ac995b301d90af68b3d9e3b9937c3213d9`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:da6f62e7a4822d683c95524b9c38b7e39d43633a4d518865fc88807116650172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67972911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1523a85a50b40de6aa255336254486bbf1dc534c39a0f2dcb7a5f69afffde5d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1c453d9c45321fd866c5830abe9036744fd50ea31aef24f0fd5b441f600d0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310b7edd1a05f5a6b1de9c12d0a3fd30be28798ce7d656f5b306158eb590c45c`

```dockerfile
```

-	Layers:
	-	`sha256:da87a8f3030a2c4d7a3e171d90c90259cecb58ab16f1f9570b999f97d340a6c6`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0e8384ace3dbca30fdface67dd29a8510a7285efdd842c51949e027ec0276891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69760973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a211b50f388cffbcec654f2c7e6951b74377f9657875d06fad2bc3915cad32c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:89c7bb5547d975cc3d11e0ae1a8ccc0351bf5fbc5335d2f5ddd2f35f6660c361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34de87369c83245725f8ef817f4b9e791ffcc508b41d1739e66e78f37aa131d9`

```dockerfile
```

-	Layers:
	-	`sha256:c32e99100ba19083df91a0159b4677528fb0e7aa00801be5cf350ba9ffa4b16e`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-dind`

```console
$ docker pull docker@sha256:9a651b22672c7151b5d8ca820ed2290b3fe4d4922e9b3f37ab14c8876da6613d
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

### `docker:28.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:63af38ad28e39198d32b84f6f0766b84f129223962a2b9d0d08895f82b8c974a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141018836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca75ab1d7a7464eafbb043969362b3580b89fc13d0a24015f05784cf1fbf4a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9f4cacdb6d1c7d18007496fd3fdc3e1a7db761aa9120a04950e745674e852fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d352174790d7d189910e7f5c3030976778ee363ffe05d6c5f85ddf5208ef9bb`

```dockerfile
```

-	Layers:
	-	`sha256:8c7368c1f564a9560c431962f192d16acdb099321d336f23a570f3eadb276e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1781a83e4d8da5abccfbc908e5a59f38842fb75fa3c92a6439f39b5ea582734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131692655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f764f0067ba36f35452a088c243700ee0a13f44b0d8398f4f41320126a60100`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52b5b50da000f825732faa0b306b0b03aba942958f60b4e4a267f64f2609725`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 7.0 MB (7036882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220971bcf994b5c3a2e140bbf3bf38830ebb2d208da3e028d0b4632a69131af`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 89.9 KB (89870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31279910422b314845644d11076adf1d5a5bf46d1bb9f5f946994d70718ba0c2`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972dc8fbd8a452f36a21a28edc3dca31c4f0cb12877b3cf4c19444a24c319082`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7f9370d4ba1a6b159b96643477be5fcd0428ad716dca0cd4ad4548d815dd5`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcbea16a18e4ce2926adfe5a067d7c48dc5df60be0750162782f6ca9e2790e1`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:dae7e1a430d410690e1ac8f97bb7ba4a9970db59b5bad071334209e728508e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fef12049e311755a88f6ed54bc48d4c1b8bf6bb0d141affdec32b274fee2fcd`

```dockerfile
```

-	Layers:
	-	`sha256:e82d1cdacd927eb5664586024dae2a1cb667e1b8faed9e64bbfb6354fea7fc01`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a06a9ae40437d600bc69403c9867d7c78bbd0261e1e8de585a9a1be038fc7e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130024916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef257cfb222c87f5b6aeb6bf1da8067196ecf6d7446a83c6120c78ccb0b4330`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a803a8a5b5db41392839b8d9e4b5dc98eb15e937e9a49ed46e2497676808283e`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 6.4 MB (6366128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53db656a9deda748d0137317b33e819676026a06a90003335d8129fd531e85`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 86.3 KB (86334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d755394c5b842899dd04ebc742660ce41ab0a2a14f38cf4d10e864b6dcffd5`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc2aa2417919467e58c0171cedbbd58423ec11584c3ed3285031ca790932146`  
		Last Modified: Tue, 04 Mar 2025 01:03:16 GMT  
		Size: 55.6 MB (55593637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eddd72049041d2e5083e7a7838eb4c6952dec7e4c186fe19c57d133194b086`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b244427612290e4f97cc15fb8e4f04d3b60140bf1ef1a77f18381bcdd2c51`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e63515a65dee56b94046151fdf91185c60bc937a4dcaaf24d898bc9f3a057cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4367ec966899922086d3466b68fade429c2841e0551179512fb2308774c3345`

```dockerfile
```

-	Layers:
	-	`sha256:649fb81baea829805bdd59d93b87a3c335ef4fc45d773b95dcc4fa47fa616e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:13 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90ca9797ce316bce5ff74d335c304e85d41d6bd981f755a3281858072bfc839a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132411588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0250bf64dd26b5fe7a1a358ac561aa69a69de05ac454d6de509ef789813a11`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f5b23b2ecb5219b4fd968f4f0e77e03bd1739c249efd6cd9743ff73138a96a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e084d1513f7ecd8f052a99a580b237130bd85603d5bacaacf72d2e9508170e20`

```dockerfile
```

-	Layers:
	-	`sha256:36cdd24344a437d2b167b4b38ada68f9f95a41ad871c683e3146b271a927edca`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-dind-rootless`

```console
$ docker pull docker@sha256:77dfe1ec10cdf5406214798bb37d7eae17b98d0dd1a8ce0cbd181e1e66ae8e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e61ae57240222f863c8a5b06b7cef58e30f0f0d0e151df70bd8b93dcb0add483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159173162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e4181b6a4dbfad3eda6a6cfe192fc9e5395c2b2e3dc7163b8049d8c8d3dae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cffb75e9d3a5007728e392783b97dc4c1457b0c9b5ed0d01c4b6f24414a8a3`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 986.6 KB (986572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2da6fe36e77ab8ccbc591eece09e51d53e8326f48eccb90161590497da92fb`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef728516ba2da965a49726affb6690ca64cca2c079d6990785b9717c4021ee30`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aa9b83388cba05ccc2d8cec1a786a6af3222350840d116b26e5f155e3eb05f`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 17.2 MB (17166413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde177038eb92e35753d04334ab44c59f7fd917a34d85872b666ccffafe69c44`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bbc21e77f41b8b6a40705c9e78a508d27da1c6c2b5cca32ef25f5d8aec78c1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95431ca3e37228cd8c5620454fe5e37fad72d2fe0452d170a71e3811d23fd298`

```dockerfile
```

-	Layers:
	-	`sha256:96d16732d86f704c5501d23bf1c915f1e338bbf89438ad4af2428a2ac063bed5`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8b7764fc03fe18004cf4f8645ed5a8cd81676ea1dafa744c15ead08f05118297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152706572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030ba4eec29973e85084b2475b96b3d968861321f544745a7690475756dd854c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2355ca5978c694d96707e17104bfa53213bbc301d053c1ad18d5848d62d7b95`  
		Last Modified: Tue, 04 Mar 2025 01:07:52 GMT  
		Size: 1.0 MB (1014205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7810dcc87146cd8f8d35999ec2eab9c9b96ec8db7cc0573bf600a6c9b6253f0f`  
		Last Modified: Tue, 04 Mar 2025 01:07:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fc3d18d4751d666afc8c89917cd8a0df97cc28f2e94d2b8554ac8e0e3fc35a`  
		Last Modified: Tue, 04 Mar 2025 01:07:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7088145dc16c08b39c911d6b5b95d35e16b264c54f9759eddefab033383fdb75`  
		Last Modified: Tue, 04 Mar 2025 01:07:52 GMT  
		Size: 19.3 MB (19279437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7163ac37a0e799a8e7e67df4c7e47106af035adff56fd17076dc8c001eb7b1d6`  
		Last Modified: Tue, 04 Mar 2025 01:07:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9231ac8f93e5816c1ba8a4867dbd89036e466b3eaa1729b2a20a1f59e97be229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfe83ec9fbf61240855ccdd060605d1fd5587cbca14cce35b775d471b52d89d`

```dockerfile
```

-	Layers:
	-	`sha256:228c43eddb59977bb2f12d9a6aef4d2fb06fa90ecb174f42e8ca898d410159a0`  
		Last Modified: Tue, 04 Mar 2025 01:07:51 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-windowsservercore`

```console
$ docker pull docker@sha256:888ccff3b9636b55646e6bb5477e92d060a93a2c17c21e6e1bddb8907b3667ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:28.0-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:c1f4df2f1e5249ae9c2805fbaa593bc9c8e76a8ed12a0436996d04e8b7cc038d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2973507774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f730146db9c7982e4e32e090d898ce8bb0203dcff5a072ab1825c8984f3af`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:47:14 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:47:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:47:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:47:26 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:47:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:47:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:47:36 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:47:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5db60003403b188f7c1530d269d228ed8fcb842beb2ef4ac0e0ffe3c87d610`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686d03d51200d5ae151d48672f750801918d278241e440704a22667d7d98b197`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 364.4 KB (364432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a92737683cf4c298dc0edec0672a162c28f51a4be547f12aa894d1bc1b9203`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98fe940464aaad024d9e1802e57ed753c43c1a3da5b7adcc82b0ab16cb0a5bd`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f6146091546c80b9879daf08ba51e90ae07e7ca2a0449b6e62db8ee4355ad2`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 19.8 MB (19832344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2a3f2b03cc567ce88efb88d37ec49e5878d1c065f3d3289b759b6f303d468b`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1efa5ff8dccab563d2fb407dba261e83538e10d8f6a52d55795eca8799e07`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a1f9cfcf1a770b8e0563e10af4fe4fd665d94dbf6202cbb5d6e70d77c47ca`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0ea793b63325756fa010233c0bcec2d5e2540ebd010c854b4871488e591249`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 22.8 MB (22757621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f5b3ea67a8a43b5157e213977222af56ae70e4f8e81817bc714e75892ea9fb`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f89fa36da2f4d182f429d1e909346499105d84b6de15f3c59f203ef327771e4`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4eaef42c69737e26a4f51b2ff86be0f80f023f1cf243c7f24b56c9f07c9125`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb16e071c42270350ca5102ef4475935e3249a11df250a83a637f0c4896a944`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 21.9 MB (21894006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:d857e60eee8f4ee9d71ea880c7faa05fbbf3965f724666008415847844f86520
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334710456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a256501bc1307f791a4185e872770e8b44e05680661816f7974a375494abe2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:53:55 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:53:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:54:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:06 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:54:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:54:08 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:54:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:54:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd0a29ac12f7f5357cfca6a7cb15badd5a2fc342a81bb77ac97698701afecd0`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016be76acd15c6840b1f3c249ab0e88aca806595f849ae4defae54014d672ed3`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 343.3 KB (343272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bba7d1b615e4aa5cf86abd0f490b746e40b90733a7ed5a7b931cc208008a0a`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a757b9a15d3fa1af7bb47a9620e1db135dc5b478b45df78506291e56a9dbcd2d`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608b6e007c175f8ae40b4011323b27a3bb45ab575d0d1ba663d62e371379c2aa`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 19.8 MB (19805728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9396c1d3ca9fd43dded5884b992f48110a5592d944cae25ac9f2739299f2b3e`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a093896c4308e2f82773042ec2d94e515963b7f483a79df82035d6b4e16e0`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2fa19931d46d88400ccbe12850373ec33422e71386cf418f0f31564f379c78`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819822354481476168a3af548619cbceceeae4c2a19a1ab2d2c49613b23d832`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 22.7 MB (22731872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923ebe1421f0c6d0754bd55e14ced92f03a796d4def86fb78edd3e143b9eb5e2`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b222136c7f0e28a6668c3f86bf7c5c39b749998b118cfe6535a5cd194057d40`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97d245b4a24d519ab255dfc31ebb0ed031408cb5df38803fedd776a39828f2b`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f118966c417c3afe3fc57523f23c754d770dd204bf1a7e23ff05c5ccb714b3e5`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 21.9 MB (21876802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:6ec89c50d8a2e7140122be3cc885817ef06db86ff79ab4959f230e563b152edb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216356810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb90c5ec050a045c16a9fcaf25f380389e43ed95b32e89c6754c3d5388ad1a2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:52:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:52:50 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:53:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:53:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:53:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aad9a715a375d2c8dbcf38b891c606580b3c469223f6a06ad300be69b95982`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f35846ff4f094309b4cb17bd9244228a41c1b24f785015035b360c10421eac`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 327.5 KB (327491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753e2664deb2e592c9acd1b487b8e2c541be824f4ab302d395d4a2a61e85ed1`  
		Last Modified: Wed, 12 Mar 2025 18:53:21 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf83ab28dea983722f41794eb1be6949042863a4e4d163096fe8a27f671bcab`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6102740590b962968e8e065bc558a49a14d55e5e20198483d48542470b76e62f`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 19.8 MB (19799094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4693030fb7a286223c350e8b41f2276f8edfec6f292227335cf7fd2dc838111d`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c35ff7e4e472d5368f2f8f84b0986949edd9cd33469def72a632a526cf8bb7`  
		Last Modified: Wed, 12 Mar 2025 18:53:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b5d10cb3dbeb63171a22ffa84f71ea66f067bc4f93b935cfc8e4e88d985f43`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88fed0b769948546d05ad2d707d73d67046f51ae307c46737ace9ce1a3ec1b9`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 22.7 MB (22723657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc8cce8f76304d63d169b17d38a8634765c802bd0c32240d8df737ab81d325`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fed1f356a2be26f78799e2e2a795459a1cb01fee11bbc19d73be193980e8b6`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450b3ffc1b8b10ce5152ee50cb2cf841409eeab832e78cda33e44710d8d9c1f3`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d330fcb490da82d9eb119a9deebdac8dd6a40333e12f3f49b0500bc871119ae1`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 21.9 MB (21860255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:061a40406076ff8843375da449424a3c19052bb114078bab3189d8cb3d4cc72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:28.0-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:6ec89c50d8a2e7140122be3cc885817ef06db86ff79ab4959f230e563b152edb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216356810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb90c5ec050a045c16a9fcaf25f380389e43ed95b32e89c6754c3d5388ad1a2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:52:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:52:50 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:53:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:53:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:53:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aad9a715a375d2c8dbcf38b891c606580b3c469223f6a06ad300be69b95982`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f35846ff4f094309b4cb17bd9244228a41c1b24f785015035b360c10421eac`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 327.5 KB (327491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753e2664deb2e592c9acd1b487b8e2c541be824f4ab302d395d4a2a61e85ed1`  
		Last Modified: Wed, 12 Mar 2025 18:53:21 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf83ab28dea983722f41794eb1be6949042863a4e4d163096fe8a27f671bcab`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6102740590b962968e8e065bc558a49a14d55e5e20198483d48542470b76e62f`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 19.8 MB (19799094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4693030fb7a286223c350e8b41f2276f8edfec6f292227335cf7fd2dc838111d`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c35ff7e4e472d5368f2f8f84b0986949edd9cd33469def72a632a526cf8bb7`  
		Last Modified: Wed, 12 Mar 2025 18:53:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b5d10cb3dbeb63171a22ffa84f71ea66f067bc4f93b935cfc8e4e88d985f43`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88fed0b769948546d05ad2d707d73d67046f51ae307c46737ace9ce1a3ec1b9`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 22.7 MB (22723657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc8cce8f76304d63d169b17d38a8634765c802bd0c32240d8df737ab81d325`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fed1f356a2be26f78799e2e2a795459a1cb01fee11bbc19d73be193980e8b6`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450b3ffc1b8b10ce5152ee50cb2cf841409eeab832e78cda33e44710d8d9c1f3`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d330fcb490da82d9eb119a9deebdac8dd6a40333e12f3f49b0500bc871119ae1`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 21.9 MB (21860255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fa4d958eb2453fec999de01713c508b53a971fbbed9f3bcda63fbe7a275ec92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:28.0-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:d857e60eee8f4ee9d71ea880c7faa05fbbf3965f724666008415847844f86520
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334710456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a256501bc1307f791a4185e872770e8b44e05680661816f7974a375494abe2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:53:55 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:53:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:54:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:06 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:54:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:54:08 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:54:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:54:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd0a29ac12f7f5357cfca6a7cb15badd5a2fc342a81bb77ac97698701afecd0`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016be76acd15c6840b1f3c249ab0e88aca806595f849ae4defae54014d672ed3`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 343.3 KB (343272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bba7d1b615e4aa5cf86abd0f490b746e40b90733a7ed5a7b931cc208008a0a`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a757b9a15d3fa1af7bb47a9620e1db135dc5b478b45df78506291e56a9dbcd2d`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608b6e007c175f8ae40b4011323b27a3bb45ab575d0d1ba663d62e371379c2aa`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 19.8 MB (19805728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9396c1d3ca9fd43dded5884b992f48110a5592d944cae25ac9f2739299f2b3e`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a093896c4308e2f82773042ec2d94e515963b7f483a79df82035d6b4e16e0`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2fa19931d46d88400ccbe12850373ec33422e71386cf418f0f31564f379c78`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819822354481476168a3af548619cbceceeae4c2a19a1ab2d2c49613b23d832`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 22.7 MB (22731872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923ebe1421f0c6d0754bd55e14ced92f03a796d4def86fb78edd3e143b9eb5e2`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b222136c7f0e28a6668c3f86bf7c5c39b749998b118cfe6535a5cd194057d40`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97d245b4a24d519ab255dfc31ebb0ed031408cb5df38803fedd776a39828f2b`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f118966c417c3afe3fc57523f23c754d770dd204bf1a7e23ff05c5ccb714b3e5`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 21.9 MB (21876802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:c1ee7176bc33fb9f8af5afecd2334b44191b9c56c7a64103d001ad7c5984aa31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:28.0-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:c1f4df2f1e5249ae9c2805fbaa593bc9c8e76a8ed12a0436996d04e8b7cc038d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2973507774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f730146db9c7982e4e32e090d898ce8bb0203dcff5a072ab1825c8984f3af`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:47:14 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:47:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:47:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:47:26 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:47:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:47:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:47:36 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:47:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5db60003403b188f7c1530d269d228ed8fcb842beb2ef4ac0e0ffe3c87d610`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686d03d51200d5ae151d48672f750801918d278241e440704a22667d7d98b197`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 364.4 KB (364432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a92737683cf4c298dc0edec0672a162c28f51a4be547f12aa894d1bc1b9203`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98fe940464aaad024d9e1802e57ed753c43c1a3da5b7adcc82b0ab16cb0a5bd`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f6146091546c80b9879daf08ba51e90ae07e7ca2a0449b6e62db8ee4355ad2`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 19.8 MB (19832344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2a3f2b03cc567ce88efb88d37ec49e5878d1c065f3d3289b759b6f303d468b`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1efa5ff8dccab563d2fb407dba261e83538e10d8f6a52d55795eca8799e07`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a1f9cfcf1a770b8e0563e10af4fe4fd665d94dbf6202cbb5d6e70d77c47ca`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0ea793b63325756fa010233c0bcec2d5e2540ebd010c854b4871488e591249`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 22.8 MB (22757621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f5b3ea67a8a43b5157e213977222af56ae70e4f8e81817bc714e75892ea9fb`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f89fa36da2f4d182f429d1e909346499105d84b6de15f3c59f203ef327771e4`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4eaef42c69737e26a4f51b2ff86be0f80f023f1cf243c7f24b56c9f07c9125`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb16e071c42270350ca5102ef4475935e3249a11df250a83a637f0c4896a944`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 21.9 MB (21894006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.1`

```console
$ docker pull docker@sha256:9a651b22672c7151b5d8ca820ed2290b3fe4d4922e9b3f37ab14c8876da6613d
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

### `docker:28.0.1` - linux; amd64

```console
$ docker pull docker@sha256:63af38ad28e39198d32b84f6f0766b84f129223962a2b9d0d08895f82b8c974a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141018836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca75ab1d7a7464eafbb043969362b3580b89fc13d0a24015f05784cf1fbf4a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1` - unknown; unknown

```console
$ docker pull docker@sha256:9f4cacdb6d1c7d18007496fd3fdc3e1a7db761aa9120a04950e745674e852fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d352174790d7d189910e7f5c3030976778ee363ffe05d6c5f85ddf5208ef9bb`

```dockerfile
```

-	Layers:
	-	`sha256:8c7368c1f564a9560c431962f192d16acdb099321d336f23a570f3eadb276e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1781a83e4d8da5abccfbc908e5a59f38842fb75fa3c92a6439f39b5ea582734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131692655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f764f0067ba36f35452a088c243700ee0a13f44b0d8398f4f41320126a60100`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52b5b50da000f825732faa0b306b0b03aba942958f60b4e4a267f64f2609725`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 7.0 MB (7036882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220971bcf994b5c3a2e140bbf3bf38830ebb2d208da3e028d0b4632a69131af`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 89.9 KB (89870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31279910422b314845644d11076adf1d5a5bf46d1bb9f5f946994d70718ba0c2`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972dc8fbd8a452f36a21a28edc3dca31c4f0cb12877b3cf4c19444a24c319082`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7f9370d4ba1a6b159b96643477be5fcd0428ad716dca0cd4ad4548d815dd5`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcbea16a18e4ce2926adfe5a067d7c48dc5df60be0750162782f6ca9e2790e1`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1` - unknown; unknown

```console
$ docker pull docker@sha256:dae7e1a430d410690e1ac8f97bb7ba4a9970db59b5bad071334209e728508e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fef12049e311755a88f6ed54bc48d4c1b8bf6bb0d141affdec32b274fee2fcd`

```dockerfile
```

-	Layers:
	-	`sha256:e82d1cdacd927eb5664586024dae2a1cb667e1b8faed9e64bbfb6354fea7fc01`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:a06a9ae40437d600bc69403c9867d7c78bbd0261e1e8de585a9a1be038fc7e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130024916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef257cfb222c87f5b6aeb6bf1da8067196ecf6d7446a83c6120c78ccb0b4330`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a803a8a5b5db41392839b8d9e4b5dc98eb15e937e9a49ed46e2497676808283e`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 6.4 MB (6366128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53db656a9deda748d0137317b33e819676026a06a90003335d8129fd531e85`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 86.3 KB (86334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d755394c5b842899dd04ebc742660ce41ab0a2a14f38cf4d10e864b6dcffd5`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc2aa2417919467e58c0171cedbbd58423ec11584c3ed3285031ca790932146`  
		Last Modified: Tue, 04 Mar 2025 01:03:16 GMT  
		Size: 55.6 MB (55593637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eddd72049041d2e5083e7a7838eb4c6952dec7e4c186fe19c57d133194b086`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b244427612290e4f97cc15fb8e4f04d3b60140bf1ef1a77f18381bcdd2c51`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1` - unknown; unknown

```console
$ docker pull docker@sha256:e63515a65dee56b94046151fdf91185c60bc937a4dcaaf24d898bc9f3a057cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4367ec966899922086d3466b68fade429c2841e0551179512fb2308774c3345`

```dockerfile
```

-	Layers:
	-	`sha256:649fb81baea829805bdd59d93b87a3c335ef4fc45d773b95dcc4fa47fa616e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:13 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90ca9797ce316bce5ff74d335c304e85d41d6bd981f755a3281858072bfc839a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132411588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0250bf64dd26b5fe7a1a358ac561aa69a69de05ac454d6de509ef789813a11`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1` - unknown; unknown

```console
$ docker pull docker@sha256:f5b23b2ecb5219b4fd968f4f0e77e03bd1739c249efd6cd9743ff73138a96a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e084d1513f7ecd8f052a99a580b237130bd85603d5bacaacf72d2e9508170e20`

```dockerfile
```

-	Layers:
	-	`sha256:36cdd24344a437d2b167b4b38ada68f9f95a41ad871c683e3146b271a927edca`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-alpine3.21`

```console
$ docker pull docker@sha256:9a651b22672c7151b5d8ca820ed2290b3fe4d4922e9b3f37ab14c8876da6613d
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

### `docker:28.0.1-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:63af38ad28e39198d32b84f6f0766b84f129223962a2b9d0d08895f82b8c974a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141018836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca75ab1d7a7464eafbb043969362b3580b89fc13d0a24015f05784cf1fbf4a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:9f4cacdb6d1c7d18007496fd3fdc3e1a7db761aa9120a04950e745674e852fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d352174790d7d189910e7f5c3030976778ee363ffe05d6c5f85ddf5208ef9bb`

```dockerfile
```

-	Layers:
	-	`sha256:8c7368c1f564a9560c431962f192d16acdb099321d336f23a570f3eadb276e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1781a83e4d8da5abccfbc908e5a59f38842fb75fa3c92a6439f39b5ea582734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131692655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f764f0067ba36f35452a088c243700ee0a13f44b0d8398f4f41320126a60100`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52b5b50da000f825732faa0b306b0b03aba942958f60b4e4a267f64f2609725`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 7.0 MB (7036882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220971bcf994b5c3a2e140bbf3bf38830ebb2d208da3e028d0b4632a69131af`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 89.9 KB (89870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31279910422b314845644d11076adf1d5a5bf46d1bb9f5f946994d70718ba0c2`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972dc8fbd8a452f36a21a28edc3dca31c4f0cb12877b3cf4c19444a24c319082`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7f9370d4ba1a6b159b96643477be5fcd0428ad716dca0cd4ad4548d815dd5`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcbea16a18e4ce2926adfe5a067d7c48dc5df60be0750162782f6ca9e2790e1`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:dae7e1a430d410690e1ac8f97bb7ba4a9970db59b5bad071334209e728508e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fef12049e311755a88f6ed54bc48d4c1b8bf6bb0d141affdec32b274fee2fcd`

```dockerfile
```

-	Layers:
	-	`sha256:e82d1cdacd927eb5664586024dae2a1cb667e1b8faed9e64bbfb6354fea7fc01`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:a06a9ae40437d600bc69403c9867d7c78bbd0261e1e8de585a9a1be038fc7e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130024916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef257cfb222c87f5b6aeb6bf1da8067196ecf6d7446a83c6120c78ccb0b4330`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a803a8a5b5db41392839b8d9e4b5dc98eb15e937e9a49ed46e2497676808283e`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 6.4 MB (6366128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53db656a9deda748d0137317b33e819676026a06a90003335d8129fd531e85`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 86.3 KB (86334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d755394c5b842899dd04ebc742660ce41ab0a2a14f38cf4d10e864b6dcffd5`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc2aa2417919467e58c0171cedbbd58423ec11584c3ed3285031ca790932146`  
		Last Modified: Tue, 04 Mar 2025 01:03:16 GMT  
		Size: 55.6 MB (55593637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eddd72049041d2e5083e7a7838eb4c6952dec7e4c186fe19c57d133194b086`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b244427612290e4f97cc15fb8e4f04d3b60140bf1ef1a77f18381bcdd2c51`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:e63515a65dee56b94046151fdf91185c60bc937a4dcaaf24d898bc9f3a057cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4367ec966899922086d3466b68fade429c2841e0551179512fb2308774c3345`

```dockerfile
```

-	Layers:
	-	`sha256:649fb81baea829805bdd59d93b87a3c335ef4fc45d773b95dcc4fa47fa616e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:13 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90ca9797ce316bce5ff74d335c304e85d41d6bd981f755a3281858072bfc839a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132411588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0250bf64dd26b5fe7a1a358ac561aa69a69de05ac454d6de509ef789813a11`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:f5b23b2ecb5219b4fd968f4f0e77e03bd1739c249efd6cd9743ff73138a96a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e084d1513f7ecd8f052a99a580b237130bd85603d5bacaacf72d2e9508170e20`

```dockerfile
```

-	Layers:
	-	`sha256:36cdd24344a437d2b167b4b38ada68f9f95a41ad871c683e3146b271a927edca`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-cli`

```console
$ docker pull docker@sha256:79bf825c5bed0d579820cc19f6857738abc424a680b619171591e969114f2015
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

### `docker:28.0.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:407b05f8635f0c78530a074e5ac3d7ca547e494f41d0b8279eb378c957d59eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73996743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7ace64e87a3531934d9d783dd55b09fba672037fb47361e760477742f81dbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e83e577007c54ec761b3cc9df69167cff393d56c84b9982c5aeaff3dc875c360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb394d129acd56043f7f5fb7f10a740ff52c5b301d50e34652f30fc3f4968535`

```dockerfile
```

-	Layers:
	-	`sha256:4e8c6e0b6ddceec47cfd0a4b2d23a912d8a9825b3412c2492d4162b91835a3ee`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:eeb4ad44bd101ca297d84a0a0c3d0a65e9c0b45a038e0311f029cf84ea075f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68966316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9dc49b493ad218febee37e481279ef5472fa3bb9a9c005a77ea867233c0fda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc9b040b7560289fbd5081459c6b6ddecaaf4363ef2436ae6c2b925e0382e3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d631428cc9605f46e62098c617996c4c90c97ed9efb14436c836857db508b29`

```dockerfile
```

-	Layers:
	-	`sha256:1fcd6fd391dd1a77f96dadcb8f3583ac995b301d90af68b3d9e3b9937c3213d9`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:da6f62e7a4822d683c95524b9c38b7e39d43633a4d518865fc88807116650172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67972911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1523a85a50b40de6aa255336254486bbf1dc534c39a0f2dcb7a5f69afffde5d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1c453d9c45321fd866c5830abe9036744fd50ea31aef24f0fd5b441f600d0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310b7edd1a05f5a6b1de9c12d0a3fd30be28798ce7d656f5b306158eb590c45c`

```dockerfile
```

-	Layers:
	-	`sha256:da87a8f3030a2c4d7a3e171d90c90259cecb58ab16f1f9570b999f97d340a6c6`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0e8384ace3dbca30fdface67dd29a8510a7285efdd842c51949e027ec0276891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69760973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a211b50f388cffbcec654f2c7e6951b74377f9657875d06fad2bc3915cad32c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:89c7bb5547d975cc3d11e0ae1a8ccc0351bf5fbc5335d2f5ddd2f35f6660c361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34de87369c83245725f8ef817f4b9e791ffcc508b41d1739e66e78f37aa131d9`

```dockerfile
```

-	Layers:
	-	`sha256:c32e99100ba19083df91a0159b4677528fb0e7aa00801be5cf350ba9ffa4b16e`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-cli-alpine3.21`

```console
$ docker pull docker@sha256:79bf825c5bed0d579820cc19f6857738abc424a680b619171591e969114f2015
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

### `docker:28.0.1-cli-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:407b05f8635f0c78530a074e5ac3d7ca547e494f41d0b8279eb378c957d59eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73996743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7ace64e87a3531934d9d783dd55b09fba672037fb47361e760477742f81dbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:e83e577007c54ec761b3cc9df69167cff393d56c84b9982c5aeaff3dc875c360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb394d129acd56043f7f5fb7f10a740ff52c5b301d50e34652f30fc3f4968535`

```dockerfile
```

-	Layers:
	-	`sha256:4e8c6e0b6ddceec47cfd0a4b2d23a912d8a9825b3412c2492d4162b91835a3ee`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:eeb4ad44bd101ca297d84a0a0c3d0a65e9c0b45a038e0311f029cf84ea075f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68966316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9dc49b493ad218febee37e481279ef5472fa3bb9a9c005a77ea867233c0fda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:dc9b040b7560289fbd5081459c6b6ddecaaf4363ef2436ae6c2b925e0382e3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d631428cc9605f46e62098c617996c4c90c97ed9efb14436c836857db508b29`

```dockerfile
```

-	Layers:
	-	`sha256:1fcd6fd391dd1a77f96dadcb8f3583ac995b301d90af68b3d9e3b9937c3213d9`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-cli-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:da6f62e7a4822d683c95524b9c38b7e39d43633a4d518865fc88807116650172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67972911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1523a85a50b40de6aa255336254486bbf1dc534c39a0f2dcb7a5f69afffde5d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:1c453d9c45321fd866c5830abe9036744fd50ea31aef24f0fd5b441f600d0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310b7edd1a05f5a6b1de9c12d0a3fd30be28798ce7d656f5b306158eb590c45c`

```dockerfile
```

-	Layers:
	-	`sha256:da87a8f3030a2c4d7a3e171d90c90259cecb58ab16f1f9570b999f97d340a6c6`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0e8384ace3dbca30fdface67dd29a8510a7285efdd842c51949e027ec0276891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69760973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a211b50f388cffbcec654f2c7e6951b74377f9657875d06fad2bc3915cad32c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:89c7bb5547d975cc3d11e0ae1a8ccc0351bf5fbc5335d2f5ddd2f35f6660c361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34de87369c83245725f8ef817f4b9e791ffcc508b41d1739e66e78f37aa131d9`

```dockerfile
```

-	Layers:
	-	`sha256:c32e99100ba19083df91a0159b4677528fb0e7aa00801be5cf350ba9ffa4b16e`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-dind`

```console
$ docker pull docker@sha256:9a651b22672c7151b5d8ca820ed2290b3fe4d4922e9b3f37ab14c8876da6613d
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

### `docker:28.0.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:63af38ad28e39198d32b84f6f0766b84f129223962a2b9d0d08895f82b8c974a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141018836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca75ab1d7a7464eafbb043969362b3580b89fc13d0a24015f05784cf1fbf4a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9f4cacdb6d1c7d18007496fd3fdc3e1a7db761aa9120a04950e745674e852fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d352174790d7d189910e7f5c3030976778ee363ffe05d6c5f85ddf5208ef9bb`

```dockerfile
```

-	Layers:
	-	`sha256:8c7368c1f564a9560c431962f192d16acdb099321d336f23a570f3eadb276e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1781a83e4d8da5abccfbc908e5a59f38842fb75fa3c92a6439f39b5ea582734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131692655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f764f0067ba36f35452a088c243700ee0a13f44b0d8398f4f41320126a60100`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52b5b50da000f825732faa0b306b0b03aba942958f60b4e4a267f64f2609725`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 7.0 MB (7036882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220971bcf994b5c3a2e140bbf3bf38830ebb2d208da3e028d0b4632a69131af`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 89.9 KB (89870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31279910422b314845644d11076adf1d5a5bf46d1bb9f5f946994d70718ba0c2`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972dc8fbd8a452f36a21a28edc3dca31c4f0cb12877b3cf4c19444a24c319082`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7f9370d4ba1a6b159b96643477be5fcd0428ad716dca0cd4ad4548d815dd5`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcbea16a18e4ce2926adfe5a067d7c48dc5df60be0750162782f6ca9e2790e1`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:dae7e1a430d410690e1ac8f97bb7ba4a9970db59b5bad071334209e728508e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fef12049e311755a88f6ed54bc48d4c1b8bf6bb0d141affdec32b274fee2fcd`

```dockerfile
```

-	Layers:
	-	`sha256:e82d1cdacd927eb5664586024dae2a1cb667e1b8faed9e64bbfb6354fea7fc01`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a06a9ae40437d600bc69403c9867d7c78bbd0261e1e8de585a9a1be038fc7e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130024916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef257cfb222c87f5b6aeb6bf1da8067196ecf6d7446a83c6120c78ccb0b4330`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a803a8a5b5db41392839b8d9e4b5dc98eb15e937e9a49ed46e2497676808283e`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 6.4 MB (6366128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53db656a9deda748d0137317b33e819676026a06a90003335d8129fd531e85`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 86.3 KB (86334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d755394c5b842899dd04ebc742660ce41ab0a2a14f38cf4d10e864b6dcffd5`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc2aa2417919467e58c0171cedbbd58423ec11584c3ed3285031ca790932146`  
		Last Modified: Tue, 04 Mar 2025 01:03:16 GMT  
		Size: 55.6 MB (55593637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eddd72049041d2e5083e7a7838eb4c6952dec7e4c186fe19c57d133194b086`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b244427612290e4f97cc15fb8e4f04d3b60140bf1ef1a77f18381bcdd2c51`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e63515a65dee56b94046151fdf91185c60bc937a4dcaaf24d898bc9f3a057cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4367ec966899922086d3466b68fade429c2841e0551179512fb2308774c3345`

```dockerfile
```

-	Layers:
	-	`sha256:649fb81baea829805bdd59d93b87a3c335ef4fc45d773b95dcc4fa47fa616e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:13 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90ca9797ce316bce5ff74d335c304e85d41d6bd981f755a3281858072bfc839a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132411588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0250bf64dd26b5fe7a1a358ac561aa69a69de05ac454d6de509ef789813a11`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f5b23b2ecb5219b4fd968f4f0e77e03bd1739c249efd6cd9743ff73138a96a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e084d1513f7ecd8f052a99a580b237130bd85603d5bacaacf72d2e9508170e20`

```dockerfile
```

-	Layers:
	-	`sha256:36cdd24344a437d2b167b4b38ada68f9f95a41ad871c683e3146b271a927edca`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-dind-alpine3.21`

```console
$ docker pull docker@sha256:9a651b22672c7151b5d8ca820ed2290b3fe4d4922e9b3f37ab14c8876da6613d
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

### `docker:28.0.1-dind-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:63af38ad28e39198d32b84f6f0766b84f129223962a2b9d0d08895f82b8c974a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141018836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca75ab1d7a7464eafbb043969362b3580b89fc13d0a24015f05784cf1fbf4a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:9f4cacdb6d1c7d18007496fd3fdc3e1a7db761aa9120a04950e745674e852fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d352174790d7d189910e7f5c3030976778ee363ffe05d6c5f85ddf5208ef9bb`

```dockerfile
```

-	Layers:
	-	`sha256:8c7368c1f564a9560c431962f192d16acdb099321d336f23a570f3eadb276e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1781a83e4d8da5abccfbc908e5a59f38842fb75fa3c92a6439f39b5ea582734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131692655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f764f0067ba36f35452a088c243700ee0a13f44b0d8398f4f41320126a60100`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52b5b50da000f825732faa0b306b0b03aba942958f60b4e4a267f64f2609725`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 7.0 MB (7036882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220971bcf994b5c3a2e140bbf3bf38830ebb2d208da3e028d0b4632a69131af`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 89.9 KB (89870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31279910422b314845644d11076adf1d5a5bf46d1bb9f5f946994d70718ba0c2`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972dc8fbd8a452f36a21a28edc3dca31c4f0cb12877b3cf4c19444a24c319082`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7f9370d4ba1a6b159b96643477be5fcd0428ad716dca0cd4ad4548d815dd5`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcbea16a18e4ce2926adfe5a067d7c48dc5df60be0750162782f6ca9e2790e1`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:dae7e1a430d410690e1ac8f97bb7ba4a9970db59b5bad071334209e728508e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fef12049e311755a88f6ed54bc48d4c1b8bf6bb0d141affdec32b274fee2fcd`

```dockerfile
```

-	Layers:
	-	`sha256:e82d1cdacd927eb5664586024dae2a1cb667e1b8faed9e64bbfb6354fea7fc01`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:a06a9ae40437d600bc69403c9867d7c78bbd0261e1e8de585a9a1be038fc7e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130024916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef257cfb222c87f5b6aeb6bf1da8067196ecf6d7446a83c6120c78ccb0b4330`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a803a8a5b5db41392839b8d9e4b5dc98eb15e937e9a49ed46e2497676808283e`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 6.4 MB (6366128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53db656a9deda748d0137317b33e819676026a06a90003335d8129fd531e85`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 86.3 KB (86334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d755394c5b842899dd04ebc742660ce41ab0a2a14f38cf4d10e864b6dcffd5`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc2aa2417919467e58c0171cedbbd58423ec11584c3ed3285031ca790932146`  
		Last Modified: Tue, 04 Mar 2025 01:03:16 GMT  
		Size: 55.6 MB (55593637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eddd72049041d2e5083e7a7838eb4c6952dec7e4c186fe19c57d133194b086`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b244427612290e4f97cc15fb8e4f04d3b60140bf1ef1a77f18381bcdd2c51`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:e63515a65dee56b94046151fdf91185c60bc937a4dcaaf24d898bc9f3a057cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4367ec966899922086d3466b68fade429c2841e0551179512fb2308774c3345`

```dockerfile
```

-	Layers:
	-	`sha256:649fb81baea829805bdd59d93b87a3c335ef4fc45d773b95dcc4fa47fa616e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:13 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90ca9797ce316bce5ff74d335c304e85d41d6bd981f755a3281858072bfc839a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132411588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0250bf64dd26b5fe7a1a358ac561aa69a69de05ac454d6de509ef789813a11`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:f5b23b2ecb5219b4fd968f4f0e77e03bd1739c249efd6cd9743ff73138a96a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e084d1513f7ecd8f052a99a580b237130bd85603d5bacaacf72d2e9508170e20`

```dockerfile
```

-	Layers:
	-	`sha256:36cdd24344a437d2b167b4b38ada68f9f95a41ad871c683e3146b271a927edca`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-dind-rootless`

```console
$ docker pull docker@sha256:77dfe1ec10cdf5406214798bb37d7eae17b98d0dd1a8ce0cbd181e1e66ae8e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.0.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e61ae57240222f863c8a5b06b7cef58e30f0f0d0e151df70bd8b93dcb0add483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159173162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e4181b6a4dbfad3eda6a6cfe192fc9e5395c2b2e3dc7163b8049d8c8d3dae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cffb75e9d3a5007728e392783b97dc4c1457b0c9b5ed0d01c4b6f24414a8a3`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 986.6 KB (986572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2da6fe36e77ab8ccbc591eece09e51d53e8326f48eccb90161590497da92fb`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef728516ba2da965a49726affb6690ca64cca2c079d6990785b9717c4021ee30`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aa9b83388cba05ccc2d8cec1a786a6af3222350840d116b26e5f155e3eb05f`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 17.2 MB (17166413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde177038eb92e35753d04334ab44c59f7fd917a34d85872b666ccffafe69c44`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bbc21e77f41b8b6a40705c9e78a508d27da1c6c2b5cca32ef25f5d8aec78c1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95431ca3e37228cd8c5620454fe5e37fad72d2fe0452d170a71e3811d23fd298`

```dockerfile
```

-	Layers:
	-	`sha256:96d16732d86f704c5501d23bf1c915f1e338bbf89438ad4af2428a2ac063bed5`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8b7764fc03fe18004cf4f8645ed5a8cd81676ea1dafa744c15ead08f05118297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152706572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030ba4eec29973e85084b2475b96b3d968861321f544745a7690475756dd854c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2355ca5978c694d96707e17104bfa53213bbc301d053c1ad18d5848d62d7b95`  
		Last Modified: Tue, 04 Mar 2025 01:07:52 GMT  
		Size: 1.0 MB (1014205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7810dcc87146cd8f8d35999ec2eab9c9b96ec8db7cc0573bf600a6c9b6253f0f`  
		Last Modified: Tue, 04 Mar 2025 01:07:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fc3d18d4751d666afc8c89917cd8a0df97cc28f2e94d2b8554ac8e0e3fc35a`  
		Last Modified: Tue, 04 Mar 2025 01:07:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7088145dc16c08b39c911d6b5b95d35e16b264c54f9759eddefab033383fdb75`  
		Last Modified: Tue, 04 Mar 2025 01:07:52 GMT  
		Size: 19.3 MB (19279437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7163ac37a0e799a8e7e67df4c7e47106af035adff56fd17076dc8c001eb7b1d6`  
		Last Modified: Tue, 04 Mar 2025 01:07:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9231ac8f93e5816c1ba8a4867dbd89036e466b3eaa1729b2a20a1f59e97be229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfe83ec9fbf61240855ccdd060605d1fd5587cbca14cce35b775d471b52d89d`

```dockerfile
```

-	Layers:
	-	`sha256:228c43eddb59977bb2f12d9a6aef4d2fb06fa90ecb174f42e8ca898d410159a0`  
		Last Modified: Tue, 04 Mar 2025 01:07:51 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.1-windowsservercore`

```console
$ docker pull docker@sha256:888ccff3b9636b55646e6bb5477e92d060a93a2c17c21e6e1bddb8907b3667ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:28.0.1-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:c1f4df2f1e5249ae9c2805fbaa593bc9c8e76a8ed12a0436996d04e8b7cc038d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2973507774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f730146db9c7982e4e32e090d898ce8bb0203dcff5a072ab1825c8984f3af`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:47:14 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:47:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:47:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:47:26 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:47:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:47:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:47:36 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:47:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5db60003403b188f7c1530d269d228ed8fcb842beb2ef4ac0e0ffe3c87d610`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686d03d51200d5ae151d48672f750801918d278241e440704a22667d7d98b197`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 364.4 KB (364432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a92737683cf4c298dc0edec0672a162c28f51a4be547f12aa894d1bc1b9203`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98fe940464aaad024d9e1802e57ed753c43c1a3da5b7adcc82b0ab16cb0a5bd`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f6146091546c80b9879daf08ba51e90ae07e7ca2a0449b6e62db8ee4355ad2`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 19.8 MB (19832344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2a3f2b03cc567ce88efb88d37ec49e5878d1c065f3d3289b759b6f303d468b`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1efa5ff8dccab563d2fb407dba261e83538e10d8f6a52d55795eca8799e07`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a1f9cfcf1a770b8e0563e10af4fe4fd665d94dbf6202cbb5d6e70d77c47ca`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0ea793b63325756fa010233c0bcec2d5e2540ebd010c854b4871488e591249`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 22.8 MB (22757621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f5b3ea67a8a43b5157e213977222af56ae70e4f8e81817bc714e75892ea9fb`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f89fa36da2f4d182f429d1e909346499105d84b6de15f3c59f203ef327771e4`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4eaef42c69737e26a4f51b2ff86be0f80f023f1cf243c7f24b56c9f07c9125`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb16e071c42270350ca5102ef4475935e3249a11df250a83a637f0c4896a944`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 21.9 MB (21894006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0.1-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:d857e60eee8f4ee9d71ea880c7faa05fbbf3965f724666008415847844f86520
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334710456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a256501bc1307f791a4185e872770e8b44e05680661816f7974a375494abe2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:53:55 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:53:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:54:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:06 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:54:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:54:08 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:54:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:54:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd0a29ac12f7f5357cfca6a7cb15badd5a2fc342a81bb77ac97698701afecd0`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016be76acd15c6840b1f3c249ab0e88aca806595f849ae4defae54014d672ed3`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 343.3 KB (343272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bba7d1b615e4aa5cf86abd0f490b746e40b90733a7ed5a7b931cc208008a0a`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a757b9a15d3fa1af7bb47a9620e1db135dc5b478b45df78506291e56a9dbcd2d`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608b6e007c175f8ae40b4011323b27a3bb45ab575d0d1ba663d62e371379c2aa`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 19.8 MB (19805728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9396c1d3ca9fd43dded5884b992f48110a5592d944cae25ac9f2739299f2b3e`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a093896c4308e2f82773042ec2d94e515963b7f483a79df82035d6b4e16e0`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2fa19931d46d88400ccbe12850373ec33422e71386cf418f0f31564f379c78`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819822354481476168a3af548619cbceceeae4c2a19a1ab2d2c49613b23d832`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 22.7 MB (22731872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923ebe1421f0c6d0754bd55e14ced92f03a796d4def86fb78edd3e143b9eb5e2`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b222136c7f0e28a6668c3f86bf7c5c39b749998b118cfe6535a5cd194057d40`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97d245b4a24d519ab255dfc31ebb0ed031408cb5df38803fedd776a39828f2b`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f118966c417c3afe3fc57523f23c754d770dd204bf1a7e23ff05c5ccb714b3e5`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 21.9 MB (21876802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0.1-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:6ec89c50d8a2e7140122be3cc885817ef06db86ff79ab4959f230e563b152edb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216356810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb90c5ec050a045c16a9fcaf25f380389e43ed95b32e89c6754c3d5388ad1a2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:52:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:52:50 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:53:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:53:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:53:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aad9a715a375d2c8dbcf38b891c606580b3c469223f6a06ad300be69b95982`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f35846ff4f094309b4cb17bd9244228a41c1b24f785015035b360c10421eac`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 327.5 KB (327491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753e2664deb2e592c9acd1b487b8e2c541be824f4ab302d395d4a2a61e85ed1`  
		Last Modified: Wed, 12 Mar 2025 18:53:21 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf83ab28dea983722f41794eb1be6949042863a4e4d163096fe8a27f671bcab`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6102740590b962968e8e065bc558a49a14d55e5e20198483d48542470b76e62f`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 19.8 MB (19799094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4693030fb7a286223c350e8b41f2276f8edfec6f292227335cf7fd2dc838111d`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c35ff7e4e472d5368f2f8f84b0986949edd9cd33469def72a632a526cf8bb7`  
		Last Modified: Wed, 12 Mar 2025 18:53:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b5d10cb3dbeb63171a22ffa84f71ea66f067bc4f93b935cfc8e4e88d985f43`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88fed0b769948546d05ad2d707d73d67046f51ae307c46737ace9ce1a3ec1b9`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 22.7 MB (22723657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc8cce8f76304d63d169b17d38a8634765c802bd0c32240d8df737ab81d325`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fed1f356a2be26f78799e2e2a795459a1cb01fee11bbc19d73be193980e8b6`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450b3ffc1b8b10ce5152ee50cb2cf841409eeab832e78cda33e44710d8d9c1f3`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d330fcb490da82d9eb119a9deebdac8dd6a40333e12f3f49b0500bc871119ae1`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 21.9 MB (21860255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:061a40406076ff8843375da449424a3c19052bb114078bab3189d8cb3d4cc72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:28.0.1-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:6ec89c50d8a2e7140122be3cc885817ef06db86ff79ab4959f230e563b152edb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216356810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb90c5ec050a045c16a9fcaf25f380389e43ed95b32e89c6754c3d5388ad1a2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:52:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:52:50 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:53:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:53:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:53:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aad9a715a375d2c8dbcf38b891c606580b3c469223f6a06ad300be69b95982`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f35846ff4f094309b4cb17bd9244228a41c1b24f785015035b360c10421eac`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 327.5 KB (327491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753e2664deb2e592c9acd1b487b8e2c541be824f4ab302d395d4a2a61e85ed1`  
		Last Modified: Wed, 12 Mar 2025 18:53:21 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf83ab28dea983722f41794eb1be6949042863a4e4d163096fe8a27f671bcab`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6102740590b962968e8e065bc558a49a14d55e5e20198483d48542470b76e62f`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 19.8 MB (19799094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4693030fb7a286223c350e8b41f2276f8edfec6f292227335cf7fd2dc838111d`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c35ff7e4e472d5368f2f8f84b0986949edd9cd33469def72a632a526cf8bb7`  
		Last Modified: Wed, 12 Mar 2025 18:53:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b5d10cb3dbeb63171a22ffa84f71ea66f067bc4f93b935cfc8e4e88d985f43`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88fed0b769948546d05ad2d707d73d67046f51ae307c46737ace9ce1a3ec1b9`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 22.7 MB (22723657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc8cce8f76304d63d169b17d38a8634765c802bd0c32240d8df737ab81d325`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fed1f356a2be26f78799e2e2a795459a1cb01fee11bbc19d73be193980e8b6`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450b3ffc1b8b10ce5152ee50cb2cf841409eeab832e78cda33e44710d8d9c1f3`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d330fcb490da82d9eb119a9deebdac8dd6a40333e12f3f49b0500bc871119ae1`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 21.9 MB (21860255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fa4d958eb2453fec999de01713c508b53a971fbbed9f3bcda63fbe7a275ec92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:28.0.1-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:d857e60eee8f4ee9d71ea880c7faa05fbbf3965f724666008415847844f86520
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334710456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a256501bc1307f791a4185e872770e8b44e05680661816f7974a375494abe2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:53:55 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:53:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:54:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:06 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:54:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:54:08 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:54:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:54:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd0a29ac12f7f5357cfca6a7cb15badd5a2fc342a81bb77ac97698701afecd0`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016be76acd15c6840b1f3c249ab0e88aca806595f849ae4defae54014d672ed3`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 343.3 KB (343272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bba7d1b615e4aa5cf86abd0f490b746e40b90733a7ed5a7b931cc208008a0a`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a757b9a15d3fa1af7bb47a9620e1db135dc5b478b45df78506291e56a9dbcd2d`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608b6e007c175f8ae40b4011323b27a3bb45ab575d0d1ba663d62e371379c2aa`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 19.8 MB (19805728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9396c1d3ca9fd43dded5884b992f48110a5592d944cae25ac9f2739299f2b3e`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a093896c4308e2f82773042ec2d94e515963b7f483a79df82035d6b4e16e0`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2fa19931d46d88400ccbe12850373ec33422e71386cf418f0f31564f379c78`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819822354481476168a3af548619cbceceeae4c2a19a1ab2d2c49613b23d832`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 22.7 MB (22731872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923ebe1421f0c6d0754bd55e14ced92f03a796d4def86fb78edd3e143b9eb5e2`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b222136c7f0e28a6668c3f86bf7c5c39b749998b118cfe6535a5cd194057d40`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97d245b4a24d519ab255dfc31ebb0ed031408cb5df38803fedd776a39828f2b`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f118966c417c3afe3fc57523f23c754d770dd204bf1a7e23ff05c5ccb714b3e5`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 21.9 MB (21876802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:c1ee7176bc33fb9f8af5afecd2334b44191b9c56c7a64103d001ad7c5984aa31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:28.0.1-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:c1f4df2f1e5249ae9c2805fbaa593bc9c8e76a8ed12a0436996d04e8b7cc038d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2973507774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f730146db9c7982e4e32e090d898ce8bb0203dcff5a072ab1825c8984f3af`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:47:14 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:47:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:47:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:47:26 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:47:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:47:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:47:36 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:47:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5db60003403b188f7c1530d269d228ed8fcb842beb2ef4ac0e0ffe3c87d610`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686d03d51200d5ae151d48672f750801918d278241e440704a22667d7d98b197`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 364.4 KB (364432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a92737683cf4c298dc0edec0672a162c28f51a4be547f12aa894d1bc1b9203`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98fe940464aaad024d9e1802e57ed753c43c1a3da5b7adcc82b0ab16cb0a5bd`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f6146091546c80b9879daf08ba51e90ae07e7ca2a0449b6e62db8ee4355ad2`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 19.8 MB (19832344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2a3f2b03cc567ce88efb88d37ec49e5878d1c065f3d3289b759b6f303d468b`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1efa5ff8dccab563d2fb407dba261e83538e10d8f6a52d55795eca8799e07`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a1f9cfcf1a770b8e0563e10af4fe4fd665d94dbf6202cbb5d6e70d77c47ca`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0ea793b63325756fa010233c0bcec2d5e2540ebd010c854b4871488e591249`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 22.8 MB (22757621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f5b3ea67a8a43b5157e213977222af56ae70e4f8e81817bc714e75892ea9fb`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f89fa36da2f4d182f429d1e909346499105d84b6de15f3c59f203ef327771e4`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4eaef42c69737e26a4f51b2ff86be0f80f023f1cf243c7f24b56c9f07c9125`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb16e071c42270350ca5102ef4475935e3249a11df250a83a637f0c4896a944`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 21.9 MB (21894006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:79bf825c5bed0d579820cc19f6857738abc424a680b619171591e969114f2015
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
$ docker pull docker@sha256:407b05f8635f0c78530a074e5ac3d7ca547e494f41d0b8279eb378c957d59eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73996743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7ace64e87a3531934d9d783dd55b09fba672037fb47361e760477742f81dbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:e83e577007c54ec761b3cc9df69167cff393d56c84b9982c5aeaff3dc875c360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb394d129acd56043f7f5fb7f10a740ff52c5b301d50e34652f30fc3f4968535`

```dockerfile
```

-	Layers:
	-	`sha256:4e8c6e0b6ddceec47cfd0a4b2d23a912d8a9825b3412c2492d4162b91835a3ee`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:eeb4ad44bd101ca297d84a0a0c3d0a65e9c0b45a038e0311f029cf84ea075f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68966316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9dc49b493ad218febee37e481279ef5472fa3bb9a9c005a77ea867233c0fda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:dc9b040b7560289fbd5081459c6b6ddecaaf4363ef2436ae6c2b925e0382e3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d631428cc9605f46e62098c617996c4c90c97ed9efb14436c836857db508b29`

```dockerfile
```

-	Layers:
	-	`sha256:1fcd6fd391dd1a77f96dadcb8f3583ac995b301d90af68b3d9e3b9937c3213d9`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:da6f62e7a4822d683c95524b9c38b7e39d43633a4d518865fc88807116650172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67972911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1523a85a50b40de6aa255336254486bbf1dc534c39a0f2dcb7a5f69afffde5d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:1c453d9c45321fd866c5830abe9036744fd50ea31aef24f0fd5b441f600d0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310b7edd1a05f5a6b1de9c12d0a3fd30be28798ce7d656f5b306158eb590c45c`

```dockerfile
```

-	Layers:
	-	`sha256:da87a8f3030a2c4d7a3e171d90c90259cecb58ab16f1f9570b999f97d340a6c6`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:0e8384ace3dbca30fdface67dd29a8510a7285efdd842c51949e027ec0276891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69760973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a211b50f388cffbcec654f2c7e6951b74377f9657875d06fad2bc3915cad32c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_VERSION=28.0.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Mon, 03 Mar 2025 18:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 03 Mar 2025 18:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 03 Mar 2025 18:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:89c7bb5547d975cc3d11e0ae1a8ccc0351bf5fbc5335d2f5ddd2f35f6660c361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34de87369c83245725f8ef817f4b9e791ffcc508b41d1739e66e78f37aa131d9`

```dockerfile
```

-	Layers:
	-	`sha256:c32e99100ba19083df91a0159b4677528fb0e7aa00801be5cf350ba9ffa4b16e`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:9a651b22672c7151b5d8ca820ed2290b3fe4d4922e9b3f37ab14c8876da6613d
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
$ docker pull docker@sha256:63af38ad28e39198d32b84f6f0766b84f129223962a2b9d0d08895f82b8c974a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141018836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca75ab1d7a7464eafbb043969362b3580b89fc13d0a24015f05784cf1fbf4a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:9f4cacdb6d1c7d18007496fd3fdc3e1a7db761aa9120a04950e745674e852fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d352174790d7d189910e7f5c3030976778ee363ffe05d6c5f85ddf5208ef9bb`

```dockerfile
```

-	Layers:
	-	`sha256:8c7368c1f564a9560c431962f192d16acdb099321d336f23a570f3eadb276e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1781a83e4d8da5abccfbc908e5a59f38842fb75fa3c92a6439f39b5ea582734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131692655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f764f0067ba36f35452a088c243700ee0a13f44b0d8398f4f41320126a60100`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52b5b50da000f825732faa0b306b0b03aba942958f60b4e4a267f64f2609725`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 7.0 MB (7036882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220971bcf994b5c3a2e140bbf3bf38830ebb2d208da3e028d0b4632a69131af`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 89.9 KB (89870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31279910422b314845644d11076adf1d5a5bf46d1bb9f5f946994d70718ba0c2`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972dc8fbd8a452f36a21a28edc3dca31c4f0cb12877b3cf4c19444a24c319082`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7f9370d4ba1a6b159b96643477be5fcd0428ad716dca0cd4ad4548d815dd5`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcbea16a18e4ce2926adfe5a067d7c48dc5df60be0750162782f6ca9e2790e1`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:dae7e1a430d410690e1ac8f97bb7ba4a9970db59b5bad071334209e728508e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fef12049e311755a88f6ed54bc48d4c1b8bf6bb0d141affdec32b274fee2fcd`

```dockerfile
```

-	Layers:
	-	`sha256:e82d1cdacd927eb5664586024dae2a1cb667e1b8faed9e64bbfb6354fea7fc01`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a06a9ae40437d600bc69403c9867d7c78bbd0261e1e8de585a9a1be038fc7e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130024916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef257cfb222c87f5b6aeb6bf1da8067196ecf6d7446a83c6120c78ccb0b4330`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a803a8a5b5db41392839b8d9e4b5dc98eb15e937e9a49ed46e2497676808283e`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 6.4 MB (6366128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53db656a9deda748d0137317b33e819676026a06a90003335d8129fd531e85`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 86.3 KB (86334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d755394c5b842899dd04ebc742660ce41ab0a2a14f38cf4d10e864b6dcffd5`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc2aa2417919467e58c0171cedbbd58423ec11584c3ed3285031ca790932146`  
		Last Modified: Tue, 04 Mar 2025 01:03:16 GMT  
		Size: 55.6 MB (55593637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eddd72049041d2e5083e7a7838eb4c6952dec7e4c186fe19c57d133194b086`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b244427612290e4f97cc15fb8e4f04d3b60140bf1ef1a77f18381bcdd2c51`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:e63515a65dee56b94046151fdf91185c60bc937a4dcaaf24d898bc9f3a057cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4367ec966899922086d3466b68fade429c2841e0551179512fb2308774c3345`

```dockerfile
```

-	Layers:
	-	`sha256:649fb81baea829805bdd59d93b87a3c335ef4fc45d773b95dcc4fa47fa616e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:13 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90ca9797ce316bce5ff74d335c304e85d41d6bd981f755a3281858072bfc839a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132411588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0250bf64dd26b5fe7a1a358ac561aa69a69de05ac454d6de509ef789813a11`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:f5b23b2ecb5219b4fd968f4f0e77e03bd1739c249efd6cd9743ff73138a96a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e084d1513f7ecd8f052a99a580b237130bd85603d5bacaacf72d2e9508170e20`

```dockerfile
```

-	Layers:
	-	`sha256:36cdd24344a437d2b167b4b38ada68f9f95a41ad871c683e3146b271a927edca`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:77dfe1ec10cdf5406214798bb37d7eae17b98d0dd1a8ce0cbd181e1e66ae8e2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e61ae57240222f863c8a5b06b7cef58e30f0f0d0e151df70bd8b93dcb0add483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159173162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e4181b6a4dbfad3eda6a6cfe192fc9e5395c2b2e3dc7163b8049d8c8d3dae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cffb75e9d3a5007728e392783b97dc4c1457b0c9b5ed0d01c4b6f24414a8a3`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 986.6 KB (986572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2da6fe36e77ab8ccbc591eece09e51d53e8326f48eccb90161590497da92fb`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef728516ba2da965a49726affb6690ca64cca2c079d6990785b9717c4021ee30`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aa9b83388cba05ccc2d8cec1a786a6af3222350840d116b26e5f155e3eb05f`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 17.2 MB (17166413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde177038eb92e35753d04334ab44c59f7fd917a34d85872b666ccffafe69c44`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bbc21e77f41b8b6a40705c9e78a508d27da1c6c2b5cca32ef25f5d8aec78c1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95431ca3e37228cd8c5620454fe5e37fad72d2fe0452d170a71e3811d23fd298`

```dockerfile
```

-	Layers:
	-	`sha256:96d16732d86f704c5501d23bf1c915f1e338bbf89438ad4af2428a2ac063bed5`  
		Last Modified: Tue, 04 Mar 2025 01:08:31 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8b7764fc03fe18004cf4f8645ed5a8cd81676ea1dafa744c15ead08f05118297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152706572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030ba4eec29973e85084b2475b96b3d968861321f544745a7690475756dd854c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2355ca5978c694d96707e17104bfa53213bbc301d053c1ad18d5848d62d7b95`  
		Last Modified: Tue, 04 Mar 2025 01:07:52 GMT  
		Size: 1.0 MB (1014205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7810dcc87146cd8f8d35999ec2eab9c9b96ec8db7cc0573bf600a6c9b6253f0f`  
		Last Modified: Tue, 04 Mar 2025 01:07:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fc3d18d4751d666afc8c89917cd8a0df97cc28f2e94d2b8554ac8e0e3fc35a`  
		Last Modified: Tue, 04 Mar 2025 01:07:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7088145dc16c08b39c911d6b5b95d35e16b264c54f9759eddefab033383fdb75`  
		Last Modified: Tue, 04 Mar 2025 01:07:52 GMT  
		Size: 19.3 MB (19279437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7163ac37a0e799a8e7e67df4c7e47106af035adff56fd17076dc8c001eb7b1d6`  
		Last Modified: Tue, 04 Mar 2025 01:07:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9231ac8f93e5816c1ba8a4867dbd89036e466b3eaa1729b2a20a1f59e97be229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfe83ec9fbf61240855ccdd060605d1fd5587cbca14cce35b775d471b52d89d`

```dockerfile
```

-	Layers:
	-	`sha256:228c43eddb59977bb2f12d9a6aef4d2fb06fa90ecb174f42e8ca898d410159a0`  
		Last Modified: Tue, 04 Mar 2025 01:07:51 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:9a651b22672c7151b5d8ca820ed2290b3fe4d4922e9b3f37ab14c8876da6613d
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
$ docker pull docker@sha256:63af38ad28e39198d32b84f6f0766b84f129223962a2b9d0d08895f82b8c974a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141018836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca75ab1d7a7464eafbb043969362b3580b89fc13d0a24015f05784cf1fbf4a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3795da19ece39a2f3e799e489d3386b647d821a7e85ce5b46158fda8385c90ae`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661467c513c0068cd667d83c057ef762773b5ccf6aad8dca72be7b0e9e58e9e`  
		Last Modified: Tue, 04 Mar 2025 00:29:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec760ee5d6f28773e7cbf44a8a2b6b34fb4aa0d6fa6d0b614fc080d333c7676`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 19.5 MB (19500670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c635aaeace6c21c4023ef00aa52d94d6562588edaa3aad82866677d7cd6a5ff`  
		Last Modified: Tue, 04 Mar 2025 00:29:10 GMT  
		Size: 21.8 MB (21830052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d14474db62f6d4f2619294ffb73aa5732222ebff4ce811b4a7b46a392f84987`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998be54fa1411f0ee896dc23f34ff26d9187f809346db77c1a808fb03dbcb953`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fb44047f2a37f86a5f6b5e48070a7d913119ce8f1b209cb835655226264209`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0edd909f3e7692f076d353fc1fe5c12f1c94db3cde6d2c554c3c65f97cdba45`  
		Last Modified: Tue, 04 Mar 2025 00:29:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b3568325ca8bac8e3cb71d242fae67bc3366bace97cd62c04e6616ffbb793`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 6.7 MB (6733038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4123c72b3c4dbad7c6ce805c7e43be3ed6021d036da1aa20e114328e622f1`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 90.3 KB (90324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca80691327dc1b41c3dc3fd8587c1d7f4a686e35d9c9b8cf1f76f3e98034f31`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afd71a730c8fad779d95aab92b3b3a1ae12d10e5bd3b2b9e37448dc3c0fd7`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 60.2 MB (60192824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21a33964add14269b10f44dd466bc3c02ceda0b65e353edcb19eb33c863aea0`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dc3a0172b64618b6019d8c9dfd03bdd3bdf91bd80aebffaa5a92c8ae5bff3c`  
		Last Modified: Tue, 04 Mar 2025 01:03:30 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:9f4cacdb6d1c7d18007496fd3fdc3e1a7db761aa9120a04950e745674e852fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d352174790d7d189910e7f5c3030976778ee363ffe05d6c5f85ddf5208ef9bb`

```dockerfile
```

-	Layers:
	-	`sha256:8c7368c1f564a9560c431962f192d16acdb099321d336f23a570f3eadb276e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:29 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:b1781a83e4d8da5abccfbc908e5a59f38842fb75fa3c92a6439f39b5ea582734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131692655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f764f0067ba36f35452a088c243700ee0a13f44b0d8398f4f41320126a60100`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 19:31:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054bdf6269bf1d44f886e0a8b7f00e0d805ca085041c657f41660939ee574e36`  
		Last Modified: Thu, 27 Feb 2025 01:51:28 GMT  
		Size: 17.5 MB (17463024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f7bc764352ec86fba70db21ddeab29e555fe6bffb436bc5d212212d378f99`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 20.4 MB (20432360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978e71e4b0a8ba81baf022cb3a734d0d6b005a7a3babd6414b3300e4458c62e`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 19.7 MB (19725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de33aa6df2b53c82eae086878b3e34c1c6cb5d0259e4369bc57a422f4be523`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec5dd4325c3a0e62da84a7230a9f3d459d05ba0c2f3e9854f4319563e396e5`  
		Last Modified: Tue, 04 Mar 2025 00:46:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82378aeb3d1e2aab7b8f2c4cff9675ec966ea134e12518f7ce032edad9c5f4a4`  
		Last Modified: Tue, 04 Mar 2025 00:46:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52b5b50da000f825732faa0b306b0b03aba942958f60b4e4a267f64f2609725`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 7.0 MB (7036882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220971bcf994b5c3a2e140bbf3bf38830ebb2d208da3e028d0b4632a69131af`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 89.9 KB (89870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31279910422b314845644d11076adf1d5a5bf46d1bb9f5f946994d70718ba0c2`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972dc8fbd8a452f36a21a28edc3dca31c4f0cb12877b3cf4c19444a24c319082`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 55.6 MB (55593673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7f9370d4ba1a6b159b96643477be5fcd0428ad716dca0cd4ad4548d815dd5`  
		Last Modified: Tue, 04 Mar 2025 01:02:54 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcbea16a18e4ce2926adfe5a067d7c48dc5df60be0750162782f6ca9e2790e1`  
		Last Modified: Tue, 04 Mar 2025 01:02:55 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:dae7e1a430d410690e1ac8f97bb7ba4a9970db59b5bad071334209e728508e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fef12049e311755a88f6ed54bc48d4c1b8bf6bb0d141affdec32b274fee2fcd`

```dockerfile
```

-	Layers:
	-	`sha256:e82d1cdacd927eb5664586024dae2a1cb667e1b8faed9e64bbfb6354fea7fc01`  
		Last Modified: Tue, 04 Mar 2025 01:02:53 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:a06a9ae40437d600bc69403c9867d7c78bbd0261e1e8de585a9a1be038fc7e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130024916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef257cfb222c87f5b6aeb6bf1da8067196ecf6d7446a83c6120c78ccb0b4330`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117311ad7167b9553281abaa7235fd5f3832a7b012cfb6b899a8b4349598da64`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 7.3 MB (7299499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b971d99e53aeff617c5aaca904195a15aeb770e375b8cfc9a61a40c532f2c869`  
		Last Modified: Thu, 27 Feb 2025 01:59:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76c5d192a5373a5dfcf506e6f8e42c9a769bd40c46e970d7af316afbc14457`  
		Last Modified: Thu, 27 Feb 2025 01:59:09 GMT  
		Size: 17.5 MB (17453605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aad7a6acb154ca593060d3e37bab904fc643be425607a808faf28baf102e3e0`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.4 MB (20410959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cbe930c38e298b5d215172a43649b69d4ec822e6f2dd9c9653d3e10c6fef7c`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 19.7 MB (19708563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ab58dff7537f1f21940512a5873857c7bfcd83b70ea566c0d893b0ed4bbe`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c58f32e0a401949f3015339b40763f13997ec258f8de853a296c690175b9a`  
		Last Modified: Tue, 04 Mar 2025 00:29:14 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb034e3b9968792379e5445118d7e948eae0509b74bbe0222c32450ce369231`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a803a8a5b5db41392839b8d9e4b5dc98eb15e937e9a49ed46e2497676808283e`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 6.4 MB (6366128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53db656a9deda748d0137317b33e819676026a06a90003335d8129fd531e85`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 86.3 KB (86334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d755394c5b842899dd04ebc742660ce41ab0a2a14f38cf4d10e864b6dcffd5`  
		Last Modified: Tue, 04 Mar 2025 01:03:14 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc2aa2417919467e58c0171cedbbd58423ec11584c3ed3285031ca790932146`  
		Last Modified: Tue, 04 Mar 2025 01:03:16 GMT  
		Size: 55.6 MB (55593637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eddd72049041d2e5083e7a7838eb4c6952dec7e4c186fe19c57d133194b086`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b244427612290e4f97cc15fb8e4f04d3b60140bf1ef1a77f18381bcdd2c51`  
		Last Modified: Tue, 04 Mar 2025 01:03:15 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:e63515a65dee56b94046151fdf91185c60bc937a4dcaaf24d898bc9f3a057cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4367ec966899922086d3466b68fade429c2841e0551179512fb2308774c3345`

```dockerfile
```

-	Layers:
	-	`sha256:649fb81baea829805bdd59d93b87a3c335ef4fc45d773b95dcc4fa47fa616e9f`  
		Last Modified: Tue, 04 Mar 2025 01:03:13 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90ca9797ce316bce5ff74d335c304e85d41d6bd981f755a3281858072bfc839a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132411588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0250bf64dd26b5fe7a1a358ac561aa69a69de05ac454d6de509ef789813a11`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-amd64'; 			sha256='b13bee81c3db12a4be7d0b9d042b64d0dd9ed116f7674dfac0ffdf2a71acfe3d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v6'; 			sha256='70dabedf4afe192e23a00c0bfe6ecda000545059abfce339f72f45b41f4fbb45'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm-v7'; 			sha256='c41700549bbf783e861cfe0c918aa152ece87cac099a260995b3822e75e3838b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-arm64'; 			sha256='7e21e62eae3243e476411c9bbe93b8ee59b5d62ddf075c527d168174c3ab3a04'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-ppc64le'; 			sha256='c817caec1e697484e8375d0fda499407e9081c8952db62edf702ccbb5d93187c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-riscv64'; 			sha256='cdac31a493fc19fab46962bbbb4fdec6d14c1549c1b5cacafc7eb5d60fe11b75'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.linux-s390x'; 			sha256='bd89f667a10870a9ce11e60a1028a2fa0395c85f27ba0faaf8d338771fb65416'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea18fe8983a070ff98fee22ab68cce13085c17b7e1d4776186ee21ea222ce77`  
		Last Modified: Tue, 04 Mar 2025 00:29:15 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23743df8d7607184ec438fe30dd013559d60f919660eebe4bd660ed8e350b13b`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 18.4 MB (18425651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac4518474b4f98d179b77a62a8746dea8e914d4d1b842cec3ccc33aa8b3645`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 20.0 MB (20040963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98b8dcf58a1cc2d3f118da44231a0c4e91b204b619bde9d940f4f4e5e2f5a5`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 19.2 MB (19222746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470f5de438243b543c91d9fbe46db8e3bd07f5722df6c60d2a5c298b70a3525`  
		Last Modified: Tue, 04 Mar 2025 00:29:16 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add59061c75d32dc7d2b7368be73fa03e9671f7689c7eccfb1d35eca042b5c41`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479fdd35f53e0fa17829a8c73680b896b41d4127977f3dd41d93a3ede36b4a8`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568759e8d939bbe44de74230baa847873cfaa0e9781f259224ad48fb2a7a7ee6`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7439101607be9a4ce7ac4378751ae85876597de922b2617cc99d8873935769`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 99.4 KB (99385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7902d446205500a9534c8d1a8548f3bd5cf345ac5d37b6eea0b98eaa92495c5f`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40292d106e777034781779ed97c292ab55add90d83b2f7493d134ae6131d0da1`  
		Last Modified: Tue, 04 Mar 2025 01:03:07 GMT  
		Size: 55.6 MB (55566464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc57b4d3db403d7c5ead3baa67aa456dedf990eeaa1d6065742572037b88e9e`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fcdcc9369383bea6c794e3a5287b99fbed5f330fca9026f8ee8af97e38e288`  
		Last Modified: Tue, 04 Mar 2025 01:03:06 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:f5b23b2ecb5219b4fd968f4f0e77e03bd1739c249efd6cd9743ff73138a96a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e084d1513f7ecd8f052a99a580b237130bd85603d5bacaacf72d2e9508170e20`

```dockerfile
```

-	Layers:
	-	`sha256:36cdd24344a437d2b167b4b38ada68f9f95a41ad871c683e3146b271a927edca`  
		Last Modified: Tue, 04 Mar 2025 01:03:05 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:888ccff3b9636b55646e6bb5477e92d060a93a2c17c21e6e1bddb8907b3667ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:c1f4df2f1e5249ae9c2805fbaa593bc9c8e76a8ed12a0436996d04e8b7cc038d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2973507774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f730146db9c7982e4e32e090d898ce8bb0203dcff5a072ab1825c8984f3af`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:47:14 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:47:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:47:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:47:26 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:47:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:47:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:47:36 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:47:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5db60003403b188f7c1530d269d228ed8fcb842beb2ef4ac0e0ffe3c87d610`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686d03d51200d5ae151d48672f750801918d278241e440704a22667d7d98b197`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 364.4 KB (364432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a92737683cf4c298dc0edec0672a162c28f51a4be547f12aa894d1bc1b9203`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98fe940464aaad024d9e1802e57ed753c43c1a3da5b7adcc82b0ab16cb0a5bd`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f6146091546c80b9879daf08ba51e90ae07e7ca2a0449b6e62db8ee4355ad2`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 19.8 MB (19832344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2a3f2b03cc567ce88efb88d37ec49e5878d1c065f3d3289b759b6f303d468b`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1efa5ff8dccab563d2fb407dba261e83538e10d8f6a52d55795eca8799e07`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a1f9cfcf1a770b8e0563e10af4fe4fd665d94dbf6202cbb5d6e70d77c47ca`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0ea793b63325756fa010233c0bcec2d5e2540ebd010c854b4871488e591249`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 22.8 MB (22757621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f5b3ea67a8a43b5157e213977222af56ae70e4f8e81817bc714e75892ea9fb`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f89fa36da2f4d182f429d1e909346499105d84b6de15f3c59f203ef327771e4`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4eaef42c69737e26a4f51b2ff86be0f80f023f1cf243c7f24b56c9f07c9125`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb16e071c42270350ca5102ef4475935e3249a11df250a83a637f0c4896a944`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 21.9 MB (21894006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:d857e60eee8f4ee9d71ea880c7faa05fbbf3965f724666008415847844f86520
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334710456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a256501bc1307f791a4185e872770e8b44e05680661816f7974a375494abe2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:53:55 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:53:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:54:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:06 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:54:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:54:08 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:54:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:54:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd0a29ac12f7f5357cfca6a7cb15badd5a2fc342a81bb77ac97698701afecd0`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016be76acd15c6840b1f3c249ab0e88aca806595f849ae4defae54014d672ed3`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 343.3 KB (343272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bba7d1b615e4aa5cf86abd0f490b746e40b90733a7ed5a7b931cc208008a0a`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a757b9a15d3fa1af7bb47a9620e1db135dc5b478b45df78506291e56a9dbcd2d`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608b6e007c175f8ae40b4011323b27a3bb45ab575d0d1ba663d62e371379c2aa`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 19.8 MB (19805728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9396c1d3ca9fd43dded5884b992f48110a5592d944cae25ac9f2739299f2b3e`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a093896c4308e2f82773042ec2d94e515963b7f483a79df82035d6b4e16e0`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2fa19931d46d88400ccbe12850373ec33422e71386cf418f0f31564f379c78`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819822354481476168a3af548619cbceceeae4c2a19a1ab2d2c49613b23d832`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 22.7 MB (22731872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923ebe1421f0c6d0754bd55e14ced92f03a796d4def86fb78edd3e143b9eb5e2`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b222136c7f0e28a6668c3f86bf7c5c39b749998b118cfe6535a5cd194057d40`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97d245b4a24d519ab255dfc31ebb0ed031408cb5df38803fedd776a39828f2b`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f118966c417c3afe3fc57523f23c754d770dd204bf1a7e23ff05c5ccb714b3e5`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 21.9 MB (21876802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:6ec89c50d8a2e7140122be3cc885817ef06db86ff79ab4959f230e563b152edb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216356810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb90c5ec050a045c16a9fcaf25f380389e43ed95b32e89c6754c3d5388ad1a2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:52:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:52:50 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:53:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:53:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:53:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aad9a715a375d2c8dbcf38b891c606580b3c469223f6a06ad300be69b95982`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f35846ff4f094309b4cb17bd9244228a41c1b24f785015035b360c10421eac`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 327.5 KB (327491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753e2664deb2e592c9acd1b487b8e2c541be824f4ab302d395d4a2a61e85ed1`  
		Last Modified: Wed, 12 Mar 2025 18:53:21 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf83ab28dea983722f41794eb1be6949042863a4e4d163096fe8a27f671bcab`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6102740590b962968e8e065bc558a49a14d55e5e20198483d48542470b76e62f`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 19.8 MB (19799094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4693030fb7a286223c350e8b41f2276f8edfec6f292227335cf7fd2dc838111d`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c35ff7e4e472d5368f2f8f84b0986949edd9cd33469def72a632a526cf8bb7`  
		Last Modified: Wed, 12 Mar 2025 18:53:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b5d10cb3dbeb63171a22ffa84f71ea66f067bc4f93b935cfc8e4e88d985f43`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88fed0b769948546d05ad2d707d73d67046f51ae307c46737ace9ce1a3ec1b9`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 22.7 MB (22723657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc8cce8f76304d63d169b17d38a8634765c802bd0c32240d8df737ab81d325`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fed1f356a2be26f78799e2e2a795459a1cb01fee11bbc19d73be193980e8b6`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450b3ffc1b8b10ce5152ee50cb2cf841409eeab832e78cda33e44710d8d9c1f3`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d330fcb490da82d9eb119a9deebdac8dd6a40333e12f3f49b0500bc871119ae1`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 21.9 MB (21860255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:061a40406076ff8843375da449424a3c19052bb114078bab3189d8cb3d4cc72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:6ec89c50d8a2e7140122be3cc885817ef06db86ff79ab4959f230e563b152edb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216356810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb90c5ec050a045c16a9fcaf25f380389e43ed95b32e89c6754c3d5388ad1a2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:52:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:52:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:52:50 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:52:51 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:53:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:53:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:53:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aad9a715a375d2c8dbcf38b891c606580b3c469223f6a06ad300be69b95982`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f35846ff4f094309b4cb17bd9244228a41c1b24f785015035b360c10421eac`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 327.5 KB (327491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753e2664deb2e592c9acd1b487b8e2c541be824f4ab302d395d4a2a61e85ed1`  
		Last Modified: Wed, 12 Mar 2025 18:53:21 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf83ab28dea983722f41794eb1be6949042863a4e4d163096fe8a27f671bcab`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6102740590b962968e8e065bc558a49a14d55e5e20198483d48542470b76e62f`  
		Last Modified: Wed, 12 Mar 2025 18:53:22 GMT  
		Size: 19.8 MB (19799094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4693030fb7a286223c350e8b41f2276f8edfec6f292227335cf7fd2dc838111d`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c35ff7e4e472d5368f2f8f84b0986949edd9cd33469def72a632a526cf8bb7`  
		Last Modified: Wed, 12 Mar 2025 18:53:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b5d10cb3dbeb63171a22ffa84f71ea66f067bc4f93b935cfc8e4e88d985f43`  
		Last Modified: Wed, 12 Mar 2025 18:53:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88fed0b769948546d05ad2d707d73d67046f51ae307c46737ace9ce1a3ec1b9`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 22.7 MB (22723657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc8cce8f76304d63d169b17d38a8634765c802bd0c32240d8df737ab81d325`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fed1f356a2be26f78799e2e2a795459a1cb01fee11bbc19d73be193980e8b6`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450b3ffc1b8b10ce5152ee50cb2cf841409eeab832e78cda33e44710d8d9c1f3`  
		Last Modified: Wed, 12 Mar 2025 18:53:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d330fcb490da82d9eb119a9deebdac8dd6a40333e12f3f49b0500bc871119ae1`  
		Last Modified: Wed, 12 Mar 2025 18:53:20 GMT  
		Size: 21.9 MB (21860255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fa4d958eb2453fec999de01713c508b53a971fbbed9f3bcda63fbe7a275ec92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull docker@sha256:d857e60eee8f4ee9d71ea880c7faa05fbbf3965f724666008415847844f86520
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334710456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a256501bc1307f791a4185e872770e8b44e05680661816f7974a375494abe2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:53:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:53:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:53:55 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:53:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:54:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:06 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:54:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:54:08 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:54:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:54:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:54:16 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:54:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd0a29ac12f7f5357cfca6a7cb15badd5a2fc342a81bb77ac97698701afecd0`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016be76acd15c6840b1f3c249ab0e88aca806595f849ae4defae54014d672ed3`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 343.3 KB (343272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bba7d1b615e4aa5cf86abd0f490b746e40b90733a7ed5a7b931cc208008a0a`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a757b9a15d3fa1af7bb47a9620e1db135dc5b478b45df78506291e56a9dbcd2d`  
		Last Modified: Wed, 12 Mar 2025 18:54:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608b6e007c175f8ae40b4011323b27a3bb45ab575d0d1ba663d62e371379c2aa`  
		Last Modified: Wed, 12 Mar 2025 18:54:32 GMT  
		Size: 19.8 MB (19805728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9396c1d3ca9fd43dded5884b992f48110a5592d944cae25ac9f2739299f2b3e`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a093896c4308e2f82773042ec2d94e515963b7f483a79df82035d6b4e16e0`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2fa19931d46d88400ccbe12850373ec33422e71386cf418f0f31564f379c78`  
		Last Modified: Wed, 12 Mar 2025 18:54:29 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819822354481476168a3af548619cbceceeae4c2a19a1ab2d2c49613b23d832`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 22.7 MB (22731872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923ebe1421f0c6d0754bd55e14ced92f03a796d4def86fb78edd3e143b9eb5e2`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b222136c7f0e28a6668c3f86bf7c5c39b749998b118cfe6535a5cd194057d40`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97d245b4a24d519ab255dfc31ebb0ed031408cb5df38803fedd776a39828f2b`  
		Last Modified: Wed, 12 Mar 2025 18:54:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f118966c417c3afe3fc57523f23c754d770dd204bf1a7e23ff05c5ccb714b3e5`  
		Last Modified: Wed, 12 Mar 2025 18:54:31 GMT  
		Size: 21.9 MB (21876802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:c1ee7176bc33fb9f8af5afecd2334b44191b9c56c7a64103d001ad7c5984aa31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull docker@sha256:c1f4df2f1e5249ae9c2805fbaa593bc9c8e76a8ed12a0436996d04e8b7cc038d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2973507774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817f730146db9c7982e4e32e090d898ce8bb0203dcff5a072ab1825c8984f3af`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:47:14 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 12 Mar 2025 18:47:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Wed, 12 Mar 2025 18:47:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Wed, 12 Mar 2025 18:47:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Wed, 12 Mar 2025 18:47:26 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Wed, 12 Mar 2025 18:47:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 12 Mar 2025 18:47:35 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-windows-x86_64.exe
# Wed, 12 Mar 2025 18:47:36 GMT
ENV DOCKER_COMPOSE_SHA256=01bce3456228d8e1e4b0ba056f4b9730b7fd2c1a7113c8a985144c0fdee797b0
# Wed, 12 Mar 2025 18:47:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5db60003403b188f7c1530d269d228ed8fcb842beb2ef4ac0e0ffe3c87d610`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686d03d51200d5ae151d48672f750801918d278241e440704a22667d7d98b197`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 364.4 KB (364432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a92737683cf4c298dc0edec0672a162c28f51a4be547f12aa894d1bc1b9203`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98fe940464aaad024d9e1802e57ed753c43c1a3da5b7adcc82b0ab16cb0a5bd`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f6146091546c80b9879daf08ba51e90ae07e7ca2a0449b6e62db8ee4355ad2`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 19.8 MB (19832344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2a3f2b03cc567ce88efb88d37ec49e5878d1c065f3d3289b759b6f303d468b`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1efa5ff8dccab563d2fb407dba261e83538e10d8f6a52d55795eca8799e07`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a1f9cfcf1a770b8e0563e10af4fe4fd665d94dbf6202cbb5d6e70d77c47ca`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0ea793b63325756fa010233c0bcec2d5e2540ebd010c854b4871488e591249`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 22.8 MB (22757621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f5b3ea67a8a43b5157e213977222af56ae70e4f8e81817bc714e75892ea9fb`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f89fa36da2f4d182f429d1e909346499105d84b6de15f3c59f203ef327771e4`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4eaef42c69737e26a4f51b2ff86be0f80f023f1cf243c7f24b56c9f07c9125`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb16e071c42270350ca5102ef4475935e3249a11df250a83a637f0c4896a944`  
		Last Modified: Wed, 12 Mar 2025 18:47:48 GMT  
		Size: 21.9 MB (21894006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

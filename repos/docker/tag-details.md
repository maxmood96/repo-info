<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.0`](#docker290)
-	[`docker:29.0-cli`](#docker290-cli)
-	[`docker:29.0-dind`](#docker290-dind)
-	[`docker:29.0-dind-rootless`](#docker290-dind-rootless)
-	[`docker:29.0-windowsservercore`](#docker290-windowsservercore)
-	[`docker:29.0-windowsservercore-ltsc2022`](#docker290-windowsservercore-ltsc2022)
-	[`docker:29.0-windowsservercore-ltsc2025`](#docker290-windowsservercore-ltsc2025)
-	[`docker:29.0.1`](#docker2901)
-	[`docker:29.0.1-alpine3.22`](#docker2901-alpine322)
-	[`docker:29.0.1-cli`](#docker2901-cli)
-	[`docker:29.0.1-cli-alpine3.22`](#docker2901-cli-alpine322)
-	[`docker:29.0.1-dind`](#docker2901-dind)
-	[`docker:29.0.1-dind-alpine3.22`](#docker2901-dind-alpine322)
-	[`docker:29.0.1-dind-rootless`](#docker2901-dind-rootless)
-	[`docker:29.0.1-windowsservercore`](#docker2901-windowsservercore)
-	[`docker:29.0.1-windowsservercore-ltsc2022`](#docker2901-windowsservercore-ltsc2022)
-	[`docker:29.0.1-windowsservercore-ltsc2025`](#docker2901-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:ecac43e78380d9b9d3bd24f0ab42b370f6391a1a06a66065c10a00b9d6d57a3e
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
$ docker pull docker@sha256:00132b42611695f0faa1ba618a46322d4ed1820196d32aa154fec32c5cb68c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144707841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b2800307a6faea084b98527766ebdf588066f1b012b87b85cd1ef067b8e31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:6fbc20d0499ae60106d5f9b49eceff31343edb8aeac3e92d63203c5d3e84f0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c5c4870972a290b16e151e59a4ac0bed7fb1a544bf966055722b1da4a48174`

```dockerfile
```

-	Layers:
	-	`sha256:8382ae4791ce77e8d80f8c180eeaf4dd13717d4fffd7461872d306908ea90568`  
		Last Modified: Fri, 14 Nov 2025 21:07:32 GMT  
		Size: 34.5 KB (34546 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:e114c1871f88412b0af04436a04da150d52fc3b5338c2c9ab6376e17c150ae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136708410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff51ffa9f6c0e603f3cd4870105c3dfa12a3d43a4b7b011894d65e2e1b0314`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fbb9ab3af5e33bbb16665bd4743801e4c0bc0edf8f15d1f24ac3b873ef9cf9`  
		Last Modified: Fri, 14 Nov 2025 17:50:53 GMT  
		Size: 7.2 MB (7230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d9ee37936557e5e5e7ec317e4534765b3c8172adc5bf93a17c6e62f4b0274`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 89.9 KB (89945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c77cfca9a877080e55292eefd2344aeca081c4265ac88d3f9788851fff4200`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f622ba6a998ec6a0e7441faff66535b0b237b7dd9e99eb0e2f6a26858913ff1`  
		Last Modified: Fri, 14 Nov 2025 17:50:57 GMT  
		Size: 58.2 MB (58226630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f54398961fe271418301e8dcae9e53f00d878b96f8a8377091a69cbb0a7fb`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03f31f2f2fbd5b1caf9390b89a591da2910325080ba25bf25fd34ad8f0a62c`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:92fb4cbe157b467796f3d3ff5a3e62a203de5b795996de10ade617404f1785dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff33814f2f295e159bd1f54fa696c6153b59888521a92bec74e8295bffe608`

```dockerfile
```

-	Layers:
	-	`sha256:382fff29d9320a2efad79391da82c3dc51464c69bab0602636a5506caed19263`  
		Last Modified: Fri, 14 Nov 2025 21:07:36 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:886e5ff459e6f6be26b7484994a8d14bebe4fab3ec9529c371290b026424424e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134835020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7491f7a31f2d5b452a5789d3b65287a5ca38f7662974f31846039905736fb6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:51:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:51:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:51:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:51:12 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c2cd84bc928c20d117c9d7635a90a39831b95e8052dff3cfe3cc1bd6f0f00`  
		Last Modified: Fri, 14 Nov 2025 17:51:33 GMT  
		Size: 6.5 MB (6538247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8831271b0fde493256cfdf625b8bd29b593b50a2e41b876bd0457c205d31e`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 86.4 KB (86382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71ccd6132c6fd73522dcd76d0bb847633486222624334da36abd2c47430fd8`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2cd691ecedb982457a39c51d8021b1c4d0b9f32c50a0a5577a9fb86883015`  
		Last Modified: Fri, 14 Nov 2025 17:51:44 GMT  
		Size: 58.1 MB (58057973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1737b7d7aac53a596ec07e87ad0b783fef1583571ae58abb857a9f11b74dd5`  
		Last Modified: Fri, 14 Nov 2025 17:51:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b20a0a6faa25f08f3ed0f08d263f46cb718486a08e704ddd3db37a2f2ea5c`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:dd6b3fe3ba751f84e6dc47893d9fe7c3bd957326add76df24fb78fbf62430bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84995271acd51564889fcdb02992d8357b44c462262206e8359b295681d6d28`

```dockerfile
```

-	Layers:
	-	`sha256:69aedff7fce428d6fcf857b03c5f072505dac8dfe9a5cadb00d593c5c93d786d`  
		Last Modified: Fri, 14 Nov 2025 21:07:39 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bb993f24897a54351c5acb5d769b63d0108e0e786677f633c8d4458716100082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133979082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ed8a923f13f7602e40108a5b68dc701a9d2393812f9ae77eecc3604d129c0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:3a293b40e13f7427b260b7b7f470a8b7265cdcc61e7dd66bf7aaf7f439a4382a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899d225e33fad6679da89493be4274ee067b3b9389d791946d24d2c5a59bcd04`

```dockerfile
```

-	Layers:
	-	`sha256:a46ef6333945bb9c7c1c75266c56c269547f0646013eb229d5855f9fbcac81d4`  
		Last Modified: Fri, 14 Nov 2025 21:07:42 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:f7d048590d889e00868920f658e807ecbc4ef662d51c9af67eb5534a447d58d6
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
$ docker pull docker@sha256:b7941b2ccd806a2c6a86a9358773aa88b14b7917ed8a22af6147b1eac167ea37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75444849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5610201729349c6a70dcb8338e5ec33e1443f2a4b390f2ace27c542e2a6551f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6639e11997628dd93c3b8971e3df09ddec13aa1090dc25e18cfd82700144c51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c10f48a4154ccf09427898d95780e35a51b74f0b0868fdf8bf3914dd5e150a7`

```dockerfile
```

-	Layers:
	-	`sha256:5acd60ebabd269e3bf29e690ffb732d33fc40c5b1d23c927a1bd86937a022403`  
		Last Modified: Fri, 14 Nov 2025 18:07:45 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:de3b12999906ced6af004389ff60e8d522230851392fd1d98c2f4b1d3a3d7aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71155509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6227483b507c988892ab228db7529b849e20aaf937ee76232ab743e0ce2382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9a87490926570243a4d251dae8b8f569662ae5af2de5025d53a42d0d08d0b913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7ce2655c6bf1df9638a7a64d777afe8ed589e15bc4098a644382eeed483709`

```dockerfile
```

-	Layers:
	-	`sha256:3ff99371b5cd8e73694b7d6b254cf527f48f5f727a79d676088cccb0830d0c89`  
		Last Modified: Fri, 14 Nov 2025 18:07:48 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:76c19db0b5751c3df03c26f0ce3ce68ab059831cb81e504f8134059758b7f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4abaf932f47f68cd8df61080df26ae2934afa32af1ef9b0199884a9b3f6ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0890e3f571d08c5d82e6a43cf4c59460170ceb9b1ff8421ea78ff9e5276788f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5368d0b81e1020cfbb376075883e1424d7ea529a38d09e4c5f6180d1ea0ee`

```dockerfile
```

-	Layers:
	-	`sha256:462519a6a1755237bf46e1f96ab675d3615d2ed4d23deac96faf17e878615c8c`  
		Last Modified: Fri, 14 Nov 2025 18:07:52 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9009a0bbad1078191e0b701bba772bfaf33f06c4aeabd0c88847cd12e27bb2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70238617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47e3268b71de1f8d2b3f16253789c894ccb5c517327e000fe4f04b56b4a700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6c4b38a379125c5a42c9424120314522bbc3c2207ec499983e38878b7fdab640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a750656c16998bce5538dc78fb7d4ee4a8651174daaa388d58a43742ed6c3b`

```dockerfile
```

-	Layers:
	-	`sha256:bd54fcfe11ce172467cf267a5b45ac604e052195b987a6ae1c5642e94d12397e`  
		Last Modified: Fri, 14 Nov 2025 18:07:55 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:ecac43e78380d9b9d3bd24f0ab42b370f6391a1a06a66065c10a00b9d6d57a3e
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
$ docker pull docker@sha256:00132b42611695f0faa1ba618a46322d4ed1820196d32aa154fec32c5cb68c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144707841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b2800307a6faea084b98527766ebdf588066f1b012b87b85cd1ef067b8e31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6fbc20d0499ae60106d5f9b49eceff31343edb8aeac3e92d63203c5d3e84f0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c5c4870972a290b16e151e59a4ac0bed7fb1a544bf966055722b1da4a48174`

```dockerfile
```

-	Layers:
	-	`sha256:8382ae4791ce77e8d80f8c180eeaf4dd13717d4fffd7461872d306908ea90568`  
		Last Modified: Fri, 14 Nov 2025 21:07:32 GMT  
		Size: 34.5 KB (34546 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:e114c1871f88412b0af04436a04da150d52fc3b5338c2c9ab6376e17c150ae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136708410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff51ffa9f6c0e603f3cd4870105c3dfa12a3d43a4b7b011894d65e2e1b0314`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fbb9ab3af5e33bbb16665bd4743801e4c0bc0edf8f15d1f24ac3b873ef9cf9`  
		Last Modified: Fri, 14 Nov 2025 17:50:53 GMT  
		Size: 7.2 MB (7230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d9ee37936557e5e5e7ec317e4534765b3c8172adc5bf93a17c6e62f4b0274`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 89.9 KB (89945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c77cfca9a877080e55292eefd2344aeca081c4265ac88d3f9788851fff4200`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f622ba6a998ec6a0e7441faff66535b0b237b7dd9e99eb0e2f6a26858913ff1`  
		Last Modified: Fri, 14 Nov 2025 17:50:57 GMT  
		Size: 58.2 MB (58226630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f54398961fe271418301e8dcae9e53f00d878b96f8a8377091a69cbb0a7fb`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03f31f2f2fbd5b1caf9390b89a591da2910325080ba25bf25fd34ad8f0a62c`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:92fb4cbe157b467796f3d3ff5a3e62a203de5b795996de10ade617404f1785dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff33814f2f295e159bd1f54fa696c6153b59888521a92bec74e8295bffe608`

```dockerfile
```

-	Layers:
	-	`sha256:382fff29d9320a2efad79391da82c3dc51464c69bab0602636a5506caed19263`  
		Last Modified: Fri, 14 Nov 2025 21:07:36 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:886e5ff459e6f6be26b7484994a8d14bebe4fab3ec9529c371290b026424424e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134835020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7491f7a31f2d5b452a5789d3b65287a5ca38f7662974f31846039905736fb6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:51:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:51:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:51:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:51:12 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c2cd84bc928c20d117c9d7635a90a39831b95e8052dff3cfe3cc1bd6f0f00`  
		Last Modified: Fri, 14 Nov 2025 17:51:33 GMT  
		Size: 6.5 MB (6538247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8831271b0fde493256cfdf625b8bd29b593b50a2e41b876bd0457c205d31e`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 86.4 KB (86382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71ccd6132c6fd73522dcd76d0bb847633486222624334da36abd2c47430fd8`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2cd691ecedb982457a39c51d8021b1c4d0b9f32c50a0a5577a9fb86883015`  
		Last Modified: Fri, 14 Nov 2025 17:51:44 GMT  
		Size: 58.1 MB (58057973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1737b7d7aac53a596ec07e87ad0b783fef1583571ae58abb857a9f11b74dd5`  
		Last Modified: Fri, 14 Nov 2025 17:51:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b20a0a6faa25f08f3ed0f08d263f46cb718486a08e704ddd3db37a2f2ea5c`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:dd6b3fe3ba751f84e6dc47893d9fe7c3bd957326add76df24fb78fbf62430bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84995271acd51564889fcdb02992d8357b44c462262206e8359b295681d6d28`

```dockerfile
```

-	Layers:
	-	`sha256:69aedff7fce428d6fcf857b03c5f072505dac8dfe9a5cadb00d593c5c93d786d`  
		Last Modified: Fri, 14 Nov 2025 21:07:39 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bb993f24897a54351c5acb5d769b63d0108e0e786677f633c8d4458716100082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133979082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ed8a923f13f7602e40108a5b68dc701a9d2393812f9ae77eecc3604d129c0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3a293b40e13f7427b260b7b7f470a8b7265cdcc61e7dd66bf7aaf7f439a4382a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899d225e33fad6679da89493be4274ee067b3b9389d791946d24d2c5a59bcd04`

```dockerfile
```

-	Layers:
	-	`sha256:a46ef6333945bb9c7c1c75266c56c269547f0646013eb229d5855f9fbcac81d4`  
		Last Modified: Fri, 14 Nov 2025 21:07:42 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:b924e5892d5aefa030d9892dbc3b85db67df24d59cf946ec7e725190c1691abd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6d29b486c85d77265cc4257132508b1a86cc3cfdc2de452344afe2c234b80a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165477802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8fc7fc34477348a244b0a621318f684459f4424c2943f4ee9cbf5abce99b89`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
# Fri, 14 Nov 2025 18:10:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 14 Nov 2025 18:10:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 14 Nov 2025 18:10:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 18:10:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 14 Nov 2025 18:10:19 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 14 Nov 2025 18:10:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 14 Nov 2025 18:10:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513878b9b4e4da83bfc8de704ddf45706f0b62a2356479af219df01188ff8a48`  
		Last Modified: Fri, 14 Nov 2025 18:10:57 GMT  
		Size: 3.4 MB (3398381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e4a8852507263a81dcd77f93d54cf66f47d8ed89c986713a9dcd74981dd3e`  
		Last Modified: Fri, 14 Nov 2025 18:10:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d074650f9e9d1dac92ea2f4c7d1026952927f1ba97c8894a1bb156a5ff9653b0`  
		Last Modified: Fri, 14 Nov 2025 18:10:56 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63526e8c52dd76c90d0e3a0e6bb13b19cda2d1ff9446b85ab9132f2fb16f78fe`  
		Last Modified: Fri, 14 Nov 2025 18:10:58 GMT  
		Size: 17.4 MB (17370238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562df067ff8bc7659a7875734d42d697ffdf76e4bed8078800e7da4e2424bbe2`  
		Last Modified: Fri, 14 Nov 2025 18:10:56 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6ec58b7f35d8d3e7f65f422c3f2833c7d6f44e72c2849305ee87a57e8f089e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223534bdcc7c40e6963d71184880072aa2eece4cb8e11d03104e7a28c4135421`

```dockerfile
```

-	Layers:
	-	`sha256:7dbc601a6f7d05ebcb9447d304eadddf1015d62e57449b3c6e86b44a9adb8c62`  
		Last Modified: Fri, 14 Nov 2025 21:07:46 GMT  
		Size: 30.6 KB (30592 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bfdf109fce0ab0fd0ba42be00451d4fb714b734228858302df9768ac6d3362a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155077380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4180e8a9ce1e43c5e639c274361cb08943b78c10c5393b47b2d71f64ea48c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
# Fri, 14 Nov 2025 18:10:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 14 Nov 2025 18:10:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 14 Nov 2025 18:10:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 18:10:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 14 Nov 2025 18:10:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 14 Nov 2025 18:10:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 14 Nov 2025 18:10:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f62158be363aa14485e96848a8b96cf255e073d928be7dc5c69b46f65eb6b5b`  
		Last Modified: Fri, 14 Nov 2025 18:11:03 GMT  
		Size: 3.4 MB (3389927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5364fd5d0f73f66aa1d964ede207f062a9e616e6b42830c1f3a166ba5fb2b49`  
		Last Modified: Fri, 14 Nov 2025 18:11:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fc17712e26dd00dc065701746564366ae6b8183f29fe9c0c6856333df3b594`  
		Last Modified: Fri, 14 Nov 2025 18:11:02 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8bd711987f26afa49fcadbe781f8c6847149015fa8e1082e4ad27d1da8d2a5`  
		Last Modified: Fri, 14 Nov 2025 18:11:06 GMT  
		Size: 17.7 MB (17707029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de028bc8dfab27deee2ca498a1190fc9f027027916111582fa052454d71bf0cb`  
		Last Modified: Fri, 14 Nov 2025 18:11:02 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1f4e1b86ed838a0859f42489582c015f364311d5ab510c177b4f7930bf040383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9f9d5aa17326ac7fd25ef8e86d235ffcad8dfa411e3ba9a78f7af36845b2be`

```dockerfile
```

-	Layers:
	-	`sha256:74d0c86fb00bbe1231f84c463b2af685b2865334e1dab867c70df0d69ea4306f`  
		Last Modified: Fri, 14 Nov 2025 21:07:49 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:772aaec5cedd47b99353c76851734473b2724c7cc430b0fcbc882c7246678b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:d4513656969f64c32a00ba744aa13642743751db9b7c2442493cff588fc97517
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1502f96214ca8b767265c2d1cf293ea85c27f0044acac3a5151b1c12e3ddc303`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Fri, 14 Nov 2025 17:55:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:55:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:55:41 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:55:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:55:54 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:56:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:56:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:56:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec8692dea2a7cfeb5456bb4b993de15f76c88f0be36ba06ff89c73fa28bd532`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3756c030c25ee9a0352e8d184c9972ad760203435a360f95000a3a9ea1483db5`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 369.1 KB (369110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438ea9e974311c3c3b6d58a49066378843912aecbb7cd0fb7d961e9c3854e226`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2397c1b0ac14feac44b1a8573714b74ed790b8508fb19c11a9d63dd27536c8d`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720e07e14cdad776989cc5b530a376ed2a8777fccbfd9e9f7d1c5e4f3159c198`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 19.4 MB (19418477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d75632fe4f81ec2a724f6cac9e1e96aa25cc0d69a55177dfc00fca22150e42`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb681c47e552d8f90a197e832ece2f5a916389ce91d7dcce373001a0cacf717`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d5289b2e911e0436443f61b478f4e7ea8fb47b49ca4f0b08c023964a93a67f`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3e80662571ee22f6f212588ff170fc2f9d03dfaf33c2ae73ac2de62dcafc55`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 23.9 MB (23922840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2d5545093c2c4372e7e37e9ffc58230f3166f4eacf2d4af33f7699bf03a4b3`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c9f72fd0ce28cce8b61e2e5039431d3b23df93018467b52b2668516b0aafc9`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbbff8fd62b3ff3bfc919aaad4ac8af852c56c386751789d24f339adc0282d0`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba18e5c2618956fa6278331e4654b4726703ba698d344205e51bca5670237e5b`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 22.7 MB (22671713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:abaa83761c38ffb230bcb50a1d39744533e9666965018cfa825b0eec05f8112e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836498567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21dfcb808df45545b0f05343454835ed030e1c989ec55b3d4f578ef9de30d1e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Fri, 14 Nov 2025 17:46:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:46:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:46:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:47:22 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:47:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:47:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:47:49 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:48:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6703b96ff9900204410d0399df239a7cabe4d5e73c952ec996266a8f45346`  
		Last Modified: Fri, 14 Nov 2025 17:56:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32feda2f6f8207494b3c9e9732ebb1862d3785b36a3e4525af2de8874ba5eee7`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 502.3 KB (502252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f8d186086c63ae6514fab9464ed5b6e84edc42d0f18d1c630bbfe43e115fef`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13d933136eb971ad9c95a6de8745441fa2624b2a27cfd060f8b3258851fe2`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8456085a802821a6c35870bb91704666a064351f24ebd7e591d39d0309f0839c`  
		Last Modified: Fri, 14 Nov 2025 17:56:41 GMT  
		Size: 19.4 MB (19420220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23228b265c8267351c3b090a7093eb367490e0702e3cb7cf5250970db0258a37`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b082f0bb7964878d7ab22207b5df4f055bfc7aa97819cc449f4d8d423b919bf2`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50ae099af18d834feac25c9900b0891a0109fb464ad8f58464aaa84dcdbc161`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a569077549ea2a7f686bf31019da93372c4d61bbfe68f9bd66f6c9b367cadce7`  
		Last Modified: Fri, 14 Nov 2025 17:56:42 GMT  
		Size: 23.9 MB (23925706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44babfbf95d13b45d09fd0e43b38bbd485fa8ceb0686cc0d6ab0d3c532121f6`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcda35700f9ec33e4f5daa7429fc8ee77d4b076e14c0f0abbade72372e0832c4`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a58f8f0d06a0c8958d452e24c82a314e37348a63b44db70f1bbb741e7727863`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69feff69baaaa2240d3c0bcddf4d4c711f13550cbc03ad8307b009d44ea6a26`  
		Last Modified: Fri, 14 Nov 2025 17:56:40 GMT  
		Size: 22.7 MB (22677039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:43bb8e65e5e41a0bee0bea69e5cc5b33d765055b0de0b6bc9584152cf3cbfdfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:abaa83761c38ffb230bcb50a1d39744533e9666965018cfa825b0eec05f8112e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836498567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21dfcb808df45545b0f05343454835ed030e1c989ec55b3d4f578ef9de30d1e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Fri, 14 Nov 2025 17:46:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:46:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:46:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:47:22 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:47:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:47:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:47:49 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:48:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6703b96ff9900204410d0399df239a7cabe4d5e73c952ec996266a8f45346`  
		Last Modified: Fri, 14 Nov 2025 17:56:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32feda2f6f8207494b3c9e9732ebb1862d3785b36a3e4525af2de8874ba5eee7`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 502.3 KB (502252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f8d186086c63ae6514fab9464ed5b6e84edc42d0f18d1c630bbfe43e115fef`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13d933136eb971ad9c95a6de8745441fa2624b2a27cfd060f8b3258851fe2`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8456085a802821a6c35870bb91704666a064351f24ebd7e591d39d0309f0839c`  
		Last Modified: Fri, 14 Nov 2025 17:56:41 GMT  
		Size: 19.4 MB (19420220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23228b265c8267351c3b090a7093eb367490e0702e3cb7cf5250970db0258a37`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b082f0bb7964878d7ab22207b5df4f055bfc7aa97819cc449f4d8d423b919bf2`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50ae099af18d834feac25c9900b0891a0109fb464ad8f58464aaa84dcdbc161`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a569077549ea2a7f686bf31019da93372c4d61bbfe68f9bd66f6c9b367cadce7`  
		Last Modified: Fri, 14 Nov 2025 17:56:42 GMT  
		Size: 23.9 MB (23925706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44babfbf95d13b45d09fd0e43b38bbd485fa8ceb0686cc0d6ab0d3c532121f6`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcda35700f9ec33e4f5daa7429fc8ee77d4b076e14c0f0abbade72372e0832c4`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a58f8f0d06a0c8958d452e24c82a314e37348a63b44db70f1bbb741e7727863`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69feff69baaaa2240d3c0bcddf4d4c711f13550cbc03ad8307b009d44ea6a26`  
		Last Modified: Fri, 14 Nov 2025 17:56:40 GMT  
		Size: 22.7 MB (22677039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:3d255dbdfb3cd84597679d5d3ca0b4a9eba95cd13ee76c69e3ed677b0d2c8406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:d4513656969f64c32a00ba744aa13642743751db9b7c2442493cff588fc97517
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1502f96214ca8b767265c2d1cf293ea85c27f0044acac3a5151b1c12e3ddc303`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Fri, 14 Nov 2025 17:55:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:55:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:55:41 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:55:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:55:54 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:56:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:56:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:56:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec8692dea2a7cfeb5456bb4b993de15f76c88f0be36ba06ff89c73fa28bd532`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3756c030c25ee9a0352e8d184c9972ad760203435a360f95000a3a9ea1483db5`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 369.1 KB (369110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438ea9e974311c3c3b6d58a49066378843912aecbb7cd0fb7d961e9c3854e226`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2397c1b0ac14feac44b1a8573714b74ed790b8508fb19c11a9d63dd27536c8d`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720e07e14cdad776989cc5b530a376ed2a8777fccbfd9e9f7d1c5e4f3159c198`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 19.4 MB (19418477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d75632fe4f81ec2a724f6cac9e1e96aa25cc0d69a55177dfc00fca22150e42`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb681c47e552d8f90a197e832ece2f5a916389ce91d7dcce373001a0cacf717`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d5289b2e911e0436443f61b478f4e7ea8fb47b49ca4f0b08c023964a93a67f`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3e80662571ee22f6f212588ff170fc2f9d03dfaf33c2ae73ac2de62dcafc55`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 23.9 MB (23922840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2d5545093c2c4372e7e37e9ffc58230f3166f4eacf2d4af33f7699bf03a4b3`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c9f72fd0ce28cce8b61e2e5039431d3b23df93018467b52b2668516b0aafc9`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbbff8fd62b3ff3bfc919aaad4ac8af852c56c386751789d24f339adc0282d0`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba18e5c2618956fa6278331e4654b4726703ba698d344205e51bca5670237e5b`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 22.7 MB (22671713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0`

```console
$ docker pull docker@sha256:ecac43e78380d9b9d3bd24f0ab42b370f6391a1a06a66065c10a00b9d6d57a3e
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

### `docker:29.0` - linux; amd64

```console
$ docker pull docker@sha256:00132b42611695f0faa1ba618a46322d4ed1820196d32aa154fec32c5cb68c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144707841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b2800307a6faea084b98527766ebdf588066f1b012b87b85cd1ef067b8e31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0` - unknown; unknown

```console
$ docker pull docker@sha256:6fbc20d0499ae60106d5f9b49eceff31343edb8aeac3e92d63203c5d3e84f0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c5c4870972a290b16e151e59a4ac0bed7fb1a544bf966055722b1da4a48174`

```dockerfile
```

-	Layers:
	-	`sha256:8382ae4791ce77e8d80f8c180eeaf4dd13717d4fffd7461872d306908ea90568`  
		Last Modified: Fri, 14 Nov 2025 21:07:32 GMT  
		Size: 34.5 KB (34546 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:e114c1871f88412b0af04436a04da150d52fc3b5338c2c9ab6376e17c150ae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136708410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff51ffa9f6c0e603f3cd4870105c3dfa12a3d43a4b7b011894d65e2e1b0314`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fbb9ab3af5e33bbb16665bd4743801e4c0bc0edf8f15d1f24ac3b873ef9cf9`  
		Last Modified: Fri, 14 Nov 2025 17:50:53 GMT  
		Size: 7.2 MB (7230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d9ee37936557e5e5e7ec317e4534765b3c8172adc5bf93a17c6e62f4b0274`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 89.9 KB (89945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c77cfca9a877080e55292eefd2344aeca081c4265ac88d3f9788851fff4200`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f622ba6a998ec6a0e7441faff66535b0b237b7dd9e99eb0e2f6a26858913ff1`  
		Last Modified: Fri, 14 Nov 2025 17:50:57 GMT  
		Size: 58.2 MB (58226630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f54398961fe271418301e8dcae9e53f00d878b96f8a8377091a69cbb0a7fb`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03f31f2f2fbd5b1caf9390b89a591da2910325080ba25bf25fd34ad8f0a62c`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0` - unknown; unknown

```console
$ docker pull docker@sha256:92fb4cbe157b467796f3d3ff5a3e62a203de5b795996de10ade617404f1785dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff33814f2f295e159bd1f54fa696c6153b59888521a92bec74e8295bffe608`

```dockerfile
```

-	Layers:
	-	`sha256:382fff29d9320a2efad79391da82c3dc51464c69bab0602636a5506caed19263`  
		Last Modified: Fri, 14 Nov 2025 21:07:36 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:886e5ff459e6f6be26b7484994a8d14bebe4fab3ec9529c371290b026424424e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134835020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7491f7a31f2d5b452a5789d3b65287a5ca38f7662974f31846039905736fb6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:51:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:51:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:51:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:51:12 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c2cd84bc928c20d117c9d7635a90a39831b95e8052dff3cfe3cc1bd6f0f00`  
		Last Modified: Fri, 14 Nov 2025 17:51:33 GMT  
		Size: 6.5 MB (6538247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8831271b0fde493256cfdf625b8bd29b593b50a2e41b876bd0457c205d31e`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 86.4 KB (86382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71ccd6132c6fd73522dcd76d0bb847633486222624334da36abd2c47430fd8`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2cd691ecedb982457a39c51d8021b1c4d0b9f32c50a0a5577a9fb86883015`  
		Last Modified: Fri, 14 Nov 2025 17:51:44 GMT  
		Size: 58.1 MB (58057973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1737b7d7aac53a596ec07e87ad0b783fef1583571ae58abb857a9f11b74dd5`  
		Last Modified: Fri, 14 Nov 2025 17:51:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b20a0a6faa25f08f3ed0f08d263f46cb718486a08e704ddd3db37a2f2ea5c`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0` - unknown; unknown

```console
$ docker pull docker@sha256:dd6b3fe3ba751f84e6dc47893d9fe7c3bd957326add76df24fb78fbf62430bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84995271acd51564889fcdb02992d8357b44c462262206e8359b295681d6d28`

```dockerfile
```

-	Layers:
	-	`sha256:69aedff7fce428d6fcf857b03c5f072505dac8dfe9a5cadb00d593c5c93d786d`  
		Last Modified: Fri, 14 Nov 2025 21:07:39 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bb993f24897a54351c5acb5d769b63d0108e0e786677f633c8d4458716100082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133979082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ed8a923f13f7602e40108a5b68dc701a9d2393812f9ae77eecc3604d129c0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0` - unknown; unknown

```console
$ docker pull docker@sha256:3a293b40e13f7427b260b7b7f470a8b7265cdcc61e7dd66bf7aaf7f439a4382a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899d225e33fad6679da89493be4274ee067b3b9389d791946d24d2c5a59bcd04`

```dockerfile
```

-	Layers:
	-	`sha256:a46ef6333945bb9c7c1c75266c56c269547f0646013eb229d5855f9fbcac81d4`  
		Last Modified: Fri, 14 Nov 2025 21:07:42 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0-cli`

```console
$ docker pull docker@sha256:f7d048590d889e00868920f658e807ecbc4ef662d51c9af67eb5534a447d58d6
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

### `docker:29.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:b7941b2ccd806a2c6a86a9358773aa88b14b7917ed8a22af6147b1eac167ea37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75444849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5610201729349c6a70dcb8338e5ec33e1443f2a4b390f2ace27c542e2a6551f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6639e11997628dd93c3b8971e3df09ddec13aa1090dc25e18cfd82700144c51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c10f48a4154ccf09427898d95780e35a51b74f0b0868fdf8bf3914dd5e150a7`

```dockerfile
```

-	Layers:
	-	`sha256:5acd60ebabd269e3bf29e690ffb732d33fc40c5b1d23c927a1bd86937a022403`  
		Last Modified: Fri, 14 Nov 2025 18:07:45 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:de3b12999906ced6af004389ff60e8d522230851392fd1d98c2f4b1d3a3d7aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71155509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6227483b507c988892ab228db7529b849e20aaf937ee76232ab743e0ce2382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9a87490926570243a4d251dae8b8f569662ae5af2de5025d53a42d0d08d0b913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7ce2655c6bf1df9638a7a64d777afe8ed589e15bc4098a644382eeed483709`

```dockerfile
```

-	Layers:
	-	`sha256:3ff99371b5cd8e73694b7d6b254cf527f48f5f727a79d676088cccb0830d0c89`  
		Last Modified: Fri, 14 Nov 2025 18:07:48 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:76c19db0b5751c3df03c26f0ce3ce68ab059831cb81e504f8134059758b7f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4abaf932f47f68cd8df61080df26ae2934afa32af1ef9b0199884a9b3f6ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0890e3f571d08c5d82e6a43cf4c59460170ceb9b1ff8421ea78ff9e5276788f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5368d0b81e1020cfbb376075883e1424d7ea529a38d09e4c5f6180d1ea0ee`

```dockerfile
```

-	Layers:
	-	`sha256:462519a6a1755237bf46e1f96ab675d3615d2ed4d23deac96faf17e878615c8c`  
		Last Modified: Fri, 14 Nov 2025 18:07:52 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9009a0bbad1078191e0b701bba772bfaf33f06c4aeabd0c88847cd12e27bb2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70238617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47e3268b71de1f8d2b3f16253789c894ccb5c517327e000fe4f04b56b4a700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6c4b38a379125c5a42c9424120314522bbc3c2207ec499983e38878b7fdab640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a750656c16998bce5538dc78fb7d4ee4a8651174daaa388d58a43742ed6c3b`

```dockerfile
```

-	Layers:
	-	`sha256:bd54fcfe11ce172467cf267a5b45ac604e052195b987a6ae1c5642e94d12397e`  
		Last Modified: Fri, 14 Nov 2025 18:07:55 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0-dind`

```console
$ docker pull docker@sha256:ecac43e78380d9b9d3bd24f0ab42b370f6391a1a06a66065c10a00b9d6d57a3e
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

### `docker:29.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:00132b42611695f0faa1ba618a46322d4ed1820196d32aa154fec32c5cb68c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144707841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b2800307a6faea084b98527766ebdf588066f1b012b87b85cd1ef067b8e31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6fbc20d0499ae60106d5f9b49eceff31343edb8aeac3e92d63203c5d3e84f0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c5c4870972a290b16e151e59a4ac0bed7fb1a544bf966055722b1da4a48174`

```dockerfile
```

-	Layers:
	-	`sha256:8382ae4791ce77e8d80f8c180eeaf4dd13717d4fffd7461872d306908ea90568`  
		Last Modified: Fri, 14 Nov 2025 21:07:32 GMT  
		Size: 34.5 KB (34546 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:e114c1871f88412b0af04436a04da150d52fc3b5338c2c9ab6376e17c150ae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136708410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff51ffa9f6c0e603f3cd4870105c3dfa12a3d43a4b7b011894d65e2e1b0314`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fbb9ab3af5e33bbb16665bd4743801e4c0bc0edf8f15d1f24ac3b873ef9cf9`  
		Last Modified: Fri, 14 Nov 2025 17:50:53 GMT  
		Size: 7.2 MB (7230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d9ee37936557e5e5e7ec317e4534765b3c8172adc5bf93a17c6e62f4b0274`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 89.9 KB (89945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c77cfca9a877080e55292eefd2344aeca081c4265ac88d3f9788851fff4200`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f622ba6a998ec6a0e7441faff66535b0b237b7dd9e99eb0e2f6a26858913ff1`  
		Last Modified: Fri, 14 Nov 2025 17:50:57 GMT  
		Size: 58.2 MB (58226630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f54398961fe271418301e8dcae9e53f00d878b96f8a8377091a69cbb0a7fb`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03f31f2f2fbd5b1caf9390b89a591da2910325080ba25bf25fd34ad8f0a62c`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:92fb4cbe157b467796f3d3ff5a3e62a203de5b795996de10ade617404f1785dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff33814f2f295e159bd1f54fa696c6153b59888521a92bec74e8295bffe608`

```dockerfile
```

-	Layers:
	-	`sha256:382fff29d9320a2efad79391da82c3dc51464c69bab0602636a5506caed19263`  
		Last Modified: Fri, 14 Nov 2025 21:07:36 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:886e5ff459e6f6be26b7484994a8d14bebe4fab3ec9529c371290b026424424e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134835020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7491f7a31f2d5b452a5789d3b65287a5ca38f7662974f31846039905736fb6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:51:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:51:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:51:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:51:12 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c2cd84bc928c20d117c9d7635a90a39831b95e8052dff3cfe3cc1bd6f0f00`  
		Last Modified: Fri, 14 Nov 2025 17:51:33 GMT  
		Size: 6.5 MB (6538247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8831271b0fde493256cfdf625b8bd29b593b50a2e41b876bd0457c205d31e`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 86.4 KB (86382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71ccd6132c6fd73522dcd76d0bb847633486222624334da36abd2c47430fd8`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2cd691ecedb982457a39c51d8021b1c4d0b9f32c50a0a5577a9fb86883015`  
		Last Modified: Fri, 14 Nov 2025 17:51:44 GMT  
		Size: 58.1 MB (58057973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1737b7d7aac53a596ec07e87ad0b783fef1583571ae58abb857a9f11b74dd5`  
		Last Modified: Fri, 14 Nov 2025 17:51:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b20a0a6faa25f08f3ed0f08d263f46cb718486a08e704ddd3db37a2f2ea5c`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:dd6b3fe3ba751f84e6dc47893d9fe7c3bd957326add76df24fb78fbf62430bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84995271acd51564889fcdb02992d8357b44c462262206e8359b295681d6d28`

```dockerfile
```

-	Layers:
	-	`sha256:69aedff7fce428d6fcf857b03c5f072505dac8dfe9a5cadb00d593c5c93d786d`  
		Last Modified: Fri, 14 Nov 2025 21:07:39 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bb993f24897a54351c5acb5d769b63d0108e0e786677f633c8d4458716100082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133979082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ed8a923f13f7602e40108a5b68dc701a9d2393812f9ae77eecc3604d129c0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3a293b40e13f7427b260b7b7f470a8b7265cdcc61e7dd66bf7aaf7f439a4382a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899d225e33fad6679da89493be4274ee067b3b9389d791946d24d2c5a59bcd04`

```dockerfile
```

-	Layers:
	-	`sha256:a46ef6333945bb9c7c1c75266c56c269547f0646013eb229d5855f9fbcac81d4`  
		Last Modified: Fri, 14 Nov 2025 21:07:42 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0-dind-rootless`

```console
$ docker pull docker@sha256:b924e5892d5aefa030d9892dbc3b85db67df24d59cf946ec7e725190c1691abd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6d29b486c85d77265cc4257132508b1a86cc3cfdc2de452344afe2c234b80a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165477802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8fc7fc34477348a244b0a621318f684459f4424c2943f4ee9cbf5abce99b89`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
# Fri, 14 Nov 2025 18:10:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 14 Nov 2025 18:10:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 14 Nov 2025 18:10:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 18:10:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 14 Nov 2025 18:10:19 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 14 Nov 2025 18:10:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 14 Nov 2025 18:10:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513878b9b4e4da83bfc8de704ddf45706f0b62a2356479af219df01188ff8a48`  
		Last Modified: Fri, 14 Nov 2025 18:10:57 GMT  
		Size: 3.4 MB (3398381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e4a8852507263a81dcd77f93d54cf66f47d8ed89c986713a9dcd74981dd3e`  
		Last Modified: Fri, 14 Nov 2025 18:10:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d074650f9e9d1dac92ea2f4c7d1026952927f1ba97c8894a1bb156a5ff9653b0`  
		Last Modified: Fri, 14 Nov 2025 18:10:56 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63526e8c52dd76c90d0e3a0e6bb13b19cda2d1ff9446b85ab9132f2fb16f78fe`  
		Last Modified: Fri, 14 Nov 2025 18:10:58 GMT  
		Size: 17.4 MB (17370238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562df067ff8bc7659a7875734d42d697ffdf76e4bed8078800e7da4e2424bbe2`  
		Last Modified: Fri, 14 Nov 2025 18:10:56 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6ec58b7f35d8d3e7f65f422c3f2833c7d6f44e72c2849305ee87a57e8f089e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223534bdcc7c40e6963d71184880072aa2eece4cb8e11d03104e7a28c4135421`

```dockerfile
```

-	Layers:
	-	`sha256:7dbc601a6f7d05ebcb9447d304eadddf1015d62e57449b3c6e86b44a9adb8c62`  
		Last Modified: Fri, 14 Nov 2025 21:07:46 GMT  
		Size: 30.6 KB (30592 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bfdf109fce0ab0fd0ba42be00451d4fb714b734228858302df9768ac6d3362a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155077380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4180e8a9ce1e43c5e639c274361cb08943b78c10c5393b47b2d71f64ea48c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
# Fri, 14 Nov 2025 18:10:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 14 Nov 2025 18:10:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 14 Nov 2025 18:10:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 18:10:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 14 Nov 2025 18:10:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 14 Nov 2025 18:10:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 14 Nov 2025 18:10:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f62158be363aa14485e96848a8b96cf255e073d928be7dc5c69b46f65eb6b5b`  
		Last Modified: Fri, 14 Nov 2025 18:11:03 GMT  
		Size: 3.4 MB (3389927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5364fd5d0f73f66aa1d964ede207f062a9e616e6b42830c1f3a166ba5fb2b49`  
		Last Modified: Fri, 14 Nov 2025 18:11:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fc17712e26dd00dc065701746564366ae6b8183f29fe9c0c6856333df3b594`  
		Last Modified: Fri, 14 Nov 2025 18:11:02 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8bd711987f26afa49fcadbe781f8c6847149015fa8e1082e4ad27d1da8d2a5`  
		Last Modified: Fri, 14 Nov 2025 18:11:06 GMT  
		Size: 17.7 MB (17707029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de028bc8dfab27deee2ca498a1190fc9f027027916111582fa052454d71bf0cb`  
		Last Modified: Fri, 14 Nov 2025 18:11:02 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1f4e1b86ed838a0859f42489582c015f364311d5ab510c177b4f7930bf040383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9f9d5aa17326ac7fd25ef8e86d235ffcad8dfa411e3ba9a78f7af36845b2be`

```dockerfile
```

-	Layers:
	-	`sha256:74d0c86fb00bbe1231f84c463b2af685b2865334e1dab867c70df0d69ea4306f`  
		Last Modified: Fri, 14 Nov 2025 21:07:49 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0-windowsservercore`

```console
$ docker pull docker@sha256:772aaec5cedd47b99353c76851734473b2724c7cc430b0fcbc882c7246678b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:29.0-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:d4513656969f64c32a00ba744aa13642743751db9b7c2442493cff588fc97517
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1502f96214ca8b767265c2d1cf293ea85c27f0044acac3a5151b1c12e3ddc303`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Fri, 14 Nov 2025 17:55:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:55:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:55:41 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:55:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:55:54 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:56:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:56:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:56:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec8692dea2a7cfeb5456bb4b993de15f76c88f0be36ba06ff89c73fa28bd532`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3756c030c25ee9a0352e8d184c9972ad760203435a360f95000a3a9ea1483db5`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 369.1 KB (369110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438ea9e974311c3c3b6d58a49066378843912aecbb7cd0fb7d961e9c3854e226`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2397c1b0ac14feac44b1a8573714b74ed790b8508fb19c11a9d63dd27536c8d`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720e07e14cdad776989cc5b530a376ed2a8777fccbfd9e9f7d1c5e4f3159c198`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 19.4 MB (19418477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d75632fe4f81ec2a724f6cac9e1e96aa25cc0d69a55177dfc00fca22150e42`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb681c47e552d8f90a197e832ece2f5a916389ce91d7dcce373001a0cacf717`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d5289b2e911e0436443f61b478f4e7ea8fb47b49ca4f0b08c023964a93a67f`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3e80662571ee22f6f212588ff170fc2f9d03dfaf33c2ae73ac2de62dcafc55`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 23.9 MB (23922840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2d5545093c2c4372e7e37e9ffc58230f3166f4eacf2d4af33f7699bf03a4b3`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c9f72fd0ce28cce8b61e2e5039431d3b23df93018467b52b2668516b0aafc9`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbbff8fd62b3ff3bfc919aaad4ac8af852c56c386751789d24f339adc0282d0`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba18e5c2618956fa6278331e4654b4726703ba698d344205e51bca5670237e5b`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 22.7 MB (22671713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.0-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:abaa83761c38ffb230bcb50a1d39744533e9666965018cfa825b0eec05f8112e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836498567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21dfcb808df45545b0f05343454835ed030e1c989ec55b3d4f578ef9de30d1e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Fri, 14 Nov 2025 17:46:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:46:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:46:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:47:22 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:47:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:47:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:47:49 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:48:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6703b96ff9900204410d0399df239a7cabe4d5e73c952ec996266a8f45346`  
		Last Modified: Fri, 14 Nov 2025 17:56:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32feda2f6f8207494b3c9e9732ebb1862d3785b36a3e4525af2de8874ba5eee7`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 502.3 KB (502252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f8d186086c63ae6514fab9464ed5b6e84edc42d0f18d1c630bbfe43e115fef`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13d933136eb971ad9c95a6de8745441fa2624b2a27cfd060f8b3258851fe2`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8456085a802821a6c35870bb91704666a064351f24ebd7e591d39d0309f0839c`  
		Last Modified: Fri, 14 Nov 2025 17:56:41 GMT  
		Size: 19.4 MB (19420220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23228b265c8267351c3b090a7093eb367490e0702e3cb7cf5250970db0258a37`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b082f0bb7964878d7ab22207b5df4f055bfc7aa97819cc449f4d8d423b919bf2`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50ae099af18d834feac25c9900b0891a0109fb464ad8f58464aaa84dcdbc161`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a569077549ea2a7f686bf31019da93372c4d61bbfe68f9bd66f6c9b367cadce7`  
		Last Modified: Fri, 14 Nov 2025 17:56:42 GMT  
		Size: 23.9 MB (23925706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44babfbf95d13b45d09fd0e43b38bbd485fa8ceb0686cc0d6ab0d3c532121f6`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcda35700f9ec33e4f5daa7429fc8ee77d4b076e14c0f0abbade72372e0832c4`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a58f8f0d06a0c8958d452e24c82a314e37348a63b44db70f1bbb741e7727863`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69feff69baaaa2240d3c0bcddf4d4c711f13550cbc03ad8307b009d44ea6a26`  
		Last Modified: Fri, 14 Nov 2025 17:56:40 GMT  
		Size: 22.7 MB (22677039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:43bb8e65e5e41a0bee0bea69e5cc5b33d765055b0de0b6bc9584152cf3cbfdfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:29.0-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:abaa83761c38ffb230bcb50a1d39744533e9666965018cfa825b0eec05f8112e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836498567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21dfcb808df45545b0f05343454835ed030e1c989ec55b3d4f578ef9de30d1e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Fri, 14 Nov 2025 17:46:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:46:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:46:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:47:22 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:47:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:47:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:47:49 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:48:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6703b96ff9900204410d0399df239a7cabe4d5e73c952ec996266a8f45346`  
		Last Modified: Fri, 14 Nov 2025 17:56:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32feda2f6f8207494b3c9e9732ebb1862d3785b36a3e4525af2de8874ba5eee7`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 502.3 KB (502252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f8d186086c63ae6514fab9464ed5b6e84edc42d0f18d1c630bbfe43e115fef`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13d933136eb971ad9c95a6de8745441fa2624b2a27cfd060f8b3258851fe2`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8456085a802821a6c35870bb91704666a064351f24ebd7e591d39d0309f0839c`  
		Last Modified: Fri, 14 Nov 2025 17:56:41 GMT  
		Size: 19.4 MB (19420220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23228b265c8267351c3b090a7093eb367490e0702e3cb7cf5250970db0258a37`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b082f0bb7964878d7ab22207b5df4f055bfc7aa97819cc449f4d8d423b919bf2`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50ae099af18d834feac25c9900b0891a0109fb464ad8f58464aaa84dcdbc161`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a569077549ea2a7f686bf31019da93372c4d61bbfe68f9bd66f6c9b367cadce7`  
		Last Modified: Fri, 14 Nov 2025 17:56:42 GMT  
		Size: 23.9 MB (23925706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44babfbf95d13b45d09fd0e43b38bbd485fa8ceb0686cc0d6ab0d3c532121f6`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcda35700f9ec33e4f5daa7429fc8ee77d4b076e14c0f0abbade72372e0832c4`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a58f8f0d06a0c8958d452e24c82a314e37348a63b44db70f1bbb741e7727863`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69feff69baaaa2240d3c0bcddf4d4c711f13550cbc03ad8307b009d44ea6a26`  
		Last Modified: Fri, 14 Nov 2025 17:56:40 GMT  
		Size: 22.7 MB (22677039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:3d255dbdfb3cd84597679d5d3ca0b4a9eba95cd13ee76c69e3ed677b0d2c8406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:29.0-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:d4513656969f64c32a00ba744aa13642743751db9b7c2442493cff588fc97517
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1502f96214ca8b767265c2d1cf293ea85c27f0044acac3a5151b1c12e3ddc303`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Fri, 14 Nov 2025 17:55:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:55:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:55:41 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:55:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:55:54 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:56:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:56:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:56:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec8692dea2a7cfeb5456bb4b993de15f76c88f0be36ba06ff89c73fa28bd532`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3756c030c25ee9a0352e8d184c9972ad760203435a360f95000a3a9ea1483db5`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 369.1 KB (369110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438ea9e974311c3c3b6d58a49066378843912aecbb7cd0fb7d961e9c3854e226`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2397c1b0ac14feac44b1a8573714b74ed790b8508fb19c11a9d63dd27536c8d`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720e07e14cdad776989cc5b530a376ed2a8777fccbfd9e9f7d1c5e4f3159c198`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 19.4 MB (19418477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d75632fe4f81ec2a724f6cac9e1e96aa25cc0d69a55177dfc00fca22150e42`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb681c47e552d8f90a197e832ece2f5a916389ce91d7dcce373001a0cacf717`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d5289b2e911e0436443f61b478f4e7ea8fb47b49ca4f0b08c023964a93a67f`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3e80662571ee22f6f212588ff170fc2f9d03dfaf33c2ae73ac2de62dcafc55`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 23.9 MB (23922840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2d5545093c2c4372e7e37e9ffc58230f3166f4eacf2d4af33f7699bf03a4b3`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c9f72fd0ce28cce8b61e2e5039431d3b23df93018467b52b2668516b0aafc9`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbbff8fd62b3ff3bfc919aaad4ac8af852c56c386751789d24f339adc0282d0`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba18e5c2618956fa6278331e4654b4726703ba698d344205e51bca5670237e5b`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 22.7 MB (22671713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0.1`

```console
$ docker pull docker@sha256:ecac43e78380d9b9d3bd24f0ab42b370f6391a1a06a66065c10a00b9d6d57a3e
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

### `docker:29.0.1` - linux; amd64

```console
$ docker pull docker@sha256:00132b42611695f0faa1ba618a46322d4ed1820196d32aa154fec32c5cb68c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144707841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b2800307a6faea084b98527766ebdf588066f1b012b87b85cd1ef067b8e31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1` - unknown; unknown

```console
$ docker pull docker@sha256:6fbc20d0499ae60106d5f9b49eceff31343edb8aeac3e92d63203c5d3e84f0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c5c4870972a290b16e151e59a4ac0bed7fb1a544bf966055722b1da4a48174`

```dockerfile
```

-	Layers:
	-	`sha256:8382ae4791ce77e8d80f8c180eeaf4dd13717d4fffd7461872d306908ea90568`  
		Last Modified: Fri, 14 Nov 2025 21:07:32 GMT  
		Size: 34.5 KB (34546 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:e114c1871f88412b0af04436a04da150d52fc3b5338c2c9ab6376e17c150ae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136708410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff51ffa9f6c0e603f3cd4870105c3dfa12a3d43a4b7b011894d65e2e1b0314`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fbb9ab3af5e33bbb16665bd4743801e4c0bc0edf8f15d1f24ac3b873ef9cf9`  
		Last Modified: Fri, 14 Nov 2025 17:50:53 GMT  
		Size: 7.2 MB (7230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d9ee37936557e5e5e7ec317e4534765b3c8172adc5bf93a17c6e62f4b0274`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 89.9 KB (89945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c77cfca9a877080e55292eefd2344aeca081c4265ac88d3f9788851fff4200`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f622ba6a998ec6a0e7441faff66535b0b237b7dd9e99eb0e2f6a26858913ff1`  
		Last Modified: Fri, 14 Nov 2025 17:50:57 GMT  
		Size: 58.2 MB (58226630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f54398961fe271418301e8dcae9e53f00d878b96f8a8377091a69cbb0a7fb`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03f31f2f2fbd5b1caf9390b89a591da2910325080ba25bf25fd34ad8f0a62c`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1` - unknown; unknown

```console
$ docker pull docker@sha256:92fb4cbe157b467796f3d3ff5a3e62a203de5b795996de10ade617404f1785dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff33814f2f295e159bd1f54fa696c6153b59888521a92bec74e8295bffe608`

```dockerfile
```

-	Layers:
	-	`sha256:382fff29d9320a2efad79391da82c3dc51464c69bab0602636a5506caed19263`  
		Last Modified: Fri, 14 Nov 2025 21:07:36 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:886e5ff459e6f6be26b7484994a8d14bebe4fab3ec9529c371290b026424424e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134835020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7491f7a31f2d5b452a5789d3b65287a5ca38f7662974f31846039905736fb6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:51:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:51:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:51:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:51:12 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c2cd84bc928c20d117c9d7635a90a39831b95e8052dff3cfe3cc1bd6f0f00`  
		Last Modified: Fri, 14 Nov 2025 17:51:33 GMT  
		Size: 6.5 MB (6538247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8831271b0fde493256cfdf625b8bd29b593b50a2e41b876bd0457c205d31e`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 86.4 KB (86382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71ccd6132c6fd73522dcd76d0bb847633486222624334da36abd2c47430fd8`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2cd691ecedb982457a39c51d8021b1c4d0b9f32c50a0a5577a9fb86883015`  
		Last Modified: Fri, 14 Nov 2025 17:51:44 GMT  
		Size: 58.1 MB (58057973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1737b7d7aac53a596ec07e87ad0b783fef1583571ae58abb857a9f11b74dd5`  
		Last Modified: Fri, 14 Nov 2025 17:51:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b20a0a6faa25f08f3ed0f08d263f46cb718486a08e704ddd3db37a2f2ea5c`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1` - unknown; unknown

```console
$ docker pull docker@sha256:dd6b3fe3ba751f84e6dc47893d9fe7c3bd957326add76df24fb78fbf62430bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84995271acd51564889fcdb02992d8357b44c462262206e8359b295681d6d28`

```dockerfile
```

-	Layers:
	-	`sha256:69aedff7fce428d6fcf857b03c5f072505dac8dfe9a5cadb00d593c5c93d786d`  
		Last Modified: Fri, 14 Nov 2025 21:07:39 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bb993f24897a54351c5acb5d769b63d0108e0e786677f633c8d4458716100082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133979082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ed8a923f13f7602e40108a5b68dc701a9d2393812f9ae77eecc3604d129c0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1` - unknown; unknown

```console
$ docker pull docker@sha256:3a293b40e13f7427b260b7b7f470a8b7265cdcc61e7dd66bf7aaf7f439a4382a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899d225e33fad6679da89493be4274ee067b3b9389d791946d24d2c5a59bcd04`

```dockerfile
```

-	Layers:
	-	`sha256:a46ef6333945bb9c7c1c75266c56c269547f0646013eb229d5855f9fbcac81d4`  
		Last Modified: Fri, 14 Nov 2025 21:07:42 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.1-alpine3.22`

```console
$ docker pull docker@sha256:ecac43e78380d9b9d3bd24f0ab42b370f6391a1a06a66065c10a00b9d6d57a3e
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

### `docker:29.0.1-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:00132b42611695f0faa1ba618a46322d4ed1820196d32aa154fec32c5cb68c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144707841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b2800307a6faea084b98527766ebdf588066f1b012b87b85cd1ef067b8e31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6fbc20d0499ae60106d5f9b49eceff31343edb8aeac3e92d63203c5d3e84f0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c5c4870972a290b16e151e59a4ac0bed7fb1a544bf966055722b1da4a48174`

```dockerfile
```

-	Layers:
	-	`sha256:8382ae4791ce77e8d80f8c180eeaf4dd13717d4fffd7461872d306908ea90568`  
		Last Modified: Fri, 14 Nov 2025 21:07:32 GMT  
		Size: 34.5 KB (34546 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:e114c1871f88412b0af04436a04da150d52fc3b5338c2c9ab6376e17c150ae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136708410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff51ffa9f6c0e603f3cd4870105c3dfa12a3d43a4b7b011894d65e2e1b0314`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fbb9ab3af5e33bbb16665bd4743801e4c0bc0edf8f15d1f24ac3b873ef9cf9`  
		Last Modified: Fri, 14 Nov 2025 17:50:53 GMT  
		Size: 7.2 MB (7230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d9ee37936557e5e5e7ec317e4534765b3c8172adc5bf93a17c6e62f4b0274`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 89.9 KB (89945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c77cfca9a877080e55292eefd2344aeca081c4265ac88d3f9788851fff4200`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f622ba6a998ec6a0e7441faff66535b0b237b7dd9e99eb0e2f6a26858913ff1`  
		Last Modified: Fri, 14 Nov 2025 17:50:57 GMT  
		Size: 58.2 MB (58226630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f54398961fe271418301e8dcae9e53f00d878b96f8a8377091a69cbb0a7fb`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03f31f2f2fbd5b1caf9390b89a591da2910325080ba25bf25fd34ad8f0a62c`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:92fb4cbe157b467796f3d3ff5a3e62a203de5b795996de10ade617404f1785dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff33814f2f295e159bd1f54fa696c6153b59888521a92bec74e8295bffe608`

```dockerfile
```

-	Layers:
	-	`sha256:382fff29d9320a2efad79391da82c3dc51464c69bab0602636a5506caed19263`  
		Last Modified: Fri, 14 Nov 2025 21:07:36 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:886e5ff459e6f6be26b7484994a8d14bebe4fab3ec9529c371290b026424424e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134835020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7491f7a31f2d5b452a5789d3b65287a5ca38f7662974f31846039905736fb6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:51:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:51:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:51:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:51:12 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c2cd84bc928c20d117c9d7635a90a39831b95e8052dff3cfe3cc1bd6f0f00`  
		Last Modified: Fri, 14 Nov 2025 17:51:33 GMT  
		Size: 6.5 MB (6538247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8831271b0fde493256cfdf625b8bd29b593b50a2e41b876bd0457c205d31e`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 86.4 KB (86382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71ccd6132c6fd73522dcd76d0bb847633486222624334da36abd2c47430fd8`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2cd691ecedb982457a39c51d8021b1c4d0b9f32c50a0a5577a9fb86883015`  
		Last Modified: Fri, 14 Nov 2025 17:51:44 GMT  
		Size: 58.1 MB (58057973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1737b7d7aac53a596ec07e87ad0b783fef1583571ae58abb857a9f11b74dd5`  
		Last Modified: Fri, 14 Nov 2025 17:51:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b20a0a6faa25f08f3ed0f08d263f46cb718486a08e704ddd3db37a2f2ea5c`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:dd6b3fe3ba751f84e6dc47893d9fe7c3bd957326add76df24fb78fbf62430bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84995271acd51564889fcdb02992d8357b44c462262206e8359b295681d6d28`

```dockerfile
```

-	Layers:
	-	`sha256:69aedff7fce428d6fcf857b03c5f072505dac8dfe9a5cadb00d593c5c93d786d`  
		Last Modified: Fri, 14 Nov 2025 21:07:39 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bb993f24897a54351c5acb5d769b63d0108e0e786677f633c8d4458716100082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133979082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ed8a923f13f7602e40108a5b68dc701a9d2393812f9ae77eecc3604d129c0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:3a293b40e13f7427b260b7b7f470a8b7265cdcc61e7dd66bf7aaf7f439a4382a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899d225e33fad6679da89493be4274ee067b3b9389d791946d24d2c5a59bcd04`

```dockerfile
```

-	Layers:
	-	`sha256:a46ef6333945bb9c7c1c75266c56c269547f0646013eb229d5855f9fbcac81d4`  
		Last Modified: Fri, 14 Nov 2025 21:07:42 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.1-cli`

```console
$ docker pull docker@sha256:f7d048590d889e00868920f658e807ecbc4ef662d51c9af67eb5534a447d58d6
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

### `docker:29.0.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:b7941b2ccd806a2c6a86a9358773aa88b14b7917ed8a22af6147b1eac167ea37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75444849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5610201729349c6a70dcb8338e5ec33e1443f2a4b390f2ace27c542e2a6551f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6639e11997628dd93c3b8971e3df09ddec13aa1090dc25e18cfd82700144c51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c10f48a4154ccf09427898d95780e35a51b74f0b0868fdf8bf3914dd5e150a7`

```dockerfile
```

-	Layers:
	-	`sha256:5acd60ebabd269e3bf29e690ffb732d33fc40c5b1d23c927a1bd86937a022403`  
		Last Modified: Fri, 14 Nov 2025 18:07:45 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:de3b12999906ced6af004389ff60e8d522230851392fd1d98c2f4b1d3a3d7aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71155509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6227483b507c988892ab228db7529b849e20aaf937ee76232ab743e0ce2382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:9a87490926570243a4d251dae8b8f569662ae5af2de5025d53a42d0d08d0b913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7ce2655c6bf1df9638a7a64d777afe8ed589e15bc4098a644382eeed483709`

```dockerfile
```

-	Layers:
	-	`sha256:3ff99371b5cd8e73694b7d6b254cf527f48f5f727a79d676088cccb0830d0c89`  
		Last Modified: Fri, 14 Nov 2025 18:07:48 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:76c19db0b5751c3df03c26f0ce3ce68ab059831cb81e504f8134059758b7f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4abaf932f47f68cd8df61080df26ae2934afa32af1ef9b0199884a9b3f6ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:0890e3f571d08c5d82e6a43cf4c59460170ceb9b1ff8421ea78ff9e5276788f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5368d0b81e1020cfbb376075883e1424d7ea529a38d09e4c5f6180d1ea0ee`

```dockerfile
```

-	Layers:
	-	`sha256:462519a6a1755237bf46e1f96ab675d3615d2ed4d23deac96faf17e878615c8c`  
		Last Modified: Fri, 14 Nov 2025 18:07:52 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9009a0bbad1078191e0b701bba772bfaf33f06c4aeabd0c88847cd12e27bb2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70238617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47e3268b71de1f8d2b3f16253789c894ccb5c517327e000fe4f04b56b4a700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6c4b38a379125c5a42c9424120314522bbc3c2207ec499983e38878b7fdab640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a750656c16998bce5538dc78fb7d4ee4a8651174daaa388d58a43742ed6c3b`

```dockerfile
```

-	Layers:
	-	`sha256:bd54fcfe11ce172467cf267a5b45ac604e052195b987a6ae1c5642e94d12397e`  
		Last Modified: Fri, 14 Nov 2025 18:07:55 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.1-cli-alpine3.22`

```console
$ docker pull docker@sha256:f7d048590d889e00868920f658e807ecbc4ef662d51c9af67eb5534a447d58d6
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

### `docker:29.0.1-cli-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:b7941b2ccd806a2c6a86a9358773aa88b14b7917ed8a22af6147b1eac167ea37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75444849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5610201729349c6a70dcb8338e5ec33e1443f2a4b390f2ace27c542e2a6551f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6639e11997628dd93c3b8971e3df09ddec13aa1090dc25e18cfd82700144c51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c10f48a4154ccf09427898d95780e35a51b74f0b0868fdf8bf3914dd5e150a7`

```dockerfile
```

-	Layers:
	-	`sha256:5acd60ebabd269e3bf29e690ffb732d33fc40c5b1d23c927a1bd86937a022403`  
		Last Modified: Fri, 14 Nov 2025 18:07:45 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:de3b12999906ced6af004389ff60e8d522230851392fd1d98c2f4b1d3a3d7aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71155509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6227483b507c988892ab228db7529b849e20aaf937ee76232ab743e0ce2382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:9a87490926570243a4d251dae8b8f569662ae5af2de5025d53a42d0d08d0b913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7ce2655c6bf1df9638a7a64d777afe8ed589e15bc4098a644382eeed483709`

```dockerfile
```

-	Layers:
	-	`sha256:3ff99371b5cd8e73694b7d6b254cf527f48f5f727a79d676088cccb0830d0c89`  
		Last Modified: Fri, 14 Nov 2025 18:07:48 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:76c19db0b5751c3df03c26f0ce3ce68ab059831cb81e504f8134059758b7f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4abaf932f47f68cd8df61080df26ae2934afa32af1ef9b0199884a9b3f6ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:0890e3f571d08c5d82e6a43cf4c59460170ceb9b1ff8421ea78ff9e5276788f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5368d0b81e1020cfbb376075883e1424d7ea529a38d09e4c5f6180d1ea0ee`

```dockerfile
```

-	Layers:
	-	`sha256:462519a6a1755237bf46e1f96ab675d3615d2ed4d23deac96faf17e878615c8c`  
		Last Modified: Fri, 14 Nov 2025 18:07:52 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9009a0bbad1078191e0b701bba772bfaf33f06c4aeabd0c88847cd12e27bb2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70238617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47e3268b71de1f8d2b3f16253789c894ccb5c517327e000fe4f04b56b4a700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6c4b38a379125c5a42c9424120314522bbc3c2207ec499983e38878b7fdab640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a750656c16998bce5538dc78fb7d4ee4a8651174daaa388d58a43742ed6c3b`

```dockerfile
```

-	Layers:
	-	`sha256:bd54fcfe11ce172467cf267a5b45ac604e052195b987a6ae1c5642e94d12397e`  
		Last Modified: Fri, 14 Nov 2025 18:07:55 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.1-dind`

```console
$ docker pull docker@sha256:ecac43e78380d9b9d3bd24f0ab42b370f6391a1a06a66065c10a00b9d6d57a3e
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

### `docker:29.0.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:00132b42611695f0faa1ba618a46322d4ed1820196d32aa154fec32c5cb68c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144707841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b2800307a6faea084b98527766ebdf588066f1b012b87b85cd1ef067b8e31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6fbc20d0499ae60106d5f9b49eceff31343edb8aeac3e92d63203c5d3e84f0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c5c4870972a290b16e151e59a4ac0bed7fb1a544bf966055722b1da4a48174`

```dockerfile
```

-	Layers:
	-	`sha256:8382ae4791ce77e8d80f8c180eeaf4dd13717d4fffd7461872d306908ea90568`  
		Last Modified: Fri, 14 Nov 2025 21:07:32 GMT  
		Size: 34.5 KB (34546 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:e114c1871f88412b0af04436a04da150d52fc3b5338c2c9ab6376e17c150ae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136708410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff51ffa9f6c0e603f3cd4870105c3dfa12a3d43a4b7b011894d65e2e1b0314`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fbb9ab3af5e33bbb16665bd4743801e4c0bc0edf8f15d1f24ac3b873ef9cf9`  
		Last Modified: Fri, 14 Nov 2025 17:50:53 GMT  
		Size: 7.2 MB (7230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d9ee37936557e5e5e7ec317e4534765b3c8172adc5bf93a17c6e62f4b0274`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 89.9 KB (89945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c77cfca9a877080e55292eefd2344aeca081c4265ac88d3f9788851fff4200`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f622ba6a998ec6a0e7441faff66535b0b237b7dd9e99eb0e2f6a26858913ff1`  
		Last Modified: Fri, 14 Nov 2025 17:50:57 GMT  
		Size: 58.2 MB (58226630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f54398961fe271418301e8dcae9e53f00d878b96f8a8377091a69cbb0a7fb`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03f31f2f2fbd5b1caf9390b89a591da2910325080ba25bf25fd34ad8f0a62c`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:92fb4cbe157b467796f3d3ff5a3e62a203de5b795996de10ade617404f1785dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff33814f2f295e159bd1f54fa696c6153b59888521a92bec74e8295bffe608`

```dockerfile
```

-	Layers:
	-	`sha256:382fff29d9320a2efad79391da82c3dc51464c69bab0602636a5506caed19263`  
		Last Modified: Fri, 14 Nov 2025 21:07:36 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:886e5ff459e6f6be26b7484994a8d14bebe4fab3ec9529c371290b026424424e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134835020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7491f7a31f2d5b452a5789d3b65287a5ca38f7662974f31846039905736fb6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:51:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:51:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:51:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:51:12 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c2cd84bc928c20d117c9d7635a90a39831b95e8052dff3cfe3cc1bd6f0f00`  
		Last Modified: Fri, 14 Nov 2025 17:51:33 GMT  
		Size: 6.5 MB (6538247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8831271b0fde493256cfdf625b8bd29b593b50a2e41b876bd0457c205d31e`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 86.4 KB (86382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71ccd6132c6fd73522dcd76d0bb847633486222624334da36abd2c47430fd8`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2cd691ecedb982457a39c51d8021b1c4d0b9f32c50a0a5577a9fb86883015`  
		Last Modified: Fri, 14 Nov 2025 17:51:44 GMT  
		Size: 58.1 MB (58057973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1737b7d7aac53a596ec07e87ad0b783fef1583571ae58abb857a9f11b74dd5`  
		Last Modified: Fri, 14 Nov 2025 17:51:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b20a0a6faa25f08f3ed0f08d263f46cb718486a08e704ddd3db37a2f2ea5c`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:dd6b3fe3ba751f84e6dc47893d9fe7c3bd957326add76df24fb78fbf62430bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84995271acd51564889fcdb02992d8357b44c462262206e8359b295681d6d28`

```dockerfile
```

-	Layers:
	-	`sha256:69aedff7fce428d6fcf857b03c5f072505dac8dfe9a5cadb00d593c5c93d786d`  
		Last Modified: Fri, 14 Nov 2025 21:07:39 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bb993f24897a54351c5acb5d769b63d0108e0e786677f633c8d4458716100082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133979082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ed8a923f13f7602e40108a5b68dc701a9d2393812f9ae77eecc3604d129c0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3a293b40e13f7427b260b7b7f470a8b7265cdcc61e7dd66bf7aaf7f439a4382a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899d225e33fad6679da89493be4274ee067b3b9389d791946d24d2c5a59bcd04`

```dockerfile
```

-	Layers:
	-	`sha256:a46ef6333945bb9c7c1c75266c56c269547f0646013eb229d5855f9fbcac81d4`  
		Last Modified: Fri, 14 Nov 2025 21:07:42 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.1-dind-alpine3.22`

```console
$ docker pull docker@sha256:ecac43e78380d9b9d3bd24f0ab42b370f6391a1a06a66065c10a00b9d6d57a3e
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

### `docker:29.0.1-dind-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:00132b42611695f0faa1ba618a46322d4ed1820196d32aa154fec32c5cb68c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144707841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b2800307a6faea084b98527766ebdf588066f1b012b87b85cd1ef067b8e31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:6fbc20d0499ae60106d5f9b49eceff31343edb8aeac3e92d63203c5d3e84f0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c5c4870972a290b16e151e59a4ac0bed7fb1a544bf966055722b1da4a48174`

```dockerfile
```

-	Layers:
	-	`sha256:8382ae4791ce77e8d80f8c180eeaf4dd13717d4fffd7461872d306908ea90568`  
		Last Modified: Fri, 14 Nov 2025 21:07:32 GMT  
		Size: 34.5 KB (34546 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-dind-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:e114c1871f88412b0af04436a04da150d52fc3b5338c2c9ab6376e17c150ae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136708410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff51ffa9f6c0e603f3cd4870105c3dfa12a3d43a4b7b011894d65e2e1b0314`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fbb9ab3af5e33bbb16665bd4743801e4c0bc0edf8f15d1f24ac3b873ef9cf9`  
		Last Modified: Fri, 14 Nov 2025 17:50:53 GMT  
		Size: 7.2 MB (7230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d9ee37936557e5e5e7ec317e4534765b3c8172adc5bf93a17c6e62f4b0274`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 89.9 KB (89945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c77cfca9a877080e55292eefd2344aeca081c4265ac88d3f9788851fff4200`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f622ba6a998ec6a0e7441faff66535b0b237b7dd9e99eb0e2f6a26858913ff1`  
		Last Modified: Fri, 14 Nov 2025 17:50:57 GMT  
		Size: 58.2 MB (58226630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f54398961fe271418301e8dcae9e53f00d878b96f8a8377091a69cbb0a7fb`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03f31f2f2fbd5b1caf9390b89a591da2910325080ba25bf25fd34ad8f0a62c`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:92fb4cbe157b467796f3d3ff5a3e62a203de5b795996de10ade617404f1785dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff33814f2f295e159bd1f54fa696c6153b59888521a92bec74e8295bffe608`

```dockerfile
```

-	Layers:
	-	`sha256:382fff29d9320a2efad79391da82c3dc51464c69bab0602636a5506caed19263`  
		Last Modified: Fri, 14 Nov 2025 21:07:36 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-dind-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:886e5ff459e6f6be26b7484994a8d14bebe4fab3ec9529c371290b026424424e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134835020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7491f7a31f2d5b452a5789d3b65287a5ca38f7662974f31846039905736fb6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:51:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:51:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:51:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:51:12 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c2cd84bc928c20d117c9d7635a90a39831b95e8052dff3cfe3cc1bd6f0f00`  
		Last Modified: Fri, 14 Nov 2025 17:51:33 GMT  
		Size: 6.5 MB (6538247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8831271b0fde493256cfdf625b8bd29b593b50a2e41b876bd0457c205d31e`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 86.4 KB (86382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71ccd6132c6fd73522dcd76d0bb847633486222624334da36abd2c47430fd8`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2cd691ecedb982457a39c51d8021b1c4d0b9f32c50a0a5577a9fb86883015`  
		Last Modified: Fri, 14 Nov 2025 17:51:44 GMT  
		Size: 58.1 MB (58057973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1737b7d7aac53a596ec07e87ad0b783fef1583571ae58abb857a9f11b74dd5`  
		Last Modified: Fri, 14 Nov 2025 17:51:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b20a0a6faa25f08f3ed0f08d263f46cb718486a08e704ddd3db37a2f2ea5c`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:dd6b3fe3ba751f84e6dc47893d9fe7c3bd957326add76df24fb78fbf62430bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84995271acd51564889fcdb02992d8357b44c462262206e8359b295681d6d28`

```dockerfile
```

-	Layers:
	-	`sha256:69aedff7fce428d6fcf857b03c5f072505dac8dfe9a5cadb00d593c5c93d786d`  
		Last Modified: Fri, 14 Nov 2025 21:07:39 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-dind-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bb993f24897a54351c5acb5d769b63d0108e0e786677f633c8d4458716100082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133979082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ed8a923f13f7602e40108a5b68dc701a9d2393812f9ae77eecc3604d129c0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:3a293b40e13f7427b260b7b7f470a8b7265cdcc61e7dd66bf7aaf7f439a4382a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899d225e33fad6679da89493be4274ee067b3b9389d791946d24d2c5a59bcd04`

```dockerfile
```

-	Layers:
	-	`sha256:a46ef6333945bb9c7c1c75266c56c269547f0646013eb229d5855f9fbcac81d4`  
		Last Modified: Fri, 14 Nov 2025 21:07:42 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.1-dind-rootless`

```console
$ docker pull docker@sha256:b924e5892d5aefa030d9892dbc3b85db67df24d59cf946ec7e725190c1691abd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.0.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6d29b486c85d77265cc4257132508b1a86cc3cfdc2de452344afe2c234b80a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165477802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8fc7fc34477348a244b0a621318f684459f4424c2943f4ee9cbf5abce99b89`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
# Fri, 14 Nov 2025 18:10:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 14 Nov 2025 18:10:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 14 Nov 2025 18:10:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 18:10:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 14 Nov 2025 18:10:19 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 14 Nov 2025 18:10:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 14 Nov 2025 18:10:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513878b9b4e4da83bfc8de704ddf45706f0b62a2356479af219df01188ff8a48`  
		Last Modified: Fri, 14 Nov 2025 18:10:57 GMT  
		Size: 3.4 MB (3398381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e4a8852507263a81dcd77f93d54cf66f47d8ed89c986713a9dcd74981dd3e`  
		Last Modified: Fri, 14 Nov 2025 18:10:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d074650f9e9d1dac92ea2f4c7d1026952927f1ba97c8894a1bb156a5ff9653b0`  
		Last Modified: Fri, 14 Nov 2025 18:10:56 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63526e8c52dd76c90d0e3a0e6bb13b19cda2d1ff9446b85ab9132f2fb16f78fe`  
		Last Modified: Fri, 14 Nov 2025 18:10:58 GMT  
		Size: 17.4 MB (17370238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562df067ff8bc7659a7875734d42d697ffdf76e4bed8078800e7da4e2424bbe2`  
		Last Modified: Fri, 14 Nov 2025 18:10:56 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6ec58b7f35d8d3e7f65f422c3f2833c7d6f44e72c2849305ee87a57e8f089e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223534bdcc7c40e6963d71184880072aa2eece4cb8e11d03104e7a28c4135421`

```dockerfile
```

-	Layers:
	-	`sha256:7dbc601a6f7d05ebcb9447d304eadddf1015d62e57449b3c6e86b44a9adb8c62`  
		Last Modified: Fri, 14 Nov 2025 21:07:46 GMT  
		Size: 30.6 KB (30592 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.0.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bfdf109fce0ab0fd0ba42be00451d4fb714b734228858302df9768ac6d3362a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155077380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4180e8a9ce1e43c5e639c274361cb08943b78c10c5393b47b2d71f64ea48c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
# Fri, 14 Nov 2025 18:10:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 14 Nov 2025 18:10:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 14 Nov 2025 18:10:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 18:10:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 14 Nov 2025 18:10:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 14 Nov 2025 18:10:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 14 Nov 2025 18:10:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f62158be363aa14485e96848a8b96cf255e073d928be7dc5c69b46f65eb6b5b`  
		Last Modified: Fri, 14 Nov 2025 18:11:03 GMT  
		Size: 3.4 MB (3389927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5364fd5d0f73f66aa1d964ede207f062a9e616e6b42830c1f3a166ba5fb2b49`  
		Last Modified: Fri, 14 Nov 2025 18:11:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fc17712e26dd00dc065701746564366ae6b8183f29fe9c0c6856333df3b594`  
		Last Modified: Fri, 14 Nov 2025 18:11:02 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8bd711987f26afa49fcadbe781f8c6847149015fa8e1082e4ad27d1da8d2a5`  
		Last Modified: Fri, 14 Nov 2025 18:11:06 GMT  
		Size: 17.7 MB (17707029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de028bc8dfab27deee2ca498a1190fc9f027027916111582fa052454d71bf0cb`  
		Last Modified: Fri, 14 Nov 2025 18:11:02 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.0.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1f4e1b86ed838a0859f42489582c015f364311d5ab510c177b4f7930bf040383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9f9d5aa17326ac7fd25ef8e86d235ffcad8dfa411e3ba9a78f7af36845b2be`

```dockerfile
```

-	Layers:
	-	`sha256:74d0c86fb00bbe1231f84c463b2af685b2865334e1dab867c70df0d69ea4306f`  
		Last Modified: Fri, 14 Nov 2025 21:07:49 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.0.1-windowsservercore`

```console
$ docker pull docker@sha256:772aaec5cedd47b99353c76851734473b2724c7cc430b0fcbc882c7246678b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:29.0.1-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:d4513656969f64c32a00ba744aa13642743751db9b7c2442493cff588fc97517
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1502f96214ca8b767265c2d1cf293ea85c27f0044acac3a5151b1c12e3ddc303`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Fri, 14 Nov 2025 17:55:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:55:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:55:41 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:55:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:55:54 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:56:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:56:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:56:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec8692dea2a7cfeb5456bb4b993de15f76c88f0be36ba06ff89c73fa28bd532`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3756c030c25ee9a0352e8d184c9972ad760203435a360f95000a3a9ea1483db5`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 369.1 KB (369110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438ea9e974311c3c3b6d58a49066378843912aecbb7cd0fb7d961e9c3854e226`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2397c1b0ac14feac44b1a8573714b74ed790b8508fb19c11a9d63dd27536c8d`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720e07e14cdad776989cc5b530a376ed2a8777fccbfd9e9f7d1c5e4f3159c198`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 19.4 MB (19418477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d75632fe4f81ec2a724f6cac9e1e96aa25cc0d69a55177dfc00fca22150e42`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb681c47e552d8f90a197e832ece2f5a916389ce91d7dcce373001a0cacf717`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d5289b2e911e0436443f61b478f4e7ea8fb47b49ca4f0b08c023964a93a67f`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3e80662571ee22f6f212588ff170fc2f9d03dfaf33c2ae73ac2de62dcafc55`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 23.9 MB (23922840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2d5545093c2c4372e7e37e9ffc58230f3166f4eacf2d4af33f7699bf03a4b3`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c9f72fd0ce28cce8b61e2e5039431d3b23df93018467b52b2668516b0aafc9`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbbff8fd62b3ff3bfc919aaad4ac8af852c56c386751789d24f339adc0282d0`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba18e5c2618956fa6278331e4654b4726703ba698d344205e51bca5670237e5b`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 22.7 MB (22671713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.0.1-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:abaa83761c38ffb230bcb50a1d39744533e9666965018cfa825b0eec05f8112e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836498567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21dfcb808df45545b0f05343454835ed030e1c989ec55b3d4f578ef9de30d1e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Fri, 14 Nov 2025 17:46:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:46:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:46:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:47:22 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:47:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:47:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:47:49 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:48:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6703b96ff9900204410d0399df239a7cabe4d5e73c952ec996266a8f45346`  
		Last Modified: Fri, 14 Nov 2025 17:56:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32feda2f6f8207494b3c9e9732ebb1862d3785b36a3e4525af2de8874ba5eee7`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 502.3 KB (502252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f8d186086c63ae6514fab9464ed5b6e84edc42d0f18d1c630bbfe43e115fef`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13d933136eb971ad9c95a6de8745441fa2624b2a27cfd060f8b3258851fe2`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8456085a802821a6c35870bb91704666a064351f24ebd7e591d39d0309f0839c`  
		Last Modified: Fri, 14 Nov 2025 17:56:41 GMT  
		Size: 19.4 MB (19420220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23228b265c8267351c3b090a7093eb367490e0702e3cb7cf5250970db0258a37`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b082f0bb7964878d7ab22207b5df4f055bfc7aa97819cc449f4d8d423b919bf2`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50ae099af18d834feac25c9900b0891a0109fb464ad8f58464aaa84dcdbc161`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a569077549ea2a7f686bf31019da93372c4d61bbfe68f9bd66f6c9b367cadce7`  
		Last Modified: Fri, 14 Nov 2025 17:56:42 GMT  
		Size: 23.9 MB (23925706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44babfbf95d13b45d09fd0e43b38bbd485fa8ceb0686cc0d6ab0d3c532121f6`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcda35700f9ec33e4f5daa7429fc8ee77d4b076e14c0f0abbade72372e0832c4`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a58f8f0d06a0c8958d452e24c82a314e37348a63b44db70f1bbb741e7727863`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69feff69baaaa2240d3c0bcddf4d4c711f13550cbc03ad8307b009d44ea6a26`  
		Last Modified: Fri, 14 Nov 2025 17:56:40 GMT  
		Size: 22.7 MB (22677039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:43bb8e65e5e41a0bee0bea69e5cc5b33d765055b0de0b6bc9584152cf3cbfdfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:29.0.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:abaa83761c38ffb230bcb50a1d39744533e9666965018cfa825b0eec05f8112e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836498567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21dfcb808df45545b0f05343454835ed030e1c989ec55b3d4f578ef9de30d1e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Fri, 14 Nov 2025 17:46:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:46:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:46:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:47:22 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:47:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:47:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:47:49 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:48:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6703b96ff9900204410d0399df239a7cabe4d5e73c952ec996266a8f45346`  
		Last Modified: Fri, 14 Nov 2025 17:56:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32feda2f6f8207494b3c9e9732ebb1862d3785b36a3e4525af2de8874ba5eee7`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 502.3 KB (502252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f8d186086c63ae6514fab9464ed5b6e84edc42d0f18d1c630bbfe43e115fef`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13d933136eb971ad9c95a6de8745441fa2624b2a27cfd060f8b3258851fe2`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8456085a802821a6c35870bb91704666a064351f24ebd7e591d39d0309f0839c`  
		Last Modified: Fri, 14 Nov 2025 17:56:41 GMT  
		Size: 19.4 MB (19420220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23228b265c8267351c3b090a7093eb367490e0702e3cb7cf5250970db0258a37`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b082f0bb7964878d7ab22207b5df4f055bfc7aa97819cc449f4d8d423b919bf2`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50ae099af18d834feac25c9900b0891a0109fb464ad8f58464aaa84dcdbc161`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a569077549ea2a7f686bf31019da93372c4d61bbfe68f9bd66f6c9b367cadce7`  
		Last Modified: Fri, 14 Nov 2025 17:56:42 GMT  
		Size: 23.9 MB (23925706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44babfbf95d13b45d09fd0e43b38bbd485fa8ceb0686cc0d6ab0d3c532121f6`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcda35700f9ec33e4f5daa7429fc8ee77d4b076e14c0f0abbade72372e0832c4`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a58f8f0d06a0c8958d452e24c82a314e37348a63b44db70f1bbb741e7727863`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69feff69baaaa2240d3c0bcddf4d4c711f13550cbc03ad8307b009d44ea6a26`  
		Last Modified: Fri, 14 Nov 2025 17:56:40 GMT  
		Size: 22.7 MB (22677039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.0.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:3d255dbdfb3cd84597679d5d3ca0b4a9eba95cd13ee76c69e3ed677b0d2c8406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:29.0.1-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:d4513656969f64c32a00ba744aa13642743751db9b7c2442493cff588fc97517
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1502f96214ca8b767265c2d1cf293ea85c27f0044acac3a5151b1c12e3ddc303`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Fri, 14 Nov 2025 17:55:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:55:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:55:41 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:55:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:55:54 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:56:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:56:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:56:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec8692dea2a7cfeb5456bb4b993de15f76c88f0be36ba06ff89c73fa28bd532`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3756c030c25ee9a0352e8d184c9972ad760203435a360f95000a3a9ea1483db5`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 369.1 KB (369110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438ea9e974311c3c3b6d58a49066378843912aecbb7cd0fb7d961e9c3854e226`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2397c1b0ac14feac44b1a8573714b74ed790b8508fb19c11a9d63dd27536c8d`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720e07e14cdad776989cc5b530a376ed2a8777fccbfd9e9f7d1c5e4f3159c198`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 19.4 MB (19418477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d75632fe4f81ec2a724f6cac9e1e96aa25cc0d69a55177dfc00fca22150e42`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb681c47e552d8f90a197e832ece2f5a916389ce91d7dcce373001a0cacf717`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d5289b2e911e0436443f61b478f4e7ea8fb47b49ca4f0b08c023964a93a67f`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3e80662571ee22f6f212588ff170fc2f9d03dfaf33c2ae73ac2de62dcafc55`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 23.9 MB (23922840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2d5545093c2c4372e7e37e9ffc58230f3166f4eacf2d4af33f7699bf03a4b3`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c9f72fd0ce28cce8b61e2e5039431d3b23df93018467b52b2668516b0aafc9`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbbff8fd62b3ff3bfc919aaad4ac8af852c56c386751789d24f339adc0282d0`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba18e5c2618956fa6278331e4654b4726703ba698d344205e51bca5670237e5b`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 22.7 MB (22671713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:f7d048590d889e00868920f658e807ecbc4ef662d51c9af67eb5534a447d58d6
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
$ docker pull docker@sha256:b7941b2ccd806a2c6a86a9358773aa88b14b7917ed8a22af6147b1eac167ea37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75444849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5610201729349c6a70dcb8338e5ec33e1443f2a4b390f2ace27c542e2a6551f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6639e11997628dd93c3b8971e3df09ddec13aa1090dc25e18cfd82700144c51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c10f48a4154ccf09427898d95780e35a51b74f0b0868fdf8bf3914dd5e150a7`

```dockerfile
```

-	Layers:
	-	`sha256:5acd60ebabd269e3bf29e690ffb732d33fc40c5b1d23c927a1bd86937a022403`  
		Last Modified: Fri, 14 Nov 2025 18:07:45 GMT  
		Size: 38.1 KB (38073 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:de3b12999906ced6af004389ff60e8d522230851392fd1d98c2f4b1d3a3d7aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71155509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6227483b507c988892ab228db7529b849e20aaf937ee76232ab743e0ce2382`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:9a87490926570243a4d251dae8b8f569662ae5af2de5025d53a42d0d08d0b913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7ce2655c6bf1df9638a7a64d777afe8ed589e15bc4098a644382eeed483709`

```dockerfile
```

-	Layers:
	-	`sha256:3ff99371b5cd8e73694b7d6b254cf527f48f5f727a79d676088cccb0830d0c89`  
		Last Modified: Fri, 14 Nov 2025 18:07:48 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:76c19db0b5751c3df03c26f0ce3ce68ab059831cb81e504f8134059758b7f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70146419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a4abaf932f47f68cd8df61080df26ae2934afa32af1ef9b0199884a9b3f6ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:0890e3f571d08c5d82e6a43cf4c59460170ceb9b1ff8421ea78ff9e5276788f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5368d0b81e1020cfbb376075883e1424d7ea529a38d09e4c5f6180d1ea0ee`

```dockerfile
```

-	Layers:
	-	`sha256:462519a6a1755237bf46e1f96ab675d3615d2ed4d23deac96faf17e878615c8c`  
		Last Modified: Fri, 14 Nov 2025 18:07:52 GMT  
		Size: 38.2 KB (38239 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9009a0bbad1078191e0b701bba772bfaf33f06c4aeabd0c88847cd12e27bb2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70238617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47e3268b71de1f8d2b3f16253789c894ccb5c517327e000fe4f04b56b4a700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6c4b38a379125c5a42c9424120314522bbc3c2207ec499983e38878b7fdab640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a750656c16998bce5538dc78fb7d4ee4a8651174daaa388d58a43742ed6c3b`

```dockerfile
```

-	Layers:
	-	`sha256:bd54fcfe11ce172467cf267a5b45ac604e052195b987a6ae1c5642e94d12397e`  
		Last Modified: Fri, 14 Nov 2025 18:07:55 GMT  
		Size: 38.3 KB (38279 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:ecac43e78380d9b9d3bd24f0ab42b370f6391a1a06a66065c10a00b9d6d57a3e
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
$ docker pull docker@sha256:00132b42611695f0faa1ba618a46322d4ed1820196d32aa154fec32c5cb68c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144707841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b2800307a6faea084b98527766ebdf588066f1b012b87b85cd1ef067b8e31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:6fbc20d0499ae60106d5f9b49eceff31343edb8aeac3e92d63203c5d3e84f0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c5c4870972a290b16e151e59a4ac0bed7fb1a544bf966055722b1da4a48174`

```dockerfile
```

-	Layers:
	-	`sha256:8382ae4791ce77e8d80f8c180eeaf4dd13717d4fffd7461872d306908ea90568`  
		Last Modified: Fri, 14 Nov 2025 21:07:32 GMT  
		Size: 34.5 KB (34546 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:e114c1871f88412b0af04436a04da150d52fc3b5338c2c9ab6376e17c150ae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136708410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff51ffa9f6c0e603f3cd4870105c3dfa12a3d43a4b7b011894d65e2e1b0314`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fbb9ab3af5e33bbb16665bd4743801e4c0bc0edf8f15d1f24ac3b873ef9cf9`  
		Last Modified: Fri, 14 Nov 2025 17:50:53 GMT  
		Size: 7.2 MB (7230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d9ee37936557e5e5e7ec317e4534765b3c8172adc5bf93a17c6e62f4b0274`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 89.9 KB (89945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c77cfca9a877080e55292eefd2344aeca081c4265ac88d3f9788851fff4200`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f622ba6a998ec6a0e7441faff66535b0b237b7dd9e99eb0e2f6a26858913ff1`  
		Last Modified: Fri, 14 Nov 2025 17:50:57 GMT  
		Size: 58.2 MB (58226630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f54398961fe271418301e8dcae9e53f00d878b96f8a8377091a69cbb0a7fb`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03f31f2f2fbd5b1caf9390b89a591da2910325080ba25bf25fd34ad8f0a62c`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:92fb4cbe157b467796f3d3ff5a3e62a203de5b795996de10ade617404f1785dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff33814f2f295e159bd1f54fa696c6153b59888521a92bec74e8295bffe608`

```dockerfile
```

-	Layers:
	-	`sha256:382fff29d9320a2efad79391da82c3dc51464c69bab0602636a5506caed19263`  
		Last Modified: Fri, 14 Nov 2025 21:07:36 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:886e5ff459e6f6be26b7484994a8d14bebe4fab3ec9529c371290b026424424e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134835020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7491f7a31f2d5b452a5789d3b65287a5ca38f7662974f31846039905736fb6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:51:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:51:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:51:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:51:12 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c2cd84bc928c20d117c9d7635a90a39831b95e8052dff3cfe3cc1bd6f0f00`  
		Last Modified: Fri, 14 Nov 2025 17:51:33 GMT  
		Size: 6.5 MB (6538247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8831271b0fde493256cfdf625b8bd29b593b50a2e41b876bd0457c205d31e`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 86.4 KB (86382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71ccd6132c6fd73522dcd76d0bb847633486222624334da36abd2c47430fd8`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2cd691ecedb982457a39c51d8021b1c4d0b9f32c50a0a5577a9fb86883015`  
		Last Modified: Fri, 14 Nov 2025 17:51:44 GMT  
		Size: 58.1 MB (58057973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1737b7d7aac53a596ec07e87ad0b783fef1583571ae58abb857a9f11b74dd5`  
		Last Modified: Fri, 14 Nov 2025 17:51:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b20a0a6faa25f08f3ed0f08d263f46cb718486a08e704ddd3db37a2f2ea5c`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:dd6b3fe3ba751f84e6dc47893d9fe7c3bd957326add76df24fb78fbf62430bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84995271acd51564889fcdb02992d8357b44c462262206e8359b295681d6d28`

```dockerfile
```

-	Layers:
	-	`sha256:69aedff7fce428d6fcf857b03c5f072505dac8dfe9a5cadb00d593c5c93d786d`  
		Last Modified: Fri, 14 Nov 2025 21:07:39 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bb993f24897a54351c5acb5d769b63d0108e0e786677f633c8d4458716100082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133979082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ed8a923f13f7602e40108a5b68dc701a9d2393812f9ae77eecc3604d129c0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:3a293b40e13f7427b260b7b7f470a8b7265cdcc61e7dd66bf7aaf7f439a4382a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899d225e33fad6679da89493be4274ee067b3b9389d791946d24d2c5a59bcd04`

```dockerfile
```

-	Layers:
	-	`sha256:a46ef6333945bb9c7c1c75266c56c269547f0646013eb229d5855f9fbcac81d4`  
		Last Modified: Fri, 14 Nov 2025 21:07:42 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:b924e5892d5aefa030d9892dbc3b85db67df24d59cf946ec7e725190c1691abd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6d29b486c85d77265cc4257132508b1a86cc3cfdc2de452344afe2c234b80a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165477802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8fc7fc34477348a244b0a621318f684459f4424c2943f4ee9cbf5abce99b89`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
# Fri, 14 Nov 2025 18:10:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 14 Nov 2025 18:10:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 14 Nov 2025 18:10:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 18:10:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 14 Nov 2025 18:10:19 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 14 Nov 2025 18:10:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 14 Nov 2025 18:10:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513878b9b4e4da83bfc8de704ddf45706f0b62a2356479af219df01188ff8a48`  
		Last Modified: Fri, 14 Nov 2025 18:10:57 GMT  
		Size: 3.4 MB (3398381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e4a8852507263a81dcd77f93d54cf66f47d8ed89c986713a9dcd74981dd3e`  
		Last Modified: Fri, 14 Nov 2025 18:10:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d074650f9e9d1dac92ea2f4c7d1026952927f1ba97c8894a1bb156a5ff9653b0`  
		Last Modified: Fri, 14 Nov 2025 18:10:56 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63526e8c52dd76c90d0e3a0e6bb13b19cda2d1ff9446b85ab9132f2fb16f78fe`  
		Last Modified: Fri, 14 Nov 2025 18:10:58 GMT  
		Size: 17.4 MB (17370238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562df067ff8bc7659a7875734d42d697ffdf76e4bed8078800e7da4e2424bbe2`  
		Last Modified: Fri, 14 Nov 2025 18:10:56 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6ec58b7f35d8d3e7f65f422c3f2833c7d6f44e72c2849305ee87a57e8f089e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223534bdcc7c40e6963d71184880072aa2eece4cb8e11d03104e7a28c4135421`

```dockerfile
```

-	Layers:
	-	`sha256:7dbc601a6f7d05ebcb9447d304eadddf1015d62e57449b3c6e86b44a9adb8c62`  
		Last Modified: Fri, 14 Nov 2025 21:07:46 GMT  
		Size: 30.6 KB (30592 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bfdf109fce0ab0fd0ba42be00451d4fb714b734228858302df9768ac6d3362a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155077380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4180e8a9ce1e43c5e639c274361cb08943b78c10c5393b47b2d71f64ea48c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
# Fri, 14 Nov 2025 18:10:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 14 Nov 2025 18:10:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 14 Nov 2025 18:10:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 18:10:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 14 Nov 2025 18:10:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 14 Nov 2025 18:10:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 14 Nov 2025 18:10:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f62158be363aa14485e96848a8b96cf255e073d928be7dc5c69b46f65eb6b5b`  
		Last Modified: Fri, 14 Nov 2025 18:11:03 GMT  
		Size: 3.4 MB (3389927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5364fd5d0f73f66aa1d964ede207f062a9e616e6b42830c1f3a166ba5fb2b49`  
		Last Modified: Fri, 14 Nov 2025 18:11:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fc17712e26dd00dc065701746564366ae6b8183f29fe9c0c6856333df3b594`  
		Last Modified: Fri, 14 Nov 2025 18:11:02 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8bd711987f26afa49fcadbe781f8c6847149015fa8e1082e4ad27d1da8d2a5`  
		Last Modified: Fri, 14 Nov 2025 18:11:06 GMT  
		Size: 17.7 MB (17707029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de028bc8dfab27deee2ca498a1190fc9f027027916111582fa052454d71bf0cb`  
		Last Modified: Fri, 14 Nov 2025 18:11:02 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1f4e1b86ed838a0859f42489582c015f364311d5ab510c177b4f7930bf040383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9f9d5aa17326ac7fd25ef8e86d235ffcad8dfa411e3ba9a78f7af36845b2be`

```dockerfile
```

-	Layers:
	-	`sha256:74d0c86fb00bbe1231f84c463b2af685b2865334e1dab867c70df0d69ea4306f`  
		Last Modified: Fri, 14 Nov 2025 21:07:49 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:ecac43e78380d9b9d3bd24f0ab42b370f6391a1a06a66065c10a00b9d6d57a3e
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
$ docker pull docker@sha256:00132b42611695f0faa1ba618a46322d4ed1820196d32aa154fec32c5cb68c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144707841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b2800307a6faea084b98527766ebdf588066f1b012b87b85cd1ef067b8e31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:47:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:47:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:47:57 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:47:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:48:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:48:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:48:00 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:56 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:56 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6ab7e708057f8066f62894c2526c969d7908c9af1271fb76b800c98958762`  
		Last Modified: Fri, 14 Nov 2025 17:48:18 GMT  
		Size: 8.2 MB (8232204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becc0e8e7d9129df5671ccf1cffa7b902cc0eedf559ae1ca40ddc38a7dbab23a`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1aa4a8bbec6de26269522a18d2e6229033f3d14bbfc0bfc588a570540429c`  
		Last Modified: Fri, 14 Nov 2025 17:48:19 GMT  
		Size: 18.8 MB (18757664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d2e68783fb41d80f2148d0bd29af26c6982d008aee3ea361c66b2c54f51200`  
		Last Modified: Fri, 14 Nov 2025 17:48:21 GMT  
		Size: 22.9 MB (22906099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ced36844c2c2d3209f65f843e7aa407c719097959e5167895e20e02079622`  
		Last Modified: Fri, 14 Nov 2025 17:48:20 GMT  
		Size: 21.7 MB (21744276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955e16fe8d1775af15245f4d1a81e938b990b5f86f2bc5196059809669ff898`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fec51a8530d0418c30de8dc3810578adc62d0890d4e9b3a5e731ee4b5cb46c`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6dd2655b8a42d1dd6c3caebaaf54298080002e3358f70c614696fa01c515c5`  
		Last Modified: Fri, 14 Nov 2025 17:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836285adbc1f8518fb3fc58f344990245405c4090bb218e47bae9f93c4fc6f8`  
		Last Modified: Fri, 14 Nov 2025 17:51:15 GMT  
		Size: 6.9 MB (6905408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d14094b040cbd5fcf1eb75c81e76084496e158dc0ee5efb3881cd9523b062`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 90.4 KB (90382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7814a8057ef7577c878fc0f55ceca04809949f65a0077398caaad49d47c0f3a`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4480e986d92de5de07b2d92e86b291d02b07b0ea4312cc25addc7d8f85f09`  
		Last Modified: Fri, 14 Nov 2025 17:51:19 GMT  
		Size: 62.3 MB (62261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e000f30dc3b3dc0f7b95ea417b8bee78256988c4afd97524f4e6f0551a7c9`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f20f37038c98785f81f9897b0f260da3efd2d8845f5edf70961489e2e356d4d`  
		Last Modified: Fri, 14 Nov 2025 17:51:14 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:6fbc20d0499ae60106d5f9b49eceff31343edb8aeac3e92d63203c5d3e84f0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c5c4870972a290b16e151e59a4ac0bed7fb1a544bf966055722b1da4a48174`

```dockerfile
```

-	Layers:
	-	`sha256:8382ae4791ce77e8d80f8c180eeaf4dd13717d4fffd7461872d306908ea90568`  
		Last Modified: Fri, 14 Nov 2025 21:07:32 GMT  
		Size: 34.5 KB (34546 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:e114c1871f88412b0af04436a04da150d52fc3b5338c2c9ab6376e17c150ae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136708410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff51ffa9f6c0e603f3cd4870105c3dfa12a3d43a4b7b011894d65e2e1b0314`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:42:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:42:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:42:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:42:38 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:42:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:42:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:42:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:42:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:42:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:42:43 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:33 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070e31b38b0b944ea72bcc0f45842389d7c60ef88d5d8e9d5d80fb74a71f3be`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 8.1 MB (8140525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a16c5f1d5dd8ae06d433603c1536495d2875c94969eeff1a97bd5f07b1d0bd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1deba3782f33b79656094a6c5dd2dabe967217e79e695749299086da1785e5`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 17.6 MB (17551855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22365c049259b23f0b92b559a7df2c4f543f849dd208cde9f187dd9631cdae7`  
		Last Modified: Fri, 14 Nov 2025 17:43:00 GMT  
		Size: 21.5 MB (21476531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403cdb0b5976caca12d3e73b658bd0b6852544a578b8c13a566f14c8c5cf89e0`  
		Last Modified: Fri, 14 Nov 2025 17:42:59 GMT  
		Size: 20.5 MB (20480366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b603366ed042cb8549765579cd20d942616ebae73cbbe18874bd0afabebe6`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108adebe7f11fc0bd949c11ddb31408463d7a0a2448f24ce7c1f57eb5c1efabd`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff3fa7ae35498948374fc7a2c541a2d7117f257c5ac84c0db2102d9caee4e`  
		Last Modified: Fri, 14 Nov 2025 17:42:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fbb9ab3af5e33bbb16665bd4743801e4c0bc0edf8f15d1f24ac3b873ef9cf9`  
		Last Modified: Fri, 14 Nov 2025 17:50:53 GMT  
		Size: 7.2 MB (7230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d9ee37936557e5e5e7ec317e4534765b3c8172adc5bf93a17c6e62f4b0274`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 89.9 KB (89945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c77cfca9a877080e55292eefd2344aeca081c4265ac88d3f9788851fff4200`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f622ba6a998ec6a0e7441faff66535b0b237b7dd9e99eb0e2f6a26858913ff1`  
		Last Modified: Fri, 14 Nov 2025 17:50:57 GMT  
		Size: 58.2 MB (58226630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f54398961fe271418301e8dcae9e53f00d878b96f8a8377091a69cbb0a7fb`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03f31f2f2fbd5b1caf9390b89a591da2910325080ba25bf25fd34ad8f0a62c`  
		Last Modified: Fri, 14 Nov 2025 17:50:52 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:92fb4cbe157b467796f3d3ff5a3e62a203de5b795996de10ade617404f1785dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff33814f2f295e159bd1f54fa696c6153b59888521a92bec74e8295bffe608`

```dockerfile
```

-	Layers:
	-	`sha256:382fff29d9320a2efad79391da82c3dc51464c69bab0602636a5506caed19263`  
		Last Modified: Fri, 14 Nov 2025 21:07:36 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:886e5ff459e6f6be26b7484994a8d14bebe4fab3ec9529c371290b026424424e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134835020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7491f7a31f2d5b452a5789d3b65287a5ca38f7662974f31846039905736fb6b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:45:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:45:29 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:45:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:45:32 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:45:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:45:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:45:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:45:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:45:37 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:51:08 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:51:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:51:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:51:12 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:51:12 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:51:12 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:51:12 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f4c88c001fa4adbc67b749450063be218fae491babf245892a1870c6e3f60`  
		Last Modified: Fri, 14 Nov 2025 17:45:52 GMT  
		Size: 7.5 MB (7461409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63344f3aea49c701c9b11d20c25b844cc51741427c4981e7ea1c46e3c4730`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc1948e096fd7e23c6a2afa991d5d78d960561c4b52d7a27d496d56ea46c48b`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 17.5 MB (17542686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b74e7d8ba7ed8d217fff407930571842b6d936dd1f667548bed9bbb8e4f6c`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 21.5 MB (21455831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db5718ddef38f49f0098b605150f18b3416ebcc6b840d9c5303bdf51a7041`  
		Last Modified: Fri, 14 Nov 2025 17:45:53 GMT  
		Size: 20.5 MB (20462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b24a5e7fc53c2253beb5e72498950c757aa2cb8373b24ca3d460016ce4a0d7`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97713ad98161e9a45f8c9a75ced42bb053482233f37737ce28c36d07e7c3f9f`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd379a14526d36259ad4865f6a3cc3abeb18446f73ffd3f20747817ebf94f4a9`  
		Last Modified: Fri, 14 Nov 2025 17:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c2cd84bc928c20d117c9d7635a90a39831b95e8052dff3cfe3cc1bd6f0f00`  
		Last Modified: Fri, 14 Nov 2025 17:51:33 GMT  
		Size: 6.5 MB (6538247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8831271b0fde493256cfdf625b8bd29b593b50a2e41b876bd0457c205d31e`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 86.4 KB (86382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71ccd6132c6fd73522dcd76d0bb847633486222624334da36abd2c47430fd8`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2cd691ecedb982457a39c51d8021b1c4d0b9f32c50a0a5577a9fb86883015`  
		Last Modified: Fri, 14 Nov 2025 17:51:44 GMT  
		Size: 58.1 MB (58057973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1737b7d7aac53a596ec07e87ad0b783fef1583571ae58abb857a9f11b74dd5`  
		Last Modified: Fri, 14 Nov 2025 17:51:31 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b20a0a6faa25f08f3ed0f08d263f46cb718486a08e704ddd3db37a2f2ea5c`  
		Last Modified: Fri, 14 Nov 2025 17:51:32 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:dd6b3fe3ba751f84e6dc47893d9fe7c3bd957326add76df24fb78fbf62430bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84995271acd51564889fcdb02992d8357b44c462262206e8359b295681d6d28`

```dockerfile
```

-	Layers:
	-	`sha256:69aedff7fce428d6fcf857b03c5f072505dac8dfe9a5cadb00d593c5c93d786d`  
		Last Modified: Fri, 14 Nov 2025 21:07:39 GMT  
		Size: 34.7 KB (34727 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bb993f24897a54351c5acb5d769b63d0108e0e786677f633c8d4458716100082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133979082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ed8a923f13f7602e40108a5b68dc701a9d2393812f9ae77eecc3604d129c0a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:46:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 14 Nov 2025 17:46:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 14 Nov 2025 17:46:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:46:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-amd64'; 			sha256='460680948a25b80e62ffe085cd2d7ef4088540f3f3f58734b445a31534198240'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v6'; 			sha256='bb50ae022407e185f9e77b5e8fec7b4460c3dab5b2f2007f74fa2d8f6b9296a5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm-v7'; 			sha256='d2a1b9a7b05d86b9f3b0b593edc2489b94ac9d27005966718374cd34cb840067'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-arm64'; 			sha256='f8e060a1a1e659d1c919d440652775320e8c2998b051eb4b5845bfcee9d85696'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-ppc64le'; 			sha256='1ad8ca464fdd5883c8b9c51294f21dac58f40acfab215371a35716c5aa1f78ee'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-riscv64'; 			sha256='d0dcc7eda556022d03403af24d8044fcefb7daf5ddb7a11f9c154800919bfa2f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.linux-s390x'; 			sha256='42f9615e3f812b4cbcec147923229ef7e404b7fe6107e10f196c7d10cdcac978'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 14 Nov 2025 17:46:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:46:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Nov 2025 17:46:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 14 Nov 2025 17:46:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 17:46:55 GMT
CMD ["sh"]
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 14 Nov 2025 17:50:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 14 Nov 2025 17:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 17:50:24 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Nov 2025 17:50:24 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 14 Nov 2025 17:50:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Nov 2025 17:50:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f2161899a1abb5d50fb6912c5aa2f9e6eba912c68d8b496eef06444930228`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c602134c557ea2f362bf95f06c9e93767d09a97301f0a1deaddc25f04fcc1a`  
		Last Modified: Fri, 14 Nov 2025 17:47:09 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1961ead4e0507fed8ab5135da65397ca2ccdc6ac4e712e30f01b997fd37dab`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 17.3 MB (17325945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe701f798b85048c5792d8b6c99b4e3ae1fa054ebeef572a96834953575f8438`  
		Last Modified: Fri, 14 Nov 2025 17:47:11 GMT  
		Size: 20.6 MB (20645339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac112059a0982f40132c4c6d71cbcc8b874dc166b3e58c7ecc5a852bcbde2`  
		Last Modified: Fri, 14 Nov 2025 17:47:14 GMT  
		Size: 19.9 MB (19869856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d076bdf6ad37fcee6a6bc455d311ed238188d1aeecdbb0ffe82b8a7728a04a1`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d57bb41964b288c9c8c25f376682c432893a713b28894dd4b4fe055f950ae`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f16cecc383cbf2dde4a689223b761384a6148fd0f797955bf80ce1fd9ce96`  
		Last Modified: Fri, 14 Nov 2025 17:47:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2028d7e174bec2fec70a48a6e2e5af0362dae7e6448a9a717eb13a16b64f2`  
		Last Modified: Fri, 14 Nov 2025 17:50:42 GMT  
		Size: 7.1 MB (7140889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88ac7a71510acfd95e68b94da000887f447d5bf427d1bd16cd8d9ae7da1a50`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 99.5 KB (99486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f6cd12f9422bf8d9798cc25a7afab0b3efbb95edafe0db28d591d3460a7ab`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6fb1c4f443080f4775a11a10e4ebb9d4dcf416613335fb59a97866675919c`  
		Last Modified: Fri, 14 Nov 2025 17:50:50 GMT  
		Size: 56.5 MB (56494090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bef92d1424078646093341c781b4d0a4108ffd29233017ebecf452578c96f07`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7be95fee2833251180b1f89458c92e825631a044971b9139eb1899074780ac`  
		Last Modified: Fri, 14 Nov 2025 17:50:41 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:3a293b40e13f7427b260b7b7f470a8b7265cdcc61e7dd66bf7aaf7f439a4382a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899d225e33fad6679da89493be4274ee067b3b9389d791946d24d2c5a59bcd04`

```dockerfile
```

-	Layers:
	-	`sha256:a46ef6333945bb9c7c1c75266c56c269547f0646013eb229d5855f9fbcac81d4`  
		Last Modified: Fri, 14 Nov 2025 21:07:42 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:772aaec5cedd47b99353c76851734473b2724c7cc430b0fcbc882c7246678b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `docker:windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:d4513656969f64c32a00ba744aa13642743751db9b7c2442493cff588fc97517
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1502f96214ca8b767265c2d1cf293ea85c27f0044acac3a5151b1c12e3ddc303`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Fri, 14 Nov 2025 17:55:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:55:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:55:41 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:55:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:55:54 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:56:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:56:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:56:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec8692dea2a7cfeb5456bb4b993de15f76c88f0be36ba06ff89c73fa28bd532`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3756c030c25ee9a0352e8d184c9972ad760203435a360f95000a3a9ea1483db5`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 369.1 KB (369110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438ea9e974311c3c3b6d58a49066378843912aecbb7cd0fb7d961e9c3854e226`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2397c1b0ac14feac44b1a8573714b74ed790b8508fb19c11a9d63dd27536c8d`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720e07e14cdad776989cc5b530a376ed2a8777fccbfd9e9f7d1c5e4f3159c198`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 19.4 MB (19418477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d75632fe4f81ec2a724f6cac9e1e96aa25cc0d69a55177dfc00fca22150e42`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb681c47e552d8f90a197e832ece2f5a916389ce91d7dcce373001a0cacf717`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d5289b2e911e0436443f61b478f4e7ea8fb47b49ca4f0b08c023964a93a67f`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3e80662571ee22f6f212588ff170fc2f9d03dfaf33c2ae73ac2de62dcafc55`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 23.9 MB (23922840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2d5545093c2c4372e7e37e9ffc58230f3166f4eacf2d4af33f7699bf03a4b3`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c9f72fd0ce28cce8b61e2e5039431d3b23df93018467b52b2668516b0aafc9`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbbff8fd62b3ff3bfc919aaad4ac8af852c56c386751789d24f339adc0282d0`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba18e5c2618956fa6278331e4654b4726703ba698d344205e51bca5670237e5b`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 22.7 MB (22671713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:abaa83761c38ffb230bcb50a1d39744533e9666965018cfa825b0eec05f8112e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836498567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21dfcb808df45545b0f05343454835ed030e1c989ec55b3d4f578ef9de30d1e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Fri, 14 Nov 2025 17:46:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:46:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:46:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:47:22 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:47:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:47:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:47:49 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:48:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6703b96ff9900204410d0399df239a7cabe4d5e73c952ec996266a8f45346`  
		Last Modified: Fri, 14 Nov 2025 17:56:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32feda2f6f8207494b3c9e9732ebb1862d3785b36a3e4525af2de8874ba5eee7`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 502.3 KB (502252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f8d186086c63ae6514fab9464ed5b6e84edc42d0f18d1c630bbfe43e115fef`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13d933136eb971ad9c95a6de8745441fa2624b2a27cfd060f8b3258851fe2`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8456085a802821a6c35870bb91704666a064351f24ebd7e591d39d0309f0839c`  
		Last Modified: Fri, 14 Nov 2025 17:56:41 GMT  
		Size: 19.4 MB (19420220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23228b265c8267351c3b090a7093eb367490e0702e3cb7cf5250970db0258a37`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b082f0bb7964878d7ab22207b5df4f055bfc7aa97819cc449f4d8d423b919bf2`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50ae099af18d834feac25c9900b0891a0109fb464ad8f58464aaa84dcdbc161`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a569077549ea2a7f686bf31019da93372c4d61bbfe68f9bd66f6c9b367cadce7`  
		Last Modified: Fri, 14 Nov 2025 17:56:42 GMT  
		Size: 23.9 MB (23925706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44babfbf95d13b45d09fd0e43b38bbd485fa8ceb0686cc0d6ab0d3c532121f6`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcda35700f9ec33e4f5daa7429fc8ee77d4b076e14c0f0abbade72372e0832c4`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a58f8f0d06a0c8958d452e24c82a314e37348a63b44db70f1bbb741e7727863`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69feff69baaaa2240d3c0bcddf4d4c711f13550cbc03ad8307b009d44ea6a26`  
		Last Modified: Fri, 14 Nov 2025 17:56:40 GMT  
		Size: 22.7 MB (22677039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:43bb8e65e5e41a0bee0bea69e5cc5b33d765055b0de0b6bc9584152cf3cbfdfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull docker@sha256:abaa83761c38ffb230bcb50a1d39744533e9666965018cfa825b0eec05f8112e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1836498567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21dfcb808df45545b0f05343454835ed030e1c989ec55b3d4f578ef9de30d1e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Fri, 14 Nov 2025 17:46:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:46:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:46:57 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:46:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:47:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:47:22 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:47:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:47:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:47:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:47:49 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:48:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6703b96ff9900204410d0399df239a7cabe4d5e73c952ec996266a8f45346`  
		Last Modified: Fri, 14 Nov 2025 17:56:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32feda2f6f8207494b3c9e9732ebb1862d3785b36a3e4525af2de8874ba5eee7`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 502.3 KB (502252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f8d186086c63ae6514fab9464ed5b6e84edc42d0f18d1c630bbfe43e115fef`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13d933136eb971ad9c95a6de8745441fa2624b2a27cfd060f8b3258851fe2`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8456085a802821a6c35870bb91704666a064351f24ebd7e591d39d0309f0839c`  
		Last Modified: Fri, 14 Nov 2025 17:56:41 GMT  
		Size: 19.4 MB (19420220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23228b265c8267351c3b090a7093eb367490e0702e3cb7cf5250970db0258a37`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b082f0bb7964878d7ab22207b5df4f055bfc7aa97819cc449f4d8d423b919bf2`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50ae099af18d834feac25c9900b0891a0109fb464ad8f58464aaa84dcdbc161`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a569077549ea2a7f686bf31019da93372c4d61bbfe68f9bd66f6c9b367cadce7`  
		Last Modified: Fri, 14 Nov 2025 17:56:42 GMT  
		Size: 23.9 MB (23925706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44babfbf95d13b45d09fd0e43b38bbd485fa8ceb0686cc0d6ab0d3c532121f6`  
		Last Modified: Fri, 14 Nov 2025 17:56:39 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcda35700f9ec33e4f5daa7429fc8ee77d4b076e14c0f0abbade72372e0832c4`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a58f8f0d06a0c8958d452e24c82a314e37348a63b44db70f1bbb741e7727863`  
		Last Modified: Fri, 14 Nov 2025 17:56:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69feff69baaaa2240d3c0bcddf4d4c711f13550cbc03ad8307b009d44ea6a26`  
		Last Modified: Fri, 14 Nov 2025 17:56:40 GMT  
		Size: 22.7 MB (22677039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:3d255dbdfb3cd84597679d5d3ca0b4a9eba95cd13ee76c69e3ed677b0d2c8406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull docker@sha256:d4513656969f64c32a00ba744aa13642743751db9b7c2442493cff588fc97517
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3301849678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1502f96214ca8b767265c2d1cf293ea85c27f0044acac3a5151b1c12e3ddc303`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Fri, 14 Nov 2025 17:55:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Nov 2025 17:55:39 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Nov 2025 17:55:41 GMT
ENV DOCKER_VERSION=29.0.1
# Fri, 14 Nov 2025 17:55:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.0.1.zip
# Fri, 14 Nov 2025 17:55:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_VERSION=0.30.0
# Fri, 14 Nov 2025 17:55:53 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.0/buildx-v0.30.0.windows-amd64.exe
# Fri, 14 Nov 2025 17:55:54 GMT
ENV DOCKER_BUILDX_SHA256=616ddbe97ab40946ee736f0adb6c8ee58328742086af06823d2491ddae6c22ae
# Fri, 14 Nov 2025 17:56:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Nov 2025 17:56:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-windows-x86_64.exe
# Fri, 14 Nov 2025 17:56:03 GMT
ENV DOCKER_COMPOSE_SHA256=4c864dd7f879dd40366e087e68a8a02cbcf018be0128867b13369898e67e1532
# Fri, 14 Nov 2025 17:56:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec8692dea2a7cfeb5456bb4b993de15f76c88f0be36ba06ff89c73fa28bd532`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3756c030c25ee9a0352e8d184c9972ad760203435a360f95000a3a9ea1483db5`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 369.1 KB (369110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438ea9e974311c3c3b6d58a49066378843912aecbb7cd0fb7d961e9c3854e226`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2397c1b0ac14feac44b1a8573714b74ed790b8508fb19c11a9d63dd27536c8d`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720e07e14cdad776989cc5b530a376ed2a8777fccbfd9e9f7d1c5e4f3159c198`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 19.4 MB (19418477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d75632fe4f81ec2a724f6cac9e1e96aa25cc0d69a55177dfc00fca22150e42`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb681c47e552d8f90a197e832ece2f5a916389ce91d7dcce373001a0cacf717`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d5289b2e911e0436443f61b478f4e7ea8fb47b49ca4f0b08c023964a93a67f`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3e80662571ee22f6f212588ff170fc2f9d03dfaf33c2ae73ac2de62dcafc55`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 23.9 MB (23922840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2d5545093c2c4372e7e37e9ffc58230f3166f4eacf2d4af33f7699bf03a4b3`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c9f72fd0ce28cce8b61e2e5039431d3b23df93018467b52b2668516b0aafc9`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbbff8fd62b3ff3bfc919aaad4ac8af852c56c386751789d24f339adc0282d0`  
		Last Modified: Fri, 14 Nov 2025 18:14:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba18e5c2618956fa6278331e4654b4726703ba698d344205e51bca5670237e5b`  
		Last Modified: Fri, 14 Nov 2025 18:14:22 GMT  
		Size: 22.7 MB (22671713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
